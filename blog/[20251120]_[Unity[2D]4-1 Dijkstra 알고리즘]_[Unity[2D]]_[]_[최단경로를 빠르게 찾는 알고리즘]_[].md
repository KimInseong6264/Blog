# Dijkstra 알고리즘

### 길 찾기 알고리즘
- F(최종 비용) = G(인접 노드 간의 거리)
1. 내 주변 레이더를 한 바퀴 돌린다.
2. 레이더에 걸리는 이동 가능 지점들의 각 이동비용을 openList에 정리
3. 비용이 가장 저렴한 경로로 이동하고 visitedList에 체크
   (비용은 방문기록이 없는 경로는 이미 이동한 비용까지 누적해서 기록)
4. 위의 내용을 반복
5. 도착지에 도착할 시에 이전 


#### 사용 List
1. openList : 방문 직전 
2. closedList
3. G

```
class DijkstarNode
{
    // ABCD, 0123 번호
    public int Index;
    // 해당 노드의 좌표
    public Vector2 Pos;
    // 시작점으로부터 현재 노드까지의 누적 거리
    public float Distance;
    // 경로 추적용 부모 노드
    public DijkstarNode Parent;

    public DijkstarNode(int index, Vector2 pos, float distance, DijkstarNode parent = null)
    {
        Index = index;
        Pos = pos;
        Distance = distance;
        Parent = parent;
    }
}

public class DijkstraExample : MonoBehaviour
{
    // 노드 표현용 변수
    int A = 0; int B = 1; int C = 2; int D = 3;  

    private void Start()
    {
        int n = 4; // 노드 개수
        int startIndex = A; // 시작 노드 인덱스 A
        int goalIndex = D; // 목표 노드 인덱스 D

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

        // 각 노드까지의 최소 거리 저장 배열
        float[] distances = new float[n];
        for (int i = A; i < D; i++)
        {
            distances[i] = float.MaxValue;
        }

        // 시작 위치
        distances[startIndex] = 0;

        // 방문 여부 저장 배열
        bool[] visited = new bool[n];

        // 탐색 대기 리스트
        var openList = new List<DijkstarNode>();
        openList.Add(new DijkstarNode(startIndex, positions[startIndex], 0));

        // 탐색 루프
        while (openList.Count > 0)
        {
            // 거리 기준으로 정렬
            openList.Sort((a,b) => a.Distance.CompareTo(b.Distance));

            // 최소 거리 노드 선택
            var current = openList[A];

            // 선택한 애는 탐색 대상에서 제외해주기
            openList.RemoveAt(A);

            // 방문한 노드면 스킵하기
            if (visited[current.Index])
                continue;

            // 방문처리
            visited[current.Index] = true;

            // 목표 노드 도착시 경로 복원
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

                // D - C -B -A

                path.Reverse();

                // A - B - C - D

                Debug.Log("Djkstra Path" + string.Join(" -> ", path));
                Debug.Log("Distance " + current.Distance);

                break;
            }

            // Goal인 노드가 아니면 다음 노드를 찾으면 됨
            foreach (var neighbor in graph[current.Index])
            {
                // 이미 방문한 노드는 패스
                if (visited[neighbor.to])
                    continue;

                // 현재 노드까지의 거리 + 간선 비용
                float t = current.Distance + neighbor.cost;

                // 더 짧은 경로 발견시
                if (t < distances[neighbor.to])
                {
                    distances[neighbor.to] = t;

                    // 새로운 노드 추가
                    openList.Add(new DijkstarNode(neighbor.to, positions[neighbor.to],t, current));
                }
            }
        }
    }
}
```