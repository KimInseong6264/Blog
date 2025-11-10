# Ⅱ. 구조체


### 1. 구조체란?
---
**※ 구조체 :** 하나의 박스에 여러 타입의 자료형을 담을 수 있게 하는 것
- 열거형과 비슷하게 struct로 지시, 새로운 자료형을 만들어 냄
- 클래스와 달리 **값 타입**을 가진다.
- 비슷한 내용을 폴더화해서 가독성을 높임
- 구조체 속의 변수들을 **"멤버변수" , "필드"** 라고 부름
- 구조체는 폴더를 만들고 그 안에 여러 파일들을 집어넣는 것과 같음
- 클래스에 비해 몇 줄 안 되는 걸 정의할 때 사용(작은 값빠르게 연산 목적)
- ex) 벡터(x , y , z)

![](https://velog.velcdn.com/images/iissk/post/a9bf3b4e-0f7d-47b7-bf64-644de5bd4ccf/image.png)

▶ 구조체를 사용하지 않는다면 비슷한 내용을 계속해서 사용하면서 가독성이 떨어짐

### 2. 구조체 사용법
---
![](https://velog.velcdn.com/images/iissk/post/e73259bd-e844-4b1f-b4d3-afe89de51790/image.png)

▶ 구조체의 선언 방식<br>
▶ 클래스 밖에 선언하는 습관

![](https://velog.velcdn.com/images/iissk/post/ab5314ca-5eeb-4af0-9565-a8a08894408d/image.png)

![](https://velog.velcdn.com/images/iissk/post/37379bed-59fe-4358-86f6-6c3f2b15ec37/image.png)

▶ 구조체의 초기화 방법 : 변수 지정 = new 자료형() { 속성 초기값(쉼표구분) }

![](https://velog.velcdn.com/images/iissk/post/b8bcab5a-ab32-4fa8-8054-8456525df983/image.png)

![](https://velog.velcdn.com/images/iissk/post/57520ae0-0fb9-4838-b35b-6d420849352f/image.png)

▶ Car 자료형을 형성하면 중괄호 내의 내용이 한꺼번에 생성됨<br>
▶ Main에서 각 멤버변수에 값을 일일히 지정해서 사용이 가능

![](https://velog.velcdn.com/images/iissk/post/9f9ff82d-f6e2-4dca-bc36-49e3c2617330/image.png)

![](https://velog.velcdn.com/images/iissk/post/b431a2b0-e2f9-4270-a99b-f25439c3a973/image.png)


▶ 구조체 자료형으로 변수 지정 후 변수에 *구조체 내의 속성*에 값을 넣어야 함<br>
▶ 배열로 지정할 수 있으며, 이 경우 각 배열 각 칸에 값을 입력해주기

**※배열에 구조체 넣기**
![](https://velog.velcdn.com/images/iissk/post/f150f0db-3258-4e41-aafe-a976238dedf3/image.png){: .align-left}

1. 구조체 각 변수의 속성들에 각각 값을 지정 
2. 각 변수들을 새롭게 지정한 배열에 각각 변수를 삽입
- 2개 속성 이상의 변수의 초기값은 
  *new 구조체명();* 으로 지정




> ![](https://velog.velcdn.com/images/iissk/post/1f005983-1ab7-4c2c-b088-f36b2c374a9c/image.png){: .align-left}
▶ 구조체의 생성자 표현도 가능하다.




>## <p style="color:green"> 🤔 마무리</p>
> 클래스를 배우게 되면 자주 사용하는 개념은 아니다.
<br> 하지만 간단한 몇 개의 정보를 담고 있는 데이터에서 사용이 용이하다.
<br> <p style="color:blue"> 
구조체는 클래스보다 **코드가 가볍다는 것**이 장점이다. 하지만 범용적으로 사용하기엔 한계가 있어서 적은 값이어도 자주 사용이 되는 Vector와 같은 곳에서 사용된다. </p>