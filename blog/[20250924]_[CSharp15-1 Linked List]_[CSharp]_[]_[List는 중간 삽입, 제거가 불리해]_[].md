# Ⅰ. Linked List

### 1. 삽입/제거에 용이한 리스트 Linked List
---
**※Linked List:** 데이터와 데이터가 연결은 되어있지만 연속적으로 연결되어있지 않고, 각 데이터는 앞뒤의 값만을 기억한다.
- 최소 2가지의 정보를 필요로 한다.(자료의 값 + 자리 주소값)
- ex) 레이드 파티 가입 탈퇴 , 프리셋 , 메이플 시퀀스

**※Node:** 각 데이터와 참조(주소)를 담은 덩어리
- **Data:** 진짜 저장할 값
- **Next:** 다음 노드 주소 정보(기본 단방향)
- **HEAD:** 첫 번째가 되는 노드(노드의 시작점, 노드의 총 갯수인 count 기억)

![](https://velog.velcdn.com/images/iissk/post/d259ae05-fc82-4339-9b94-71b8a160667d/image.png)

▶ Head와 Tail에는 data가 들어있지 않다.

###### 생성방식
![](https://velog.velcdn.com/images/iissk/post/347a855b-ef53-4e35-848b-5ec8ed4bcfb1/image.png)



### 2. List가 만들어지는 과정
---

> ##### 전제코드
>![](https://velog.velcdn.com/images/iissk/post/e8f49d5d-d424-4578-bc2c-d33b99615fc5/image.png)
>![](https://velog.velcdn.com/images/iissk/post/56f6d0a3-7737-4297-82a6-19ee868b44d6/image.png)
>![](https://velog.velcdn.com/images/iissk/post/2b395a66-7281-4f59-908d-cba074138ee4/image.png)
>![](https://velog.velcdn.com/images/iissk/post/2399cc20-826f-471f-b710-98cc9b066cbc/image.png)



![](https://velog.velcdn.com/images/iissk/post/11e45a47-7254-429c-a1ef-87f590260b36/image.png)

▶ 처음 생성되는 Node는 다음으로 올 Node가 없으므로 null로 지정


![](https://velog.velcdn.com/images/iissk/post/fa170209-cfba-4bb6-8eab-65c643494c5f/image.png)

▶ Head는 Node< T >의 주소값이므로 Next와 서로 타입을 공유한다.


![](https://velog.velcdn.com/images/iissk/post/418984e9-d284-490b-a3aa-9ccca1ce2de6/image.png)

▶ **AddLsat** 리스트 맨 끝에 노드를 추가하고 연결한다.(처음 생성시에는 Head에 다음 주소값이 부여된다.)


![](https://velog.velcdn.com/images/iissk/post/43c4594a-aac0-44b9-a443-a02c370f9294/image.png)

▶ **Remove** 입력한 value에 해당하는 node를 찾아서 제거(Head가 제거시 새로운 Head가 만들어진다.)


![](https://velog.velcdn.com/images/iissk/post/bb5b5227-8c51-44e7-918d-95f01fd347ef/image.png)

▶ **Find** 특정 node를 찾아주는 메서드




![](https://velog.velcdn.com/images/iissk/post/95dd5f5b-d369-42d4-ba25-66103e79c81e/image.png)

value의 확인이 필요하다!
