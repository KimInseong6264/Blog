# Ⅲ. Dictionary

### C#에서의 도감 검색 "해시 테이블"
---
**※Hash Table:** 키와 값을 한 쌍으로 저장하는 자료구조
- **Key:** 열쇠로 쓰일 키워드(해싱되어 키워드로 동작)
- **Value:** 진짜 위 열쇠를 통해 가지고 온 값
- **Hash Function:** Key를 해싱하여 값을 배열에 지정하는 것
- Key와 Value는 1:1 대응이 되어야 한다. 이를 위반할 경우 충돌이 일어난다.

#### 키의 충돌시 해결법

![](https://velog.velcdn.com/images/iissk/post/f25ab247-f04c-4fd9-ae37-e58d67871dcc/image.png)

▶ **체이닝** 같은 Key에 2개의 Value가 입력될 시, 배열의 연결리스트를 만들어 겹치는 Value를 함께 저장


![](https://velog.velcdn.com/images/iissk/post/c4412751-c3f8-4afc-96f8-0a7f4ee0b8b4/image.png)

▶ **개방 주소법-선형 탐사** 겹치는 Value를 가까운 빈 배열에 저장


![](https://velog.velcdn.com/images/iissk/post/25a71399-955c-4c67-bbc5-cb65b2b0db79/image.png)

▶ **개방 주소법-제곱 탐사** 충돌한 수의 제곱 한 만큼 공간을 늘리고 그 공간에 저장


![](https://velog.velcdn.com/images/iissk/post/1ebe4cf2-bcb6-4683-bc97-50c14a24f64e/image.png)

▶ **개방 주소법-이중 해싱** 충돌시 재차 Hashing을 하면서 빈 배열에 저장

### 2.  Dictionary
---
**※Dictionary:** 도감처럼 특정 키워드로 원하는 value값을 꺼내는 검색메서드
- 진짜 검색하기 위한 키워드, 키워드를 통한 진짜 내용으로 구성
- List의 경우는 인덱스를 통해 값을 찾아왔다면, Dictionary는 Key를 통해 값을 찾아온다.
- Key와 Value가 1:1매칭이 되어야 한다.
ex) 도감, 아이템 검색, 데이터관리, 업적, 키입력 시스템, 튜토리얼


**기본형식**
![](https://velog.velcdn.com/images/iissk/post/534a69ea-1578-4208-9e04-eed31305ff30/image.png)



![](https://velog.velcdn.com/images/iissk/post/5a22872f-e09b-4aea-8439-86aa0e2d552a/image.png)

▶ 위의 Dictionary는 string값이 Key가 되고 , int값이 Value가 된다.


![](https://velog.velcdn.com/images/iissk/post/897cbc16-0ed9-4e22-9115-fc940b0bd772/image.png)

▶ Dictionary를 출력할 때는 깔끔하게 출력이 Key와 Value를 깔끔하게 출력할 수 있다.