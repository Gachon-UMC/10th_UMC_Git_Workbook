Git: 파일의 변경 사항을 추적하고 여러 사용자 간에 해당 파일들의 작업들을 조율하기 위한 분산 버전 관리 시스템
Git의 역할: 파일의 변경사항을 저장하고 체계적으로 관리, 한 파일을 동시에 여러 사용자가 접근할 수 있도록 해줌, 여러 작업자의 개별 작업 결과를 기록으로서 반영

Working Directory: 내가 현재 작업하고 있는 공간(폴더), 이 때 보안 등의 문제로 공유하지 않는 파일은 ".gitignore" 파일을 생성하여 관리
> staged(add) > commit >
staging area: 진행 상황을 저장해두는 세이브포인트 같은 개념
> commit >
Local Repository: 파일의 변경 사항을 기록하는 곳
> push >
원격 Repository

Git Repository
Repository name: 레포지토리의 이름
Description: 레포지토리의 부가적인 설명을 작성하는 부분
Public/Private: 레포지토리의 공개 여부

git clone (레포지토리 주소): Git clone 폴더 생성 및 연결

gitignore 관리: 터미널에서 .gitignore 또는 gitignore.io를 사용해서 생성
touch .gitignore: 숨김처리(.)된 파일을 파일 탐색기에서 숨김 해제
*.txt # *.(확장자 이름): 확장자에 따라 추적 해제
folder_name/ # (폴더 이름)/: 폴더를 추적 해제
git add .: 모든 파일 staged
git add (파일 이름): 특정 파일 staged
git commit -m "(커밋 메시지)"
git push origin (브랜치 이름)
git status: 내 파일 상태 확인

branch: 작업하는 독립적인 영역
git branch (브랜치 이름): 브랜치 생성
git checkout (브랜치 이름) / git switch (브랜치 이름): 브랜치 이동(switch 추천)
git merge (병합할 브랜치): 브랜치 병합

git log: 커밋 기록 확인
> **커밋 해시** : `commit 691ceb4268ec2c5b2d1afd79dd41f5783dcfac46`
> 
> 
> **커밋 생성자** : `youz2me <kynhun20@gachon.ac.kr>`
> 
> **커밋 일시** : `Sun Sep 22 18:34:03 2024 +0900`
> 
> **커밋 메시지:** `fix: validate 명령어 파라미터 안들어가게 수정`
>

HEAD: 내 브랜치의 가장 최신 주소, 이전 브랜치의 commit 기록을 가져옴

Issue: 프로젝트 작업 진행 현황과 기능 구현, 버그 수정, 리팩토링 등을 공유하기 위해 생성
Pull request(PR): 내 작업을 메인 브랜치에 반영하기 위해 생성, 메인 브랜치에 Pull 요청