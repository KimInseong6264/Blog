# Ⅱ. 정렬 방법


## 1. Bubble 정렬

**알고리즘**
1. 배열을 반복하면서, 인접한 두 값을 비교합니다
2. 두 값이 크기 순서에 맞지 않으면 위치를 교환합니다
3. 배열이 끝까지 비교를 반복하면 가장 큰 값이 배열 끝으로 이동
4. 배열이 정렬될 때까지 위 과정을 반복

```
public static void BubbleSort(int[] array)
{
    for (int i = 0; i < array.Length; i++)  //일단 0부터 모든 요소 반복
    {
        for (int j = 0; j < array.Length - i - 1; j++)
        {
            if (array[j] > array[j + 1]) //잘못된 순서라면?
            {
                int temp = array[j];
                array[j] = array[j + 1];
                array[j + 1] = temp;
            }
        }
    }
}
```
▶ 첫번째 인덱스의 수부터 옆에 있는 수와 비교해서 자신이 큰 값이면 자리를 바꾸는 것을 반복하며 정렬하는 방법

<br>

## 2. Seection 정렬

**알고리즘**
1. 0번의 인덱스의 값을 기준으로 잡는다.
2. 기준인 값을 다른 인덱스들과 비교한다.
3. 기준보다 작은 값이 있으면 기준을 바꿔서 나머지들과 비교
4. 최종으로 남은 기준은 최소값이 되어 0번 인덱스에 넣는다.(0번의 값과 자리 바꿈)
5. 인덱스를 1씩 올리면서 반복한다.

```
public static void SeletionSort(int[] array)
{
    for (int i = 0; i < array.Length - 1; i++)
    {
        int minIndex = i;                       //하나를 선택하여 기준을 잡고
        for (int j = i + 1; j < array.Length; j++)
        {
            if ((array[j] < array[minIndex]))   //반복을 돌며 그 선택된 애랑 비교
            {
                minIndex = j;   //반복을 돌다가 필요할 경우 최소값을 j로 바꿈
            }


            //이제 여기까지 왔다는 뜻은, 배열 끝까지 다 봤다는 뜻이니
            //최소값을 현재 위치로 교환
            int temp = array[minIndex];
            array[minIndex] = array[i];
            array[i] = temp;

        }
    }
}
```
▶ 앞에서부터 최소값을 찾아서 최소값 순서로 정렬을 하는 방법

<br>

## Insertion 정렬

**알고리즘**
1. Key가 되는 기준 값을 정한다.
2. Key 이하의 인덱스들의 값들을 비교한다.
3. Key보다 큰 수면 오른쪽으로 보낸다.
4. Key가 더 이상 인덱스 이동이 없으면 Key를 고른 인덱스를 1증가시킨다.
5. 위의 시행을 반복한다.

```
//정렬되지 않은 데이터를 알맞은 자리에 끼워넣는다.
public static void InsertionSort(int[] arr)
{
    int n = arr.Length;

    for (int i = 1; i < n; i++)
    {
        int key = arr[i];
        int j = i - 1;
        
        //  key보다 큰 요소들을 한 칸씩 뒤로 이동
        while (j >= 0 && arr[j] > key)
        {
            arr[j + 1] = arr[j];
            j--;
        }

        arr[j + 1] = key;
    }
}
```
▶ 특정 Key값로 정한 값의 자리부터 정확히 정해주면서 점차 인덱스를 높여가는 정렬방법 높여가는 정렬방법


#### 각 정렬의 시간 복잡도

![](https://velog.velcdn.com/images/iissk/post/05352646-37a6-42ec-90e7-16462c942403/image.png)
