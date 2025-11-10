# Ⅱ. 조건문switch

### 1. switch문
---
**※switch문의 기본 형태**

![](https://velog.velcdn.com/images/iissk/post/95b303e4-1686-4422-8349-034a15c6366a/image.png)
▶ 조건에 입력되는 특정한 값에 대한 선택지 설정이 용이함 <br> 
ex) 웹RPG처럼 선택지에 따라 이동하는 것에 사용

![](https://velog.velcdn.com/images/iissk/post/e7adb60a-77ee-49ba-b8ef-8486429e061e/image.png)
▶ Console.ReadLine(); 을 통해 유저가 입력한 것에 따라 선택지 선택이 가능

- switch문은 if문에 비해 논리연산이 어렵다.


### 2. switch문 + if문
---
**※두 개의 연산자를 통해 선택지를 고르면 이동하는 게임 만들기**

![](https://velog.velcdn.com/images/iissk/post/0757ef43-0a59-47a8-aeb1-ec70a2e02f21/image.png)
▶ 선택지 출력과 유저 입력을 TryParse로 받는다.

![](https://velog.velcdn.com/images/iissk/post/e95e26eb-fc82-499c-8f69-3118b39fcbe0/image.png)
▶ swich문으로 각 선택지에 해당하는 장소로 이동 출력한다. <br> 
▶ if문으로 유저가 숫자가 아닌 값을 입력할 때 올바르지 않다는 것을 출력한다.


> ## 🤔 마무리
> switch는 사실 if문에 비해 자주 사용하는 느낌은 아니다.  
> 하지만 여러 종류의 경우(case) 중에서 선택적으로 실행을 할 때에는 가독성을 높이는 방법이었다.  
> **주의할 점은 반드시 break을 통해 각 상황이 끝난 것을 구분해 주어야 하며,  
> 이 때의 break은 추후의 반복문의 break과는 별개로 동작한다는 것을 기억하자!