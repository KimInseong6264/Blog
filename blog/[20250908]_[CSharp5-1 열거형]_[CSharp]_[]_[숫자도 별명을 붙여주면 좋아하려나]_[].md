# Ⅰ. 열거형


### 1. 열거형이란?
---
**※enum :** switch문 등에서 여러 케이스들이 헷갈리지 않도록 각 케이스별 명칭을 지정해주는 것
- 사용자가 직접 자료형을 만드는 것
- 내가 만든 자료형의 값만을 변수로 지정해서 넣을 수 있음
- 쉽게 말해, 숫자에 별명을 붙여주는 C#의 키셋팅 기능

![](https://velog.velcdn.com/images/iissk/post/378c3849-5a69-4018-a12a-6e2c41729377/image.png)
▶ class 밖에 지정을 해야 함(Main에 지정X)


![](https://velog.velcdn.com/images/iissk/post/ea537716-5fb3-4e24-9fc3-3e03d6d66e7a/image.png)
▶ 변수 지정하듯, 변수명 선언을 하고 변수값에는 해당 자료형의 어떤 값을 지정해주면 됨
```
선언 : (열거형 이름) (변수명);
```
```
사용 : (변수명) = (열거형 이름).(열거형 내의 값);
```

### 2. 열거형 적용
---
![](https://velog.velcdn.com/images/iissk/post/2e8b7781-c390-456d-9f28-25ac00316c89/image.png)
▶ Enum.TryParse를 지정하면 ReadLine도 사용이 가능해짐<br>
▶ switch문에 각 케이스들에도 열거형을 그대로 입력해서 사용


![](https://velog.velcdn.com/images/iissk/post/eb172605-2ef0-41b3-a382-9dbdad069532/image.png)
▶ 열거형의 특정값에 숫자를 지정해주면 나머지 값들도 **자동적으로 숫자가 지정**됨


### 3. 열거형과 형변환
---
![](https://velog.velcdn.com/images/iissk/post/830b5b49-2a0c-47c2-90d0-8dfd20b479ce/image.png)
▶ 숫자로도 열거형을 지정할 수 있음 
But. 형변환을 해야 가능함(프로그램 내에 다른 열거형 다수 존재)


![](https://velog.velcdn.com/images/iissk/post/6cbdfe02-5d2f-4334-9ac0-d478f120436b/image.png)
▶ 숫자로 열거형을 출력할 경우, 열거형 안의 값으로 지정 되어 있는지 판별을 해야 함
 ㄴ Enum.IsDefined( typeof(변수명 이름), 숫자) 를 사용해야 함


### 4. 열거형 인자값 
---
![](https://velog.velcdn.com/images/iissk/post/b2a7cc5a-e754-4d31-bf1c-8e47ca4ff642/image.png)

![](https://velog.velcdn.com/images/iissk/post/e25eb927-6a5a-4707-bcaa-fc2062dea9cc/image.png)
▶ 백그라운드 컬러, 폰트 컬러 변경법


![](https://velog.velcdn.com/images/iissk/post/dd687053-f7bb-4124-bd3e-e64a5ebbe985/image.png)

![](https://velog.velcdn.com/images/iissk/post/456960fb-9c18-4a82-8809-13d87f8d4fcb/image.png)
▶ 폰트 색 변경을 함수로 지정할 수 있음, 인자값으로 열거형 사용 가능
(ConsoleColor는 프로그램 내 지정된 열거형)


>## <p style="color:green"> 🤔 마무리</p>
> 열거형은 숫자에 별명을 붙여주는 것이다.
<br> 처음 이 개념을 배울 때는 이후에 나올 구조체와 함께 학습 할 때 뭐가 뭔지 몰라 헷갈리기에 딱 좋은 내용이었다.
<br> 하지만 코딩에 익숙해지다보면 **가독성**을 확실히 높여주고 말그대로 **깔!끔!** 한 코드를 작성할 수 있는 기가 막힌 방법이다!
<br> <p style="color:blue"> 
참고로 나는 콘솔 프로젝트 시기에 동전의 앞 뒤를 표현하는데 열거형을 사용했다</p>