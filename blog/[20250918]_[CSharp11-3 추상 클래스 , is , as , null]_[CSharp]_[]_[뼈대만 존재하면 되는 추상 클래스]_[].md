# Ⅲ. 추상 클래스 , is , as , null

### 1. 추상클래스
---
**※추상클래스:** 세부적인 구현은 자식에서 구현하도록 위임하고 본인은 최소한의 기능만 가지는 클래스
- 반드시 파생클래스에 오버라이딩이 되어야 한다.(재정의를 강제함)
- virtual이 아닌 abstract를 사용해서 오버라이딩 진행
- 실체화 될 수 없고, 이를 상속받은 자식들만 실체화가 가능
  ![](https://velog.velcdn.com/images/iissk/post/9d696a9e-d9f6-4a6c-87ec-365004336cfd/image.png)

![](https://velog.velcdn.com/images/iissk/post/20411ced-cf60-4e38-a9d6-e1babefc41d0/image.png)

  ▶ 자동차의 뼈대만 만들어놓는 것과 같음(독립적으로 사용불가)


![](https://velog.velcdn.com/images/iissk/post/41140dfe-903a-41b1-855b-49a7aeb1fbec/image.png)

▶ 파생 클래스에도 추상클래스의 메서드가 동일하게 정의 되어야 한다.

![](https://velog.velcdn.com/images/iissk/post/76f07440-9da7-4683-9d93-ec243d409c9a/image.png)

▶ 오버라이딩하기 위해서 abstract를 사용하며 파생 클래스에 오버라이딩이 되면서 에러가 해결된다.

![](https://velog.velcdn.com/images/iissk/post/30414ada-2e28-46bd-90c8-e9154983838e/image.png)



### 2. is 와 as 와 null조건부 연산자
---
###### ※is키워드: 좌우항의 "형식"을 비교해서 같은 형식이면 'true' , 다른 형식이면 'false'를 출력력
- 본질의 형식이 우항과 같은지?
- 좌항 객체에 우항이 담겨도 문제가 없는지?

![](https://velog.velcdn.com/images/iissk/post/aa56f476-7e66-41fb-9133-2d06681a68e4/image.png)



###### ※as키워드: 좌항을 우항의 "형식"으로 바꾼다.
![](https://velog.velcdn.com/images/iissk/post/c3b58974-2313-405f-88e3-d3ee514347cc/image.png)

▶ as키워드를 사용해서 참조타입의 형변환시에 안전한 코딩이 가능하다.


###### ※null조건부 연산자: 앞에 null을 입력으로 받게 되면 이후 호출을 모두 무시한다.
- 연산자로는 '?'를 사용한다.
- 주로 null일 가능성이 있는 코드에 '?'를 적으며 복잡한 계산을 빠르게 생략 및 터지는 일을 방지한다.

![](https://velog.velcdn.com/images/iissk/post/e98239a4-bf4e-43c1-9371-125dd3d2cd22/image.png)

