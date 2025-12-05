# Ⅰ. Generic
### 1. 자료형을 치환하는 Generic
---
**※Generic:** 하나의 클래스 내에서 다양한 형태의 자료형을 치환해서 적용할 수 있는 방식
- < T >를 사용해서 T를 치환시켜서 임의로 자료형을 입력할 수 있다.(T를 사용하는 게 국룰)
- Cup< > 가 하나의 자료형으로 사용된다.
- < T >에 너무 아무거나 담을 수가 있다.(단점)
   ㄴ where T :  을 사용해서 특정 T만을 넣을 수 있다.
- new() 할당도 허용(where)을 해주어야 사용이 가능하다.

![](https://velog.velcdn.com/images/iissk/post/55683578-3269-4881-b264-53f1dbb30cef/image.png)

![](https://velog.velcdn.com/images/iissk/post/abbef874-b235-4d7e-8a6a-9c552f74af46/image.png)

▶ generic을 지정하는 방식

![](https://velog.velcdn.com/images/iissk/post/a5d6c786-be51-4be4-8362-9a4cf4699f4b/image.png)

▶ where T : class는 클래스만 담도록 하는 것


![](https://velog.velcdn.com/images/iissk/post/cd509866-9b7e-4669-841d-4d631f6c3b00/image.png)

▶ where T : struct는 클래스만 담도록 하는 것



![](https://velog.velcdn.com/images/iissk/post/e48a0648-7784-4e61-8c5a-5795baf6d4c8/image.png)

▶ 두 개 이상을 치환값으로 쓸 수 있다.

![](https://velog.velcdn.com/images/iissk/post/5ff886df-9d6b-45d3-a97c-a06418201ccc/image.png)

▶ new도 직접 where로 허용을 해주어야 한다.


![](https://velog.velcdn.com/images/iissk/post/d1797b64-83b2-43d2-8355-0669e2e4ee9e/image.png)

▶ 특정 클래스만을 치환받을 수도 있다.


![](https://velog.velcdn.com/images/iissk/post/38aab678-6b86-4b77-9984-4e1cd9a60c7d/image.png)

▶ Cup이 아닌 Cup< > 가 하나의 자료형이 된 것
