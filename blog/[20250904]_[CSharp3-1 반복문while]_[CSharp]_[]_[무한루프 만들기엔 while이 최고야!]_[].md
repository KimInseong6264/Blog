# Ⅰ. 반복문while


### 1. 반복문 안에 반복문
---
- for문 안에 또 하나의 반복문을 집어넣어서 계산한다.
- 각 for문에 해당하는 변수는 반복문 안에 있는 동안에는 지역변수로 사용이 가능하다.
   ㄴ for문을 나가게 되면 해당 변수는 사라지게 됨

![](https://velog.velcdn.com/images/iissk/post/efaca191-9a17-416c-a772-e8a3d0e2f770/image.png)


### 2. while문
---
```
while( 이 내용이 참이라면 반복진행 )
{
    여기 내용을 반복
}
```

![](https://velog.velcdn.com/images/iissk/post/aaf36a4d-c5e5-4572-95ca-5f829190c445/image.png)

- for문에 비해 조건의 기입방식이 간단하지만 복잡한 조건 설정은 불편함
- 부한루프를 만들 때 유용함

<img src="../img/Mine/{B7D358F5-871B-43B7-8A5B-E025202FDC49}.png">

### 3. Break문과 Continue문
---
**1) Break문**
- 반복문에서 루프를 즉시 종료시키는 키워드
- 반복문 안에 종료하고 싶은 부분에 break; 입력시 해당 내용 수행하고 곧바로 반복문을 나오게 됨

![](https://velog.velcdn.com/images/iissk/post/03a7dc16-7326-451e-b7f2-beed4d714151/image.png)

![](https://velog.velcdn.com/images/iissk/post/b42fd72a-2a46-40c3-97bf-d8ae4b2ca717/image.png)


**2) Continue문**
- 반복문에서 다음 반복을 시작하는 키워드
- 반복문에서 continue를 만나게 되면 아래의 어떤 코드라도 시행하지 않고 다음 반복을 진행함

![](https://velog.velcdn.com/images/iissk/post/db0d0982-84cc-4de6-8993-968628bf26a8/image.png)

![](https://velog.velcdn.com/images/iissk/post/69a6d96b-284a-4148-a594-b7d9b83293c2/image.png)



>**무한 입력 루프**

- 사용자에게 입력을 받을 때, 숫자가 아닌 경우 다시 입력을 받게 되는 무한 루프 형성

![](https://velog.velcdn.com/images/iissk/post/1343d502-2061-4257-8a85-633a71665481/image.png)
▶ TryParse를 활용해서 false값(숫자 이외의 입력)을 입력시, 루프를 반복하는 방식

> **선택지 무한 입력 루프**

- switch를 이용해서 선택지를 구분하며, 선택지 이외의 선택시 이동이 불가능하도록 무한루프 형성

![](https://velog.velcdn.com/images/iissk/post/c920b6f8-e13b-4681-bc7f-bbe98ddad74a/image.png)


> ## 🤔 마무리
> while은 간단한 조건을 걸어서 반복문을 형성하는 문법이다.
<br> 간단한 대신 복잡한 조건을 이용할 수는 없지만, **무한루프를 만들어야 하는 경우, 대표적으로는 콘솔 프로젝트에서 콘솔창이 꺼지지 않도록 while문으로 포장을 할 때 유용하게 사용했다.**