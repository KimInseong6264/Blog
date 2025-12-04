# Ⅰ. static 필드(매개변수)

### 1. static 필드(매개변수)
---
**※static :** 프로그램 실행시, static 메모리 공간을 미리 할당을 해서 메모리를 적재시킨다.
- 클래스의 필드들이 동일한 값(정적필드)을 공유하는 공유 필드로 만들 수 있다.
- 똑같은 설계도(class) 내에서 같은 값을 공유한다.
ex) 게임 속 데스카운트 , 메이플 속 유니온 , 계정 속 공유화폐
- static은 static공간(정적공간)을 새롭게 만들어낸다.
- static은 인스턴스에 종속된 것x 즉, class를 통해서 불러올 수 있다.
![](https://velog.velcdn.com/images/iissk/post/efd52ef6-73a6-4b66-9af4-8be0d7364b75/image.png)


>**static의 장점**
> 1. 편하게 꺼내 쓸 수 있다.(ex. Random)
> 2. 객체를 새로 만들지 않고도 값을 도출할 수 있다.(ex. cw)

![](https://velog.velcdn.com/images/iissk/post/9036dc73-ea4d-4e56-a752-fe7d6933a1fc/image.png)
▶ static은 class, Heap과 무관한 공간이 새롭게 만들어짐


![](https://velog.velcdn.com/images/iissk/post/6465f0f6-823d-41b0-92da-ae58ab7f0533/image.png)

![](https://velog.velcdn.com/images/iissk/post/5da8669d-3106-4dc7-a776-9ca3db4a2b45/image.png)
▶ Enemy1,2,3의 모든 값이 static createConut를 공유함


![](https://velog.velcdn.com/images/iissk/post/12a6016d-16b4-4961-8999-70f53b006f03/image.png)
▶ 서로 다른 인스턴스를 생성자로 실행해도 createConut의 값이 static이기 때문에 함께 증가한다.


![](https://velog.velcdn.com/images/iissk/post/feb8268e-bb04-4bd5-8adf-bf2fb408bc6b/image.png)
▶ class에 자명한 값이므로 인스턴스 생성 없이 단독으로 호출 할 수 있다.
