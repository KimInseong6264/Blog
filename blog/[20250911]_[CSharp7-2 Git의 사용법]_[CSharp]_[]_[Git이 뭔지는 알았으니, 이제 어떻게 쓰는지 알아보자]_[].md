# Ⅱ. Git의 사용법


### 1. Commit : 임시 저장
---

![](https://velog.velcdn.com/images/iissk/post/2d1b3e11-925b-4c17-9b33-b15d5a0e047c/image.png)

![](https://velog.velcdn.com/images/iissk/post/04564725-67aa-4ec9-adf2-0061c85ff3e8/image.png)

▶ Repository를 새로 만들어서 Local에 저장할 공간을 확보(Localrepo 형성)
▶ ReadMe(Remote에 올린 파일의 설명을 적기 용이)를 만드는 것을 습관화한다.


![](https://velog.velcdn.com/images/iissk/post/c26c3854-1ae6-4a78-be82-5281b9a29e15/image.png)

▶ LocalRepo 폴더에 들어있는 프로젝트, 소스코드등의 변동사항이 Staging area에 기록이 된다.


![](https://velog.velcdn.com/images/iissk/post/484dd2bd-5602-4dbf-ab9f-62bcc9461ea7/image.png)


![](https://velog.velcdn.com/images/iissk/post/cbc29d4b-7d6c-47da-8c66-a43b2b490948/image.png)

▶ 프로젝트를 생성된 Repository에 옮겨주면 Git에 자동으로 자동저장된다.
▶ 이후 변동 사항을 Commit하면 Local에 저장된다.


![](https://velog.velcdn.com/images/iissk/post/9e58bb56-af61-4634-97c8-8da345716956/image.png)


![](https://velog.velcdn.com/images/iissk/post/c937a33d-39d8-46d6-8bcd-baf1da83a522/image.png)

▶ 변동사항에 따라 색깔이 다르게 표시가 된다.
▶ 좌하단의 내용을 입력하고 Git Commit 진행
	ㄴ 기본용어 및 팀규칙 참고



![](https://velog.velcdn.com/images/iissk/post/66b1114b-9be4-48af-bd49-e73b570265c3/image.png)


![](https://velog.velcdn.com/images/iissk/post/d4b7a3fa-4e9e-4c6b-8609-7ec5f05ddb31/image.png)

▶ History를 통해 Commit 된 리스트 확인가능하다.

#### 2. Push : 원격으로 업로드
---

![](https://velog.velcdn.com/images/iissk/post/ae8f3cc9-be23-4f94-b708-6dafc73bd0ba/image.png)

▶ Commit만 진행했을 때, 로컬에만 저장되어 있다.


![](https://velog.velcdn.com/images/iissk/post/5709a4a1-f10d-473e-9812-714f20016e18/image.png)

▶ Commit을 진행 한 후에 Push Origin 활성화 시에 클릭


![](https://velog.velcdn.com/images/iissk/post/aad7efb1-6afe-4ba1-ae9b-2dfd2b75c831/image.png)

▶ Push를 함으로 Remote에 저장이 된다.


### 3. 원격 수정
---

![](https://velog.velcdn.com/images/iissk/post/22695f93-b6eb-45d0-9915-c5f03916d8d3/image.png)

![](https://velog.velcdn.com/images/iissk/post/787949be-e71c-4916-8582-e9bff197de42/image.png)

▶ GitHub 홈페이지에서 수정이 가능하다.


### 4. Pull : Local로 다운로드
---

![](https://velog.velcdn.com/images/iissk/post/76b57fc3-d3d7-4acc-92cd-3a46fa31cf21/image.png)
▶ Clone repository 통해 다운로드(원격에서 열기)가 가능하다.

![](https://velog.velcdn.com/images/iissk/post/2b800b44-b40d-417c-a251-5fea7305f15a/image.png)
▶ 원격에 있는 커밋을 Local로 다운로드한다.

![](https://velog.velcdn.com/images/iissk/post/b1965172-220c-497f-a6d5-c9e70862f816/image.png)
▶ Fetch origin(새로고침)를 통해 커밋을 읽어오고 Pull origin을 통해 Git으로 옮겨온다.

### ※코드 충돌을 막으려면 Step By Step으로 순차적으로 작업을 진행해야 한다.

#### Local에서 Commit을 새로 만들고, Push한다.
#### Fetch 하고 Pull로 당겨와서 작업한다.
<br> <p style="color:red"> 
**Local에 저장된 파일로 무작정 작업해서는 안됨**
</p>


>## <p style="color:green"> 🤔 마무리</p>
> Git은 많이 사용해봐야만 감을 익힐 수 있는 것 같다.
<br> 앞으로 계속해서 파일을 관리하다보면 자연스럽게 Git 사용법을 익힐 수 있을 것이다. 
<br> <p style="color:blue"> 
반드시 다음날 작업을 하는 경우처럼 내 컴퓨터의 로컬 파일을 그대로 수정을 하는 습관보다 **항상 원격의 내용을 Pull받고 작업을 하자!**
<br>
(당연히 작업이 끝난 건 바로바로 푸쉬하는 습관도 들여야 함)
</p>