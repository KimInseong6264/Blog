# Ⅱ. 오버로딩

### 1. 오버로딩
---
**※오버로딩:** 같은 이름의 메서드 혹은 생성자들을 매개변수 차이로 구분해서 정의하는 것
- 인자값이 서로 다른 생성자는 input 자료형에 따라 다르게 작동
- 인자값이 동일한 자료형을 요구할 경우엔 "에러"가 발생
- 인자값이 2개 이상으로 설정시에도 오버로딩 가능

>**※메서드 시그니처:** 메서드이름 + 매개변수 정보
> - 메서드의 구분은 이름이 아닌 시그니처로 구분한다.

![](https://velog.velcdn.com/images/iissk/post/c5b4ce02-3470-4725-85fb-644c50e60e28/image.png)
▶ 인자값의 자료형이 겹치지 않게 해야 한다.


![](https://velog.velcdn.com/images/iissk/post/f175a1f3-d947-4c03-b76a-61fb46e2dc4b/image.png)
▶ IDE 자체적으로 다른 생성자와 구분가능


![](https://velog.velcdn.com/images/iissk/post/b94c6d0b-19d7-4cf4-adfd-0b600c8aa9b7/image.png)
▶ 여러 오버로딩된 생성자들 중에 인자값을 어떤 것을 요구하는지 알 수 있는 인자값 보기기능


#### 메서드의 오버로딩

![](https://velog.velcdn.com/images/iissk/post/6f26c391-e4d3-4621-96d8-0f051147e343/image.png)
▶ 메서드도 생성자와 마찬가지로 오버로딩 가능
- 비슷한 기능을 하는 경우에만 메서드 이름을 동일시 해서 이용(*남발해서는 안됨*)



### 2. 디폴트 매개변수
---
**※인자값이 겹치는 경우는 디폴트 매개변수가 없는 것을 먼저 출력**
- 디폴트 매개변수를 인자값으로 주어지지 않으면 최초 지정된 값이 인자값으로 사용
- 디폴트 매개변수가 앞에 있는 것부터 사용가능
	ex) 포켓몬포획시, 별명을 짓지 않으면 기본설정된 이름으로 저장


![](https://velog.velcdn.com/images/iissk/post/b0b5c883-cdd4-466c-872c-390c00982ed6/image.png)
▶ int lvl 값만 인자값으로 받을 경우, nName 과 toPrint의 값은 주어진 값으로 임의로 입력된


![](https://velog.velcdn.com/images/iissk/post/b2fe7107-bb97-4da2-8043-eb263cf7bc1b/image.png)
▶ 순서에 따라 nName을 입력하지 않고 toPrint만 인자값으로 입력은 불가능


![](https://velog.velcdn.com/images/iissk/post/2a33cc1f-9d44-4af2-b0be-50deb2f1bcfc/image.png)
▶ 디폴트 매개변수보다 일반 생성자의 우선도가 먼저 적용된다.



