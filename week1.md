# Git & GitHub 기초 정리

## 1. Git이란?
Git은 파일의 변경사항을 기록하고 관리하는 버전 관리 시스템이다.  
파일을 여러 개 복사해서 저장하는 대신, 변경된 부분만 저장해서 효율적으로 관리할 수 있다.

- 수정 이력 확인 가능
- 이전 버전으로 되돌리기 가능
- 협업 시 동일한 파일 공유 가능

## 2. GitHub와 로컬/원격 개념

- 로컬(local): 내 컴퓨터
- 원격(remote): GitHub 같은 온라인 저장소

GitHub를 통해 여러 사람이 같은 프로젝트를 공유하고 협업할 수 있다.

## 3. Git 구조

1) Working Directory  
실제 파일을 수정하는 작업 공간

2) Staging Area  
커밋할 파일을 선택하는 공간 (git add)

3) Local Repository  
커밋이 저장되는 공간 (git commit)

흐름: 작업 → add → commit → push

## 4. 주요 명령어

git add .
git commit -m "메시지"
git push origin main

add: 파일을 스테이징 영역에 올림  
commit: 변경 내용을 저장  
push: GitHub에 업로드  

## 5. .gitignore

특정 파일을 Git이 추적하지 않도록 설정하는 파일이다.

예시:
ignore.md
*.txt

보안 파일이나 필요 없는 파일을 제외할 때 사용한다.

## 6. 브랜치 (Branch)

브랜치는 독립적인 작업 공간이다.

- 여러 작업을 동시에 진행 가능
- 서로 영향을 주지 않음

git checkout -b 브랜치명

기능별로 나누어 작업할 때 사용한다.

## 7. merge와 PR

merge: 브랜치를 합치는 작업  
Pull Request: 코드 합쳐달라고 요청하는 것  

협업에서는 PR을 통해 리뷰 후 merge를 진행한다.

## 8. commit 기록 확인

git log

커밋 기록을 확인하고 변경 이력을 추적할 수 있다.