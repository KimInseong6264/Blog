# Ⅰ. delegate

### 1. 함수를 담는 자료형 delegate
---
**※Delegate:** 특별히 메서드/함수를 담는 자료형
- 함수와 메서드를 담는 변수를 만들 수 있게 된다.
- delegate 사용을 하고 마지막에 null처리를 해줘야 재사용시에 유용하다.

![](https://velog.velcdn.com/images/iissk/post/6b6003a6-8fe8-403a-834a-404820e10a8d/image.png)

▶ 대체로 class 밖에서 정의하며, 함수를 만들 때처럼 선언하면 된다.


![](https://velog.velcdn.com/images/iissk/post/ca5f5315-54c8-48dd-8d68-ebdc33753cc1/image.png)

![](https://velog.velcdn.com/images/iissk/post/9ece56d9-35ef-49a7-8515-89e77a6ad11a/image.png)

▶ 클래스 객체를 만들고 객체에 함수를 담는다.(괄호는 제외)


![](https://velog.velcdn.com/images/iissk/post/694319ba-44c2-4e79-abce-8244d7d4f2c0/image.png)

▶ () 를 쓸 경우 함수의 리턴값을 담는다는 의미이므로 함수식이 delegate에 담길 수가 없다.
![](https://velog.velcdn.com/images/iissk/post/dc6b48c8-462c-4533-88b8-ed0778da037a/image.png)

▶ 함수출력은 delegate 객체에 () 를 붙여서 출력(인자값이 없는 경우)


![](https://velog.velcdn.com/images/iissk/post/1aae8198-261e-40f9-82b3-5d59cbddd845/image.png)

▶ delegate는 객체를 요구한다.


![](https://velog.velcdn.com/images/iissk/post/8e8edaf4-75c3-409f-8f02-fdb89f553635/image.png)

▶ 인자값을 요구하는 함수의 경우, 오버로딩할 때와 같이 인자값의 수와 자료형이 일치하도록 입력해야 한다.


### 2. Delegate Chain
---
**※하나의 delegate에 여러 함수/메서드를 등록해서 한 번에 실행하는 것**
- '+=' 는 함수를 등록 , '-=' 는 등록취소한다는 의미
- 등록 안 되어 있는 거는 등록취소해도 터지지 않는다.(C#내에서 안전장치)
- 위험성: '=' 대입연산자로 메서드를 입력시 이전의 체인들을 모두 없애고 덮어씌워버린다.
  (event로 대입연산자, Invoke 사용을 막아야 하는 이유)
  델리게이트 체인에 비정적 객체의 메서드를 추가하면, 메모리에서 해제되지 않는다.

> ##### 전제 코드
> ![](https://velog.velcdn.com/images/iissk/post/b811b5e9-fcb0-43e7-a77a-397defb933b8/image.png)


![](https://velog.velcdn.com/images/iissk/post/3485123c-adf6-4488-9251-12228b6dcfe2/image.png)

▶ 왼쪽의 코드를 오른쪽의 deleagate를 활용해서 간략화가 가능하다.


![](https://velog.velcdn.com/images/iissk/post/8a119161-afe7-47c5-a0bb-2ef576e6ec1e/image.png)

▶ delegate에 null의 함수연산이 들어가면 터져버린다.

![](https://velog.velcdn.com/images/iissk/post/d5a68be6-ea21-4923-96a6-c4d6959ac720/image.png)

▶ ?.Invoke 를 활용해서 null을 함수식 들어가는 것을 방지할 수 있다.


### 3. Action&Func
---
**※Action:** C#에서 정의되어 있는 return 반환하지 않는 void형 델리게이트

- ```Action<T>``` 대리자: T형의 매개변수가 하나이고 값을 반환하지 않는 메서드 캡슐화

**※Func:** C#에서 정의되어 있는 return 반환하는 자료형 델리게이트
- 델리게이트의 인자값과 자료형만 다를 뿐 속 내용물은 똑같기 때문에 C#에서 임의로 지정을 해준 것

- ```Func<T, TResult>``` 대리자: T형의 매개변수가 하나이고, TResult 매개변수에 지정된 형식 값을 반환하는 메서드 캡슐화


![](https://velog.velcdn.com/images/iissk/post/69a091d0-fad5-4e17-800f-44a71dde37ef/image.png)

▶ 클래스 외부에 delegate 생성 없이 Action을 사용해서 delegate 생성



![](https://velog.velcdn.com/images/iissk/post/0169b624-474f-408a-8274-b9adb848b13c/image.png)

▶ 클래스 외부에 delegate 생성 없이 Func<>를 사용해서 delegate 생성
