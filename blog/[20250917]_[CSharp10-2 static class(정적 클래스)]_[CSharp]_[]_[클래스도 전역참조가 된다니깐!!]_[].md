# Ⅱ. static class(정적 클래스)

### 1. static class
---
###### ※static class 는 초기화(new)가 1번만 진행을 하게 된다.
###### ※static class는 객체가 1개라도 만들어져야만 쓸 수 있다.
- static 필드와 달리 객체를 요구한다.
- static 프로퍼티를 사용해서 객체 없이도 static 사용이 가능
###### ※인스턴스 생성 불가능, 모든 필드는 const 혹은 static이여야 한다.
- static만의 공간이 만들어져서 객체가 필요하지 않지만 일반 변수들은 객체를 요구하기 때문에 사용이 불가능
###### ※정적 클래스는 메모리에 항상 존재하고, 프로그램 종료까지 사라지지 않는다.

![](https://velog.velcdn.com/images/iissk/post/b0613a12-f4fb-4a69-88a9-ad2881ef6df4/image.png)

![](https://velog.velcdn.com/images/iissk/post/162f08da-48a9-490f-9a80-30ceb9f6c322/image.png)
▶ Reward 초기화값이 static으로 개별 생성자들도 공유를 하는 값이기 때문에 초기화는 1번이면 충분하다.


![](https://velog.velcdn.com/images/iissk/post/87cc5e8b-7ce0-4f5b-855a-39f6eb2a568d/image.png)
▶ static 필드와는 달리 static class는 프로퍼티 후에 접근을 할 수 있다.
▶ 외부에서 임의로 static값을 직접 접근하면 수정의 위험성이 있어서 프로퍼티로 보호한다.


![](https://velog.velcdn.com/images/iissk/post/6c728eab-0450-4974-b4fc-729a9c233d3d/image.png)
▶ const(상수) , static 값만을 정적 클래스 내부에서 사용이 가능하다.