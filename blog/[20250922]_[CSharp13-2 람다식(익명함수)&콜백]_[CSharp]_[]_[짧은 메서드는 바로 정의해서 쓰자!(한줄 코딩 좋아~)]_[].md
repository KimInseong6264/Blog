# Ⅱ. 람다식(익명함수)&콜백


### 1. 람다식, 익명함수
---
**※람다식(익명함수):**  델리게이트 인자값에 자료형이 정의되어 있어서 함수명을 사용하지 않고  함수식 설정이 가능
-  가볍게 정의해서 가볍게 쓰고 버리는 방식

![](https://velog.velcdn.com/images/iissk/post/da8c2362-09d9-482c-8e37-7c13bfd6021b/image.png)

▶ delegate 안에 가벼운 연산의 함수를 1줄로 지정해서 사용(가볍게 사용 용이)

![](https://velog.velcdn.com/images/iissk/post/d8fd672c-82dc-4919-b37a-bc59d35e8268/image.png)

▶ 임시 사용 목적으로 중간에 연산을 바꿔서 delegate에 넣어서 사용 가능하다.



### 2. 콜백
---


![](https://velog.velcdn.com/images/iissk/post/a78e88f9-4186-41a1-ab2b-27b8f0025cb7/image.png)

![](https://velog.velcdn.com/images/iissk/post/b3ef513a-c1bc-438e-b2b5-b6a6ab655062/image.png)

▶ 웨이팅 예시

**※콜백:** 특정 작업이 완료된 후 호출되는 메서드
- 우리가 원하는 내용을 다른 함수에게 실행시켜 달라고 요청하여 실행시키는 일
  (1번 명령으로 2번의 메서드 실행해줘)
- 메서드 안에 delegate가 들어가서 추가 메서드 실행이 되는 것
  (이 때, 인자값으로 메서드가 들어가야 하는데 그 때 자료형이 delegate인 것)

> **콜백 예시**
> 1. 이벤트 처리, 유니티에서 버튼 클릭이 일어나면 무엇을 한다.
> 2. 알고리즘 구현, 정렬, 검색 시 동작을 유연하게 갈아끼기 위해 사용
> 3. UI 업데이트: 백그라운드 모든 작업 완료 시 화면 갱신 등등
>
>나중에 네트워크 같은 비동기 작업이 있을 때 콜백이 많이 도배되어 있음


> ##### 전제 코드
> ![](https://velog.velcdn.com/images/iissk/post/75ccf379-ecd3-4a67-9259-da41ddd61f45/image.png)
> ![](https://velog.velcdn.com/images/iissk/post/52d64077-70ca-4e24-9409-04674c0b056e/image.png)

![](https://velog.velcdn.com/images/iissk/post/df0b69ca-0954-4927-9b89-3e953917347d/image.png)

▶ 아래에서 Dowork의 인자값으로 AfterWork를 입력시 Dowrk실행하고 callbackMethod(인자값: AfterWork)를 실행한다.

![](https://velog.velcdn.com/images/iissk/post/6f696f14-d945-4c4c-8940-5898b8e8a18d/image.png)

▶ 콜백은 인자값에 메서드를 넣어서 이중으로 메서드가 실행되게 한다.
