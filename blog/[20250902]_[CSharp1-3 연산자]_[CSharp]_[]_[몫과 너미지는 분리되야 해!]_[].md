# Ⅲ. 연산자

**1. #region**
- 코드편집기에서 사용자가 임의로 카테고리를 나눌 수 있게 함
- 주석과 같이 컴퓨터는 이를 인식하지는 못함

![](https://velog.velcdn.com/images/iissk/post/655e992c-760e-45f4-b307-257237b8e924/image.png)

**2. 기본 사칙연산**

![](https://velog.velcdn.com/images/iissk/post/4dfe8c67-b6be-4c4a-b1db-da9cdc5abbdc/image.png)

![](https://velog.velcdn.com/images/iissk/post/476631fb-de29-4196-9dd6-3048563f0ff9/image.png)


**3. 복합대입 연산자**

![](https://velog.velcdn.com/images/iissk/post/b59a3453-f43a-4848-99cf-5ff6d781038d/image.png)


![](https://velog.velcdn.com/images/iissk/post/9a7e3ee1-c21a-4ff4-80a6-4b312b345b25/image.png)


**4. ReadLine()**
: 플레이어에게 직접 입력을 받을 수 있는 함수
- 입력을 받는 값은 C#에서는 항상 **문자열**으로 인식함
- 이를 해결하기 위해서 Parse를 통해 변환을 함

**5. Parse & TryParse**
: 문자열의 " "를 제거하는 함수 => 문자열을 숫자열로 변환

※int. Parse( 변환할 문자열 );
- Parse는 숫자가 아닌 문자열을 인식할 경우 에러가 발생하게 됨
- 이를 보완할 수 있는 것이 TryParse이다.
- 앞의 int는 다른 float, double등으로 바꿔도 무관
![](https://velog.velcdn.com/images/iissk/post/4ccf703f-36ab-4631-b16a-c1b790a36da2/image.png)


※TryParse( 변환할 문자열, out 변환을 끝낸 값을 담을 변수 );
- TryParse의 출력값은 TRUE or FALSE로만 나타남
- '변환할 문자열'이 숫자열로 변환되면 TRUE 
   변환되지 않는 문자라면 FALSE
- TRUE일 경우, 변수에 '변환된 숫자열'을 담게 됨
FALSE일 경우, 변수에 '0'을 담게 됨

![](https://velog.velcdn.com/images/iissk/post/40905682-4621-43d9-943f-84650dd7b54f/image.png)

이를 Console.WriteLine()으로 logic과 num값을 출력하면

![](https://velog.velcdn.com/images/iissk/post/167a0648-3f85-4884-81c4-001a418f92ea/image.png)

이와 같은 출력값을 나타냄을 알 수 있다.


> ## 🤔 마무리
> 
> 변수만 이용해서는 구체적인 코드 구성을 할 수 없다!  
> 나는 이 중에서 '/' 와 '%' 연산자를 왜 구분한 것인지 처음에는 잘 이해를 못했는데  
> 코드 사용을 하다보니, 몫만을 필요로 하는 문제들(물건 쌓기 시 층 구하기), 나머지만 필요한 문제들(배수를 구할 때)을 풀면서 구분 되어 있는 이유를 알 수 있었다.