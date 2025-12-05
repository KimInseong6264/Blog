# Ⅱ. Stack과 Queue

**※Stack:** 자료를 적층구조로 쌓는 모양
- 뒤로 가기처럼 차곡차곡 시행되는 것
- 가장 먼저 들어간 자료가 가장 늦게 나오는 구조
  (선입후출 , 후입선출 , First in Last Out , Last in First Out ) => LIFO
- ex) 웹브라우저 뒤로가기 , 체스: 턴 무르기 , ctrl + z, UI팝업, 히스토리

### 2. stack 메서드
---

**Push** stack에 차곡차곡 값을 집어넣는다.
![](https://velog.velcdn.com/images/iissk/post/4b1cffaf-c324-4c13-a0e1-7bb44d4f3b67/image.png)



**Pop** stack의 가장 위의 요소를 반환하고 stack에서 없앰
![](https://velog.velcdn.com/images/iissk/post/729d5cde-2a4e-49cc-afa8-989f1d34b4a6/image.png)



**Peek** stack의 가장 위의 요소를 보기만 함(읽기전용)
![](https://velog.velcdn.com/images/iissk/post/12d427da-d72f-4205-8f6b-4797829ad80a/image.png)



**Any** stack의 요소가 1개라도 존재하면 true를 반환(Pop을 할 때, 반복문 조건으로 사용)
![](https://velog.velcdn.com/images/iissk/post/bc7c8269-0d52-4435-8302-18431962253d/image.png)




### 3. Queue
---
**※Queue:** 자료를 줄세워서 1번이 먼저 나오는 것
- Stack과 반대로 먼저 입력된 자료가 먼저 출력되는 구조
- 선입선출
- ex) 유닛 생산, 대기열, 매칭, RTS 건물 생산, 예약시스템, 제작, 턴제, 메크로



### 4. Queue 메서드
---
**Enqueue** stack에 차곡차곡 값을 집어넣는다.
![](https://velog.velcdn.com/images/iissk/post/abda3d71-82fa-42bc-8c2d-9de9f956f1b6/image.png)



**Dequeue** 가장 먼저 들어가 있던 값을 꺼내서 반환한다.
![](https://velog.velcdn.com/images/iissk/post/d8b3768d-c063-4fa5-987a-5c25cade93d5/image.png)



**Peek** 가장 먼저 들어가 있던 값을 읽기만 한다.(꺼내지 않음)
![](https://velog.velcdn.com/images/iissk/post/fb3ce8be-7cc5-4c6f-8026-c8daf01c6b7d/image.png)

