# Ⅲ. event, 캡쳐와 클로저

### 1. event, 특정 상황에서의 delegate
---
**※event는  특수한 제약조건이 추가된 delegate이다. 특정 상황이 발생했을 때 실행할 동작을 정의한다.**
- event는 어떤 행위가 발생하는 것(입력) / event Handler는 이벤트 발생시 실행되는 것(출력)
- 외부: 메서드 등록과 제거는 허용 , 인보크는 막아주는 역할
  (외부에서 임의로 함수조작 방지)
- 내부: 액션 델리게이트를 정의한 클래스 내에서만 .Invoke가 가능하다.

> ##### 전제코드
>![](https://velog.velcdn.com/images/iissk/post/b093c780-659f-45d7-9b64-be76a9504085/image.png)
>![](https://velog.velcdn.com/images/iissk/post/6cad0e50-5a2d-4f9b-a39c-2acc62b24e5a/image.png)


![](https://velog.velcdn.com/images/iissk/post/4a63c097-21ef-462b-af60-09e085a9c2ab/image.png)
▶ 원하는 버튼 기능만 넣고 싶은데, 외부에서 임의로 조작할 위험성이 있다.

![](https://velog.velcdn.com/images/iissk/post/6d80bc0a-f5c2-44ca-977a-4d32ff5c9f31/image.png)
▶ event 를 이용해서 클래스 외부에서의 접근은 차단하고 메서드의 등록과 해제는 가능하게 제약을 걸 수가 있게 된다.


**※.Invoke:** delegate함수/메서드를 실행한다는 명시적인 의미(일반함수/메서드 실행과 차이를 두는 표현)

#### delegate에서 사용하는 private 기능이라고 생각하면 쉽다.


### 델리게이트 캡쳐
---
###### 람다식이나, 익명함수에서 외부 범위에서 선언된 변수(지역변수 , 필드)를 사용하는 것


```
int val = 42;

Func<int> getVal;

getVal = () => val;  //
```

- 캡쳐가 일어나게 되면 람다식 내의 변수들은 다 사라져야 하지만, 사라지지 않고 생명주기가 길어지게 된다.


### 클로저
---
###### 캠쳐된 변수와 해당 변수를 사용하는 함수를 묶어서 저장하는 방식, 클로저 덕분에 함수가 외부 범위의 변수를 "생명주기와 관계 없이 계속 사용할 수 있게" 만듦

- 원래 사라져야 할 변수가 살아남아있는 것을 의미
- 의도적이지 않았다면 버그를 유발한다

위의 코드에서 getVal을 [클로저 객체]라고 한다.

```
Func<int> Closure()
{
    int counter = 0;
    return () => ++ counter;  // counter가 람다식에서 저장이 되어지고 있음
}
```