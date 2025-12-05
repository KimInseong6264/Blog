# Ⅱ. List(자료구조 개념)

#### using System.Collection.Generic;
**이거를 반드시 달아주고 사용하자!**

### 1. 배열의 강화판! List
---
**※List:** 배열이면서 길이가 자유롭게 변하는 가변배열
- 배열은 공간의 변동성을 적용하기가 어렵다.(공간에 null이 적용하기가 어려움)
- 이런 배열의 문제점을 개선하기 위해서 List를 사용한다.
- 단점: 중간  삽입/삭제 시, 연속성을 유지하기 위해 연산 부하가 생김(변동 인덱스 이후로 다시 값을 덮어씌우는 형식)

![](https://velog.velcdn.com/images/iissk/post/57c3edef-508d-4dc2-aea6-6b4d17e2d6b6/image.png)



### 2. List가 만들어지는 과정
---

> ##### 전제코드
>![](https://velog.velcdn.com/images/iissk/post/eb0dac54-e5fe-4880-bbfc-7dadbf252402/image.png)
>![](https://velog.velcdn.com/images/iissk/post/3a43bf76-d37d-465c-8ac9-7dcaa31284bf/image.png)
>![](https://velog.velcdn.com/images/iissk/post/1d4af49b-115e-4703-9ad1-eabffd08f1cf/image.png)



![](https://velog.velcdn.com/images/iissk/post/753984cb-1750-4753-a0ee-9981f145bde8/image.png)

▶ 배열의 길이를 결정하는 Capacity 생성


![](https://velog.velcdn.com/images/iissk/post/07efbe21-6920-4e14-a33b-76e2bc86b6f0/image.png)

▶ count는 class내부에서만 동작해야 하기 때문에 get만 설정(Capacity 동일)
▶ 배열 공간 자체를 직접적으로 조작하는 것은 외부에서 불가능하다.


![](https://velog.velcdn.com/images/iissk/post/debec999-47b4-4689-aab9-08c91c4480eb/image.png)

▶ class Troop의 생성자 지정, 인자값으로 배열의 사이즈를 받는다.


![](https://velog.velcdn.com/images/iissk/post/aeed2625-a04d-479d-a39c-071e24bc5a9f/image.png)

▶ **RemoveAt메서드 :** 배열 중간에 null값이 없도록 인덱스값 제거와 함께 나머지 값들을 제거한 자리부터 덮어씌우는 메서드


![](https://velog.velcdn.com/images/iissk/post/b9a844e4-af39-4ec9-85b4-61bfb02fa127/image.png)

▶ **Add메서드 :** T에 해당하는 타입의 매개변수가 들어올 때, count(현재 값이 들어있는 공간 수)에 따라 공간을 넓히고 배열값을 추가하는 메서드

![](https://velog.velcdn.com/images/iissk/post/2de8661d-2431-41cc-b316-8b6b449d6a5c/image.png)

▶ count를 0으로 만든다 = List를 비운다.


>**List는 C#내에 만들어진 클래스이며 배열의 사이즈를 변동하는데 기존의 배열보다 자유로운 것이 특징이다. List의 기본 기능부터 다양한 메서드까지 모두 기초적인 클래스, 메서드, 생성자등의 결합으로 만들어지는 것이다.**

