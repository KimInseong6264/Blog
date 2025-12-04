# Ⅲ. static 메서드(정적 메서드)

### 1. static 메서드
---
###### ※static 메서드에는 비정적 필드값은 사용이 불가능하다.
- 별도의 객체를 요구하는 값들이기 때문에 정적 메서드 내부에서 사용이 안된다.(static 클래스와 비슷한 원리)
###### ※메서드 내부에서 정의한 임시 변수들은 static이 아니더라도 사용이 가능하다.
- 메서드 벗어날 경우 사라지기 때문

![](https://velog.velcdn.com/images/iissk/post/5a3a7c23-4e3c-4e84-a5b9-b3373d2ae7d1/image.png)
▶ 외부에 정의된 비정적 필드(nonStaticNum)는 정적 메서드 내부에서는 사용이 불가능하다.


![](https://velog.velcdn.com/images/iissk/post/624ae09e-f140-4f7f-b190-4de3cf5f86af/image.png)
▶ 임시변수는 메서드 내에서 사용이 가능하다.





