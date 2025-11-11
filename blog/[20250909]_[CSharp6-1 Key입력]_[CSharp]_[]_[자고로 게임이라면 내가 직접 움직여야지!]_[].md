# Ⅰ. Key입력



### 1. 키입력
---
**※ConsoleKeyInfo :** 콘솔 내에서 만들어져 있는 키입력을 하도록 지시하는 자료형

![](https://velog.velcdn.com/images/iissk/post/6a221bd5-de64-4a1e-8cb4-28e97e6dd091/image.png)

![](https://velog.velcdn.com/images/iissk/post/e2d4f3a0-56fb-4afc-b9d4-1a117a50ea98/image.png)

▶ 키입력 기본 세팅

![](https://velog.velcdn.com/images/iissk/post/9f73c1ef-21e7-42c8-836c-7a5141e59a08/image.png)

▶ 변수.Key : 변수에 입력된 콘솔 키를 가져오는 것이다.


### 2-1. 키입력 응용
---
![](https://velog.velcdn.com/images/iissk/post/26b90d31-5d63-4a1f-b13a-d9268f8989c4/image.png)

▶ 키 입력을 통한 커서 이동을 진행하기
![](https://velog.velcdn.com/images/iissk/post/3f05c626-255b-475b-9d42-917c43168ec3/image.png)

▶ x , y 변수를 이용해 x축, y축 이동을 시킬 수 있다.

![](https://velog.velcdn.com/images/iissk/post/ccc9e349-88a6-4c7c-a0c8-078e21f1da41/image.png)

▶ 해당 case의 키를 입력하면 x , y가 변하면서 Console.SetCursorPosition(x, y); 를 이용해서 커서 이동을 시키게 된다.



### 2-2. 뱀 그리기
---
![](https://velog.velcdn.com/images/iissk/post/2743ca6c-dcc4-4102-930e-0cb78a645b6d/image.png)

▶ 초기 변수 지정

![](https://velog.velcdn.com/images/iissk/post/3794412d-ca29-4ffd-934e-8e0d581350d2/image.png)

▶ 특정 키 입력으로 커서의 위치를 변형하게 된다.

**※방어코드:** 의도와 다르게 프로그램이 종료되는 것을 방지하기 위해 작성하는 코드
ex) 위의 예시에서는 x , y가 음수가 되지 않아야 함으로 코드가 추가됨

![](https://velog.velcdn.com/images/iissk/post/206c4f01-2756-4564-8ed7-e2b326f0250b/image.png)

▶ 키입력을 통해 자취를 남기는 프로그램 제작


>## <p style="color:green"> 🤔 마무리</p>
> 결국 플레이어가 직접 움직이지 않으면 게임이 아니다. 그냥 영상 시청하는 거지...
<br> 키입력 자체는 어려운 개념은 아니지만 뭔가 응용하는 것에서 어려움을 느낄 것 같았다.
<br> 하지만 원리 자체만 보면 **반복문 안(Unity에선 Update)에서 키입력이 들어오면 조건을 실행한다**
<br> 이것만 기억하면 된다.