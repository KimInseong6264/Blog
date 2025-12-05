
# Ⅰ. 피셔 에이츠 셔플


#### ※알고리즘 및 코드
```
 public static void FirsherYatesShuffle(int[] inputArr)
 {
     Random random = new Random();   //섞을꺼니까 랜덤

     for (int i = inputArr.Length - 1; i > 0; i--) //인덱스 역순
     {
         int j = random.Next(0, i + 1);  //0부터 i까지 랜덤 인덱스 선택

         int temp = inputArr[i];
         inputArr[i] = inputArr[j];
         inputArr[j] = temp;
     }
 }
 ```


![](https://velog.velcdn.com/images/iissk/post/1d127dac-8d3a-4d24-a5d5-1453274730e7/image.png)

1. 끝 자리 인덱스의 값을 다른 자리의 값과 바꾼다.
2. 인덱스를 1씩 낮추고, 그 이하의 인덱스 값과 값을 바꾼다.
3. 2를 반복하면서 1번 인덱스에서의 셔플이 끝나면 셔플이 끝난다.