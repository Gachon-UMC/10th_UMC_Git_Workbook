# 1주차 Git 스터디 정리

## Git이란?
- 파일의 변경 사항을 추적
- 여러 사용자간에 해당 파일들의 작업들을 조율
- 분산 버전 관리시스템

## 주요 명령어
### 기본 명령어
- git clone (레포지토리 주소): 원격레포 복제
- git status: 파일 상태 확인
- touch .gitignore: gitignore 생성

### 파일 관리
- git add .: 모든 변경사항 스테이징
- git commit -m "메시지": 변경사항 커밋
- git push origin 브랜치명: 원격레포에 푸시

### 브랜치 관리
- git branch: 브랜치 목록 확인
- git branch 브랜치명: 새 브랜치 생성
- git switch 브랜치명: 브랜치 전환
