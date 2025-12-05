# Ⅰ. 상속

### 1. 상속의 개념
---
**※상속:** 클래스를 만드는데, 중복된 내용을 하나의 클래스로 지정하여 종속된 클래스들을 만들어내는 방식
ex) 필기구 , 자동차 공통조건
- **base클래스(부모클래스):** 타 클래스의 근간이 되는 클래스
- **파생클래스(자식클래스):** base클래스에 종속되어 객체, 메서드등을 공유하는 클래스

![](https://velog.velcdn.com/images/iissk/post/12c52685-04a9-4e66-b2c1-cf739bbb3bc6/image.png)

![](https://velog.velcdn.com/images/iissk/post/1be45c72-1a76-4689-9f31-9fa0f97e9180/image.png)

▶ : Car 를 이용해서 클래스를 종속시킨다.


![](https://velog.velcdn.com/images/iissk/post/48e87c34-41e7-46f7-8a82-01a6396ab849/image.png)

▶ 부모클래스가 private 되어 있어서 보호수준 에러가 발생

![](https://velog.velcdn.com/images/iissk/post/f63fed4b-dc5b-4f96-83cc-718ff292d3b4/image.png)

▶ **protected :** 상속 클래스 내에서 보호수준을 열어주는 기능
▶ public이 아니므로 Main에서는 접근 할 수 없다.


### 2. 상속클래스의 생성자
---

![](https://velog.velcdn.com/images/iissk/post/ebce44b0-b355-4e18-87f7-2d0b8c806bc5/image.png)

▶ Sedan 생성자만으로도 Car(부모클래스)의 생성자도 함께 출력된다.
- Car(부모클래스)의 생성자가 먼저 출력된다.


![](https://velog.velcdn.com/images/iissk/post/9840488b-0e66-4fb9-b3de-a22085702bbb/image.png)

▶ : base(인자값)를 통해 부모클래스의 임의 생성자를 선택해서 Sedan 클래스와 함께 호출할 수 있다.
- Car의 생성자만 호출하고 싶을 경우엔 new Car로 불러오면 된다.

##### ※sealed class
![](https://velog.velcdn.com/images/iissk/post/082cbc1b-b129-486f-815e-ee4c0f511512/image.png)

▶ 부모클래스 앞에 sealed를 입력해서 상속이 불가능한 클래스를 만들 수 있다.
