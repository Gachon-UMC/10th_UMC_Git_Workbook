# 📌 1주차 Git 정리

## 🔥 Git이란?
Git은 파일의 변경 사항을 기록하고 관리하는 **분산 버전 관리 시스템**이다.  
이전 버전을 저장하고 필요할 때 되돌릴 수 있으며, 여러 사람이 동시에 작업할 수 있도록 도와준다. :contentReference[oaicite:0]{index=0}

---

## 📁 Git의 기본 개념

### 1. Working Directory
현재 내가 작업하고 있는 폴더 공간

### 2. Staging Area
커밋하기 전, 변경된 파일을 올려두는 공간

### 3. Local Repository
commit을 통해 변경사항이 저장되는 공간

---

## 🔄 Git 작업 흐름
```bash
git add .
git commit -m "메시지"
git push origin 브랜치명

- add → 파일을 staging area로 이동
- commit → 변경사항 저장
- push → GitHub(원격 저장소)에 업로드


## 🗂️ .gitignore

특정 파일을 Git이 추적하지 않도록 설정하는 파일
예시 :
ignore.md
*.txt

## 🌳 Branch

브랜치는 독립적으로 작업할 수 있는 공간이다.
여러 사람이 동시에 작업할 때 서로 영향을 주지 않도록 도와준다.

예시 :git checkout -b 브랜치이름

상태 확인 git status

--- 

📌 핵심 정리
Git은 버전 관리 도구이다
add → commit → push 흐름 중요
.gitignore로 파일 추적 제외 가능
브랜치로 협업 가능