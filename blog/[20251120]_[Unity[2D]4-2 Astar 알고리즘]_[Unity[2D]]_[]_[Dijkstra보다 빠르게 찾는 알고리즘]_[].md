# Astra 알고리즘

### 길찾기 알고리즘
- F(최종 비용) = G(인접 노드 간의 거리) + H(예측치)
1. 1. 내 주변 레이더를 한 바퀴 돌린다.
2. 레이더에 걸리는 이동 가능 지점들의 각 이동비용을 openList에 정리
3. 비용이 가장 저렴한 경로로 이동하고 visitedList에 체크
   (비용은 방문기록이 없는 경로는 이미 이동한 비용까지 누적해서 기록)
4. 위의 내용을 반복
5. 도착지에 도착할 시에 이전 

H(휴리스틱): 최종 목적지를 기준으로 값을 처음에 정함

#### 사용 List
1. openList : 방문 직전 
2. closedList
3. G
4. H
5. F

```
class AstarNode : IComparable<AstarNode>
{
    public int Index;  // 노드 인덱스, 구별값 ABCD 0123
    public Vector2 pos;  // 노드 위치
    public float G;  // 시작점에서 지금 위치까지의 실제 비용
    public float H;  // 휴리스틱, 예측 비용
    public float F => G + H;  // 총 점수, 가중치
    public AstarNode Parent;  // 부모 노드, 경로 복원 용도

    public AstarNode(int index, Vector2 pos, float g, float h, AstarNode parent = null)
    {
        Index = index;
        this.pos = pos;
        this.G = g;
        this.H = h;
        Parent = parent;
    }

    // F값 기준 정렬을 위한 비교 함수
    public int CompareTo(AstarNode other)
    {
        // F값으로 우선 비교해보기
        int fCompare = F.CompareTo(other.F);
        if (fCompare != 0) 
            return fCompare;

        // F값이 같을 경우 인덱스 기준 비교하기
        return Index.CompareTo(other.Index);
    }
}

public class AstarExample : MonoBehaviour
{
    // 노드 표현용 변수
    int A = 0; int B = 1; int C = 2; int D = 3;

    // 두 좌표 사이의 거리를 휴리스틱으로 사용하기로 함
    static float Heuristic(Vector2 a, Vector2 b) => Vector2.Distance(a, b);

    private void Start()
    {
        int n = 4;
        int startIndex = 0;
        int goalIndex = 3;

        // 각각의 노드에 좌표 설정해주기(그냥 시각적인 위치를 표현하기 위한 틀 만든 것)
        Vector2[] positions = new Vector2[4]
        {
            new Vector2 (0, 0), // A
            new Vector2 (1, 0), // B
            new Vector2 (0, 1), // C
            new Vector2 (1, 1), // D
        };

        // 그래프 구성(graph[i]의 i는 출발 위치를 의미 0 => A , 1 => B , 2 => C)
        List<(int to, float cost)>[] graph = new List<(int to, float cost)>[n];
        for (int i = 0; i < n; i++)
        {
            graph[i] = new List<(int to, float cost)>();
        }

        // 비용 정보 추가 
        graph[A].Add((B, 1)); // A -> B (1)
        graph[A].Add((C, 4)); // A -> C (4)
        graph[B].Add((C, 2)); // B -> C (2)
        graph[B].Add((D, 6)); // B -> D (6)
        graph[C].Add((D, 3)); // C -> D (3)

        // G 점수 배열 초기화
        float[] gScores = new float[n];
        for (int i = A; i < D; i++)
        {
            gScores[i] = float.MaxValue;
        }

        // 시작 위치
        gScores[startIndex] = 0;

        // 방문 여부
        bool[] closed = new bool[n];

        // 오픈 리스트, 탐색 대상들
        var openList = new List<AstarNode>();

        // 시작 지점 추가( + 휴리스틱 수치만 추가)
        openList.Add(new AstarNode(startIndex, positions[startIndex], 0,
            Heuristic(positions[startIndex], positions[goalIndex])));

        // 탐색 루프
        while (openList.Count > 0)
        {
            // F값 기준 정렬
            openList.Sort((a,b) => a.CompareTo(b));

            // 가장 F가 낮은 노드 찾아오기
            var current = openList[0];

            // 방문한 노드는 제거
            openList.RemoveAt(0);

            // 이미 방문한 노드면 패스
            if (closed[current.Index])
                continue;

            // 방문처리
            closed[current.Index] = true;

            // 목표에 도달했으면 경로 복원
            if (current.Index == goalIndex)
            {
                // 경로 저장용 리스트
                var path = new List<int>();
                var temp = current;

                // 부모 따라 역추적
                while (temp != null)
                {
                    path.Add(temp.Index);
                    temp = temp.Parent;
                }

                // 역순으로 들어갔으니까 뒤집기
                // D - C -B -A
                path.Reverse();

                // A - B - C - D

                Debug.Log("A* Path Path" + string.Join(" -> ", path));
                Debug.Log("Distance " + current.G);

                break;
            }

            // 인접 노드 탐색
            foreach (var neighbor in graph[current.Index])
            {
                // 이미 처리한 노드는 패스
                if (closed[neighbor.to])
                    continue;

                // 현재의 G + 이동 비용 계산
                float t = current.G + neighbor.cost;

                // 더 짧은 경로 발견시 갱신
                if (t < gScores[neighbor.to])
                {
                    gScores[neighbor.to] = t;

                    // H값 계산
                    float h = Heuristic(positions[neighbor.to], positions[goalIndex]);

                    // 새로운 노드 추가
                    openList.Add(new AstarNode(neighbor.to, positions[neighbor.to],t,h,current));
                }
            }

        }
    }
}
```