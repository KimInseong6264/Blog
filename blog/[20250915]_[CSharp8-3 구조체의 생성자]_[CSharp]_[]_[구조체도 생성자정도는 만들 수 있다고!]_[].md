# Ⅲ. 구조체의 생성자

### 1. 자료형의 초기값
---
**※값타입 자료형에도 new를 사용할 수 있다.**
- new를 통해 초기값을 만들어 변수에 넣게 된다.

![](https://velog.velcdn.com/images/iissk/post/85a8ea42-de36-4bec-a385-41319abe61ae/image.png)

![](https://velog.velcdn.com/images/iissk/post/6f4ff106-9c2a-4d0d-9558-a8bb37de814b/image.png)

▶ new int(); 단독으로 초기값을 상징한다.

![](https://velog.velcdn.com/images/iissk/post/aa11e617-9589-4e5d-a144-7fbee8516ef4/image.png)

1) new Vector2(); 를 통해 임시로 모든 속 내용이 0으로 초기화 된 임시 구조체를 '잠시' 만든다.
2) 옆의 playerPos에 복사가 된다.
3) new Vector2(); 는 playerPos에 값이 입력되면 곧바로 사라진다.

### 2. struct의 생성자
---
![](https://velog.velcdn.com/images/iissk/post/7fe047be-4f39-4a11-bb6d-4231487c558e/image.png)

▶ 구조체도 생성자를 만들 수 있다.
- 생성자에 반드시 인자값이 주어져야 한다.
- 구조체 내부의 멤버변수에 모두 값이 할당 되어야 한다.

![](https://velog.velcdn.com/images/iissk/post/78692fbc-9f39-41bf-9d7b-b9fcf1031f93/image.png)

▶ 구조체 내부에 생성자가 없을 경우
- new Vector2(); 자체로 초기값 할당이 가능하다.

> **struct의 생성자를 통해 임의의 초기값을 할당 가능하다.**


### 3. new의 활용
---
##### 1. 배열에 new 사용
![](https://velog.velcdn.com/images/iissk/post/56bb3f72-b5ba-4d67-891b-5b996a6e0d06/image.png)

1. Heap 영역에 공간을 빌린다.
2. 어디에 저장되었는지 주소값을 좌항에 넣어라.

##### 2. 구조체에 new 사용
![](https://velog.velcdn.com/images/iissk/post/23c0b91c-6520-48e5-8f45-30895292f8ca/image.png)

1. 해당하는 생성자를 불러온다.
2. 임시 구조체를 만들어라.
3. 좌항에 넣어라.

##### 3. 클래스에서 new 사용
![](https://velog.velcdn.com/images/iissk/post/97cc3a38-61c2-469d-82d9-7d8cd59932ef/image.png)

1) 해당하는 생성자 불러온다.
2) Heap 영역에 공간도 빌린다. 
3) 주소를 좌항에 넣어라.

### 4. 인자값에 new할당
---
## ※중요※

![](https://velog.velcdn.com/images/iissk/post/42f2e271-383d-445d-99c0-dfa176621589/image.png)

![](https://velog.velcdn.com/images/iissk/post/0c7db227-35c9-42e8-912d-2dd49dbc0da8/image.png)
1) Vector2에서 Vector2(4 , 4)에 해당하는 생성자 할당
2) Player 생성자에 Vector2(4 , 4)를 인자값으로 입력
3) Player 생성자의 공간 주소값을 player에 할당



