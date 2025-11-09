# Ⅰ. 조건문if

### ※조건문
##### 조건문은 특정 조건이 만족하면 조건문의 대괄호 안에있는 코드를 수행하라 라고 정의하는 겁니다.
---

#### 1. if문 
- 변수가 특정 조건에 알맞는지 판단하여 True값으로 판단되었을 때, if문 안의 있는 내용을 실행한다.
- 조건을 만족하지 않는다면 if문 전체를 생략하고 다음 내용을 실행

if( 괄호 안이 'True'라면 조건문 실행 )
{
      여기 중괄호 내용 실행
}

![](https://velog.velcdn.com/images/iissk/post/6e8cc2b5-1764-44e8-8f3d-38b396da33e9/image.png)

#### 2. else if & else
**1) else if**
- if문 직후에 연결되는 조건문으로 if문에 해당하지 않은 것들 중에 else if의 조건을 만족하면 조건문 안의 내용을 실행
- else if 이후로 다른 조건으로 연속적으로 사용이 가능

else if( 앞선 if문을 만족하지 않는 것들 중에 괄호 안이'True'라면 조건문 실행 )
{
      여기 중괄호 내용 실행
}

**2) else**
- 앞선 if와 else if의 조건에 맞지 않는 모든 조건들에 대해 실행함
- 예외인 모든 조건에 해당함으로 괄호를 따로 사용하지 않음

else
{
      여기 중괄호 내용 실행
}

![](https://velog.velcdn.com/images/iissk/post/4f6f8784-6d3d-41c2-995d-8d01007c3ac2/image.png)

#### 3. if문 논리연산
- 논리연산: 'and'와 'or'과 'not'에 해당하는 연산

![](https://velog.velcdn.com/images/iissk/post/fe5cb7aa-f6e9-412b-bc23-7aab494bcba0/image.png)


![](https://velog.velcdn.com/images/iissk/post/acfa14ec-56ce-4d20-b088-325c2b2f5dd1/image.png)


> ## 🤔 마무리
> if는 코딩을 하면서 평생 사용되는 가장 중요한 문법이다!  
> 함수의 동작 조건, 동작 시 제한조건을 만드는 등 많은 경우에 사용된다.  
> **만약 프로그램 동작 시켰을 때, 버그 발생시에 조건이 맞게 들어갔는지부터 확인하자....**
> <br>의도한 조건과 다른 조건이 들어가서 객체가 무한히 이동하거나, 무한 생성 되는 문제가 있던 게 한 두번이 아니었던....