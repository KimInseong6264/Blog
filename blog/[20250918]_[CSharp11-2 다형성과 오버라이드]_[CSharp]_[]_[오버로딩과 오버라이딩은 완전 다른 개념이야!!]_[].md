# Ⅱ. 다형성과 오버라이드

### 1. 다형성
---
**※다형성:** 부모클래스 객체를 자식클래스의 인스턴스로 채워넣을 수 있는 것
- 업캐스팅 - 자식  객체를 부모 객체로 타입을 바꿔 넣는 것(기본적으로 가능)
- 다운캐스팅 - 부모 객체를 자식 객체로 타입을 바꿔 넣는 것(is , as등을 사용해야 함)


![](https://velog.velcdn.com/images/iissk/post/80554acd-a8f0-4b46-bd0d-9d0bc21aa039/image.png)

▶ Car 자료형에 Sedan , Bulldoser 라는 자식 클래스의 인스턴스가 담길 수 있다.


![](https://velog.velcdn.com/images/iissk/post/ebb12cbc-e907-4f11-af34-f09715b7058e/image.png)

▶ 파생클래스 기준으로 다른 파생클래스 , 부모클래스를 담을 수는 없다.
▶ **(부모클래스) = (자식클래스);** 형태로만 담을 수 있다.


![](https://velog.velcdn.com/images/iissk/post/f3a5af2d-06f7-4b55-9404-4c6e74857ffc/image.png)

▶ Car배열을 1개를 만들고 다형성을 이용해 Car배열에 자식 클래스들을 담아내며 코드가 간소화 되었다.



### 2. 오버라이딩
---
**※오버라이딩:** 상속관계에서 부모클래스의 메서드를 파생클래스에서 재정의 하여 사용하는 것
- "권한을 덮어씌다" , "재정의하다"라는 의미

오버로딩이 클래스 내에서 동일한 이름으로 추가 정의하는 것이라면, 오버라이딩은 클래스 간 상속 관계에서 메서드를 재정의하는 것

![](https://velog.velcdn.com/images/iissk/post/8afc7bcc-88f5-4baf-b4dc-dbfb53280deb/image.png)

▶ **부모클래스와 동일한 이름의 메서드 사용시,** 부모 클래스의 메서드가 먼저 동작한다.


![](https://velog.velcdn.com/images/iissk/post/e4bded05-843b-4497-ae98-da2ee413ac88/image.png)

▶ **virtual :** 자식이 재정의하도록 허락을 해준다.(본래 메서드에 영향을 주지 않는다.)
▶ **override :** 부모의 메서드와 다르게 재정의하겠다.


![](https://velog.velcdn.com/images/iissk/post/abd827ff-6286-4f8b-af2c-76c1d5b5b74d/image.png)

▶ 오버라이딩 이후로는 각 파생클래스에 해당되는 메서드(Drive)로 출력이 된다.


![](https://velog.velcdn.com/images/iissk/post/2efcbfea-0471-4b41-9b37-61d89ea52b34/image.png)

▶ **base.메서드 :** 부모 클래스의 메서드를 호출
- 파생 클래스에서 base클래스의 메서드 호출할 때는 새로운 메서드 생성하는 것이 가독성과 효율성을 높일 수 있다.


![](https://velog.velcdn.com/images/iissk/post/718ed907-09d1-4518-8423-7ada9ca9ecaf/image.png)

▶ base클래스인 Truck의 오버라이딩 메서드를 Porter에서 다시 재정의(오버라이드)를 할 수 있다.


![](https://velog.velcdn.com/images/iissk/post/3387abb5-6baa-40f8-9d2e-38f1f58af4ad/image.png)

▶ 2,3차로 상속되는 파생클래스에서 오버라이딩을 사용할 경우 중간 클래스들에서도 오버라이딩이 되어야 한다.



> ※섀도잉
>    : 지역변수와 매개변수가 메서드의 멤버변수를 숨겨버리는 것
>    maxSpeed(메서드 밖 변수) = maxSpeed(메서드 멤버변수); 가 가능하다.
> ![](https://velog.velcdn.com/images/iissk/post/2da6d9ec-2c19-4218-b8c7-4db27ce81f3d/image.png)
> 	1. 지역변수 : class에서 사용하는 변수
> 	2. 멤버변수 : 메서드에서 사용하는 변수
> 	3. 매개변수 : 인자값