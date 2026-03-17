# WEEK 1 개발을 위한 Git과 Github에서 배운 점 정리
---

# 1. git이란 무엇인가?
## 정의
- Git이란 파일의 변경 사항을 추적하고 작업들을 조율하기 위한 버전 관리 시스템이다.
- 여기서 추적이란, 파일 내 변화를 기록하고 찾아주는 것을 의미한다.

---

# 2. github은 또 무엇인가?
## 정의
- Github이란 git을 기반으로 소스 코드를 저장, 공유, 협업할 수 있는 웹 기반 개발자 플랫폼이다.
- 개발을 진행할 때는 github은 클라우드와 같은 원격 저장소이자 공동 작업자(개발자)들과의 소통을 할 수 있는 인터페이스 창구가 되기도 한다.
- Git과 Github를 통해 우리는 편하게 협업이 필요한 큰 프로젝트를 여러 개발자와 협력하여 작업하고, 작업 결과를 기록할 수 있다. 그래서, Git은 "분산 버전 관리 시스템"이라고 한다.

---

# 3. Git은 어떻게 여러 파일을 관리할까?
## 개념 및 용어 정리
(1) 저장소 (Repository) : 작업하는 파일들이 저장되는 폴더이다. (내 개인 컴퓨터의 저장소를 Local Repository라고 하고, github에 있는 저장소를 Remote Repository라고 한다.
(2) 나의 작업 공간 (Working Directory): 마치 리눅스의 pwd처럼 현재 작업하고 있는 공간(폴더)를 의미한다. 해당 공간 내의 파일들은 git에 의해 추적된다. (하지만, 아직 git add를 하지 않은 (거의 신규)파일들은 추적되지 않는다. 이를 untracked 상태라고 한다.)
(3) Staging Area: git add 했을 때 파일이 올라가는 층이다. git add가 되면 git이 해당 파일을 추적하기 시작한다. 그리고, staging area에 있는 파일을 commit 하면 나의 레포지토리에 완벽히 저장된다.

---

Working Directory -> Staging Area -> Local Repository -> Remote Repository라고(? 너무 일반화이긴 하지만..) 생각하면 된다.

---

# 4. Git과 Github 연동하는 법
1. 내 계정의 Github의 Repository로 가 New를 눌러 새로운 Remote Repository를 만든다.
2. 새로 만든 Repository의 url 주소를 복사하여 연동하고 싶은 디렉토리(폴더)에서 cmd를 쳐서 **git clone (url)**을 적으면 연동이 되며 해당 폴더에 원격 레포 폴더가 생긴 것을 알 수 있다.
3. 윈도우에서는 touch 등의 리눅스 명령어가 잘 안되므로, git bash로 들어가 해당 폴더로 경로를 이동하고 (cd) touch .gitignore파일을 만들어 git의 추적을 해제할 파일이나 디렉토리 집합을 적는다.(보안 등)
4. **git add .** 로 새로 만들어 아직 untracked 상태인 파일들을 staged 상태로 마든다.(staging area로 올리기!) (특정 파일만 올리고 싶을 때는 **git add (파일 이름)**이라고 한다.
5. **git commit -m "커밋 메시지"**로 로컬 레포에 저장 및 기록한다. 
6. **git push origin (브랜치 이름)**을 통해 로컬 레포에 커밋된 파일을 원격 레포에도 올린다.
7. **git status**를 통해 확인한다.(난 아직 초보니까 늘 확인하는 습관을 들이자)

---

# 5. Branch란??
- 나뭇가지라는 뜻으로 main 브랜치(실제 git에 있는 메인 프로젝트 파일)을 변경하기 무서울 때나 여러 기능을 여러 프로젝트 팀이 따로따로 맡을 때, 메인 프로젝트를 똑같이 복제한 프로젝트를 만든 것이다.
- 이로써 메인 프로젝트를 건들지 않은 채, 여러 가지(branch)에서 개발할 수 있다!!

## Branch 만들고 전환하는 법
1. git branch (브랜치 이름)
2. git switch (브랜치 이름)
3. branch에서 개발
4. 개발한 내용을 main 브랜치에 적용할 때는 git merge (병합할 브랜치)를 하는데, 애는 잘 사용하지 않는다. (위험하기 때문!!!)
5. merge 대신 Pull Request를 많이 사용한다.

---

# 기록 확인하는 법
- git log 를 통해 커밋 기록을 볼 수 있다. (git log --oneline --graph --all 를 사용하면 더 좋다고 한다.)
- git log의 출력 형식은 다음과 같다.
> **커밋 해시** : `commit 691ceb4268ec2c5b2d1afd79dd41f5783dcfac46` (HEAD -> main, origin/main, origin/HEAD)
>
> **커밋 생성자** : `youz2me <kynhun20@gachon.ac.kr>`
>
> **커밋 일시** : `Sun Sep 22 18:34:03 2024 +0900`
>
> **커밋 메시지:** `fix: validate 명령어 파라미터 안들어가게 수정`

- 여기서 HEAD는 무엇이냐???
현재 브랜치의 최신 커밋을 참조하는 값으로, 브랜치의 최신 커밋을 포인터로 가리키고 있다. 그래서, 다른 브랜치에서 커밋을 하고, git log를 하면, HEAD -> hedgehog_Ko가 된다!

---
