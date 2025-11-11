# Ⅲ. 코드 충돌


### 1. 코드충돌
---
**※** 수정이 잦은 프로젝트, 타인과의 협업등에서 각각의 Commit들에서 중복된 수정이 발견될 경우 *코드충돌*이 발생한다.

## ※코드 충돌을 막기 위한 방법
### 1. 코드 새로 작성하기 전에 최신작업 확인!!
- **절대 Local에 저장된 파일로 바로 작업X**
### 2. Fetch부터 받고, 최신본을 먼저 Pull받기!!
### 3. Pull받은 최신본으로 변동사항 작업진행!!
### 4. Commit 만들고 수정본을 Push한다!!


![](https://velog.velcdn.com/images/iissk/post/061e0443-f3bd-4fd5-8bb7-13838bca36c7/image.png)

![](https://velog.velcdn.com/images/iissk/post/341ae05e-7b4e-46a0-a87d-1551184c06d9/image.png)

▶ Local의 Commit과 Remote의 Commit의 동일한 코드를 각각 다르게 수정

![](https://velog.velcdn.com/images/iissk/post/ab346ebe-e2b3-4f16-8743-6b0892e3e3ef/image.png)

▶ Remote에서의 세이브버전이 서로 충돌했다는 문구, Fetch하라는 내용

![](https://velog.velcdn.com/images/iissk/post/8f704221-e86b-42df-9515-47ef78008de2/image.png)

▶ 같은 줄을 누군가 수정했다는 걸 알려준다.
<br>
▶ Fetch origin : 원격에서 수정된 사항이 있을 때, 갱신해주는 것


![](https://velog.velcdn.com/images/iissk/post/224a47ec-1f88-42c7-9d2a-47731342c326/image.png)

▶ Use the....main : Local의 Commit을 쓰겠다.
<br>
▶ Use the....ongn_main : Remote의 Commit을 쓰겠다.
<br>
▶ Open with ~ : 희망 코드에디터로 직접 코드 수정


![](https://velog.velcdn.com/images/iissk/post/017a4a10-0193-4766-b713-cb5ba0d138d1/image.png)

▶ 수정 파일을 열면 새로운 주석이 생성되어 있다.
<br>
▶ HEAD와 추가된 주석들을 지워주면 수정 사항을 저장할 수 있다.
- 특별히 수정할 내용이 크게 없다면 주석만 지워주면 됨

![](https://velog.velcdn.com/images/iissk/post/2c209895-46c9-4407-9e0a-69d3bd70d6ce/image.png)
▶ 주석만 지워주고 충돌했던 코드를 모두 유지한 상태


![](https://velog.velcdn.com/images/iissk/post/29ae9641-06a3-4d70-9512-60fc541bc10d/image.png)
▶ 수정이 완료되면면 충돌이 되었다는 것을 확인할 수 있다.


![](https://velog.velcdn.com/images/iissk/post/27d3cdb6-5f6d-4a9e-bc16-18349dd44ca6/image.png)
▶ Push가 2개로 나오게 됨 - 원래 Local에 1개가 있고, merge한(수정) Commit이 하나 더 생겨서 2개가 발생하는 것


>## <p style="color:green"> 🤔 마무리</p>
> Git이 얼마나 중요하면 3개로 나눠서 글을 적었을까 싶다. 
<br>
그만큼 중요하기도 하고 실수하기도 너무 
<br>
앞으로 계속해서 파일을 관리하다보면 자연스럽게 Git 사용법을 익힐 수 있을 것이다. 
<br> <p style="color:blue"> 
반드시 다음날 작업을 하는 경우처럼 내 컴퓨터의 로컬 파일을 그대로 수정을 하는 습관보다 **항상 원격의 내용을 Pull받고 작업을 하자!**
<br>
(당연히 작업이 끝난 건 바로바로 푸쉬하는 습관도 들여야 함)
</p>