# Ⅱ. 디버거

### 1. 디버거
---
※ 프로그램 수행시 중첩 반복, 무한반복등의 문제가 발생하는 버그시에 디버그하기에 용이하도록 IDE 내에 내장되어 있는 장치

- F11을 활용하여 디버거 동작
- 컴퓨터가 어떻게 코딩을 처리하는지 순서대로 확인이 가능
  (F11을 추가적으로 입력하여 다음 순서 확인)

![](https://velog.velcdn.com/images/iissk/post/4823ebd8-b0e2-4f73-9602-e3877051f501/image.png)
▶ F11을 누르면서 다음 동작을 확인 가능

![](https://velog.velcdn.com/images/iissk/post/916a711d-2675-4450-8611-d08928e73efb/image.png)
▶ F11을 눌렀을 때 선택된 줄(노란색)을 수행하고 다음 줄로 넘어감

![](https://velog.velcdn.com/images/iissk/post/4cfb22db-fe0e-4cbc-8835-e562dbefd3c2/image.png)
▶ F11을 추가적으로 입력하여 최종적인 출력까지 동작확인

> 필요한 줄을 바로 찾아서 디버깅
- F9를 입력하여 특정 줄에서부터의 디버그확인 가능(해당 줄 F9 추가 입력시 선택해제)

![](https://velog.velcdn.com/images/iissk/post/33cf8aba-ffef-423a-9fe8-664db812cfce/image.png)
▶ F9를 입력하여 Console.WriteLine(increasingNum); 부터 디버그 확인을 할 수 있음

### 2. 실수의 부정확함
---
※ 정수형과 달리 실수형은 많은 범위의 숫자를 나타내기 위해 복잡한 수식을 사용한다. 
float는 4byte인데, 작은 크기에 정보를 담는 과정에서 특이한 표현방법을 사용한다.

![](https://velog.velcdn.com/images/iissk/post/182626ff-09c4-46be-9f72-d75ea6f42d17/image.png)
▶ 부동소수점 표현법: 실수형이 표현 범위를 늘이기 위해 정확도(오차발생)를 일부 포기한 형태

![](https://velog.velcdn.com/images/iissk/post/4d6049d1-97d7-4ba6-ab00-74f3ef0aa88b/image.png)
▶ 실제 계산시 2.1 X 6.2 = 13.02 로 계산되어야 함


![](https://velog.velcdn.com/images/iissk/post/d665fbf6-90ce-4a0a-a889-bedf0e0631d9/image.png)
▶ m은 출력시 13.02로 계산된 것처럼 보이나 디버그한 값을 보면 13.0199986으로 근사값이 나온다는 것을 알 수 있다.

![](https://velog.velcdn.com/images/iissk/post/5acdeda0-8cf1-491b-a25a-5d34185e9b51/image.png)
▶ 결과적으로 m≠13.02 이므로 if문의 내용을 수행하게 된다.