# Ⅱ. class(프로퍼티, 메서드)


### 1. class 기본형식
#### 기본형식
![](https://velog.velcdn.com/images/iissk/post/e1c4bbb9-ba2c-43dd-9d9d-acf0e1fbaf28/image.png)

▶ 클래스는 메인 외부에 생성할 수 있지만

![](https://velog.velcdn.com/images/iissk/post/26b39ab2-c60e-4248-91fc-1034279227a0/image.png)

![](https://velog.velcdn.com/images/iissk/post/d1513ad7-d615-4fbb-9001-05e9b0b2f348/image.png)

▶ cs파일을 추가해서 class 전용 공간을 만들어서 작성한다.

![](https://velog.velcdn.com/images/iissk/post/8f42e621-c84a-46a6-9cec-3d441d4f44ce/image.png)
▶ class의 필드를 추가함으로 객체의 기본값(속성)을 지정한다.
- enum을 class 안에 넣을 경우, class 내부에서만 사용 가능한 자료형이 된다.
- enum을 class 밖에 넣을 경우, 다른 class(Main포함)에서도 사용 가능한 자료형이 된다.



### 2. 프로퍼티
**※프로퍼티:** private인 값을 외부에서 출력(get) , 변경(set)을 할 수 있도록 하는 기능
- ex) 마우스의 클릭버튼, 휠, 센서 등의 일종의 개체
- 외부에서는 *(인스턴스명).(프로퍼티명)* 으로 실행한다.
- 필드(매개변수)의 조건, 범위를 제한할 수 있다.

![](https://velog.velcdn.com/images/iissk/post/bbf18bbb-5f70-4a1a-bb7a-2a92ce0c4166/image.png)

**※자동구현 프로퍼티:** 내부적으로 관리하는 변수를 백킹 필드에 자동으로 만들어준다.

![](https://velog.velcdn.com/images/iissk/post/bd695501-b04c-4c39-ba84-28467e0a68a4/image.png)

**※'=>'를 이용해서 간단하게 표현 할 수도 있다.**
![](https://velog.velcdn.com/images/iissk/post/88fc293b-6fc5-4e55-80af-63f2d7a59aa8/image.png)


### 3. 메서드
---
**※메서드:** class 내의 객체에 기능을 부여하는 함수
- ex) 마우스 클릭시 선택, 더블클릭 창이동 등의 기능
- 외부에서 *(인스턴스명).(메서드명)* 으로 실행한다.

![](https://velog.velcdn.com/images/iissk/post/b320fce0-4451-4109-a8b5-33ebe128b525/image.png)
▶ petPank가 출력될 때 폰트색깔을 교체하는 메서드

### 4. partial
---
**※partial:** class를 분할해서 사용할 수 있는 것

![](https://velog.velcdn.com/images/iissk/post/f0f7fd2a-eae8-4a4e-b5c0-1759053b659e/image.png)

![](https://velog.velcdn.com/images/iissk/post/a2ed1a2e-a878-4649-a7aa-21494a32be6f/image.png)
▶ 서로 다른 cs파일이지만 같은 클래스를 공유해서 level 변수를 사용할 수 있게 된다.
- 서로 같은 클래스로 인식하기 때문에 프로퍼티 사용하지 않아도 된다.



>## <p style="color:green"> 🤔 마무리</p>
> class는 객체지향의 기본이 되는 요소이다.
<br>
객체를 생성할 때, 객체의 **각 기능에 따라 class를 만들어서 각 class를 서로 연결함**으로 객체를 만든다.
<br>
이 때 우리는 Solid원칙과 같이 class가 어느정도의 독립성을 가지고 있어야 한다는 것을 기억해야 한다.
<br>
비슷한 기능은 묶되, 그렇지 않은 내용은 다른 class로 분리한다는 것을 항상 염두하며 코드를 작성하자!
<br> <p style="color:blue">
나는 처음엔 진짜 난해하고 어떻게 동작하는지도 제대로 감이 안 왔는데, 
<br>
확실히 반복해서 써보니까 느낌이 오기 시작하고 지금은 class가 있어서 코드를 읽고 쓰는 게 굉장히 편하다는 것을 느꼈다.
<br>
이를 가장 절실히 느낀 건 다른 사람의 코드를 볼 때였는데
<br>
클래스로 구분이 되어 있어서 그나마 하나하나 데이터와 메서드들을 따라가다보니 코드를 해석할 수 있었지만,
<br>
만약 클래스로 분리가 안 되었다면....해석하는 시간은 2,3배로 더 늘어나지 않았을까 생각했던 적이 있다.
</p>