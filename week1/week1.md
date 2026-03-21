# Git이란?
===
1. 파일을 여러 번 수정하며 생기는 변동 사항들을 저장하는 버전 관리를 도와주는 것
2. 원격  저장소를 이용하여 한 파일을 동시에 여러 사용자의 컴퓨터에서 접근할 수 있으며 해당 파일의 기록 또한 각 사용자의 컴퓨터에서 확인 가능 -> 모든 사용자가 동일한 작업 내용 공유로 협업 가능
3. 분산 버전관리 가능: 여러 명이 한 파일에 접근해 개별적으로 작업하고, 작업 결과를 기록으로서 반영하는 시스템

## 파일 버전 관리
===
- 여러 파일을 한꺼번에 관리해야할 경우, Git이 repository라는 개념으로 작업하는 파일들이 저장되는 폴더를 만들어 관리하도록 도움.
- 사용자의 컴퓨터 내의 로컬 repository, Github에 올라가 있는 원격 repository로 나누어 관리

1. Working directory: 내가 현재 작업하고 있는 공간
2. Staging Area: 파일의 변경사항 반영하는 공간. unmodified -> modified -> staged로 구간을 나눠 선택적으로 commit할 수 있도록 도움
3. Local Repository: staging area에 올라가 있는 파일들을 commit하여 변경 사항들을 기록하는 곳

### Branch
===
- Main branch: 최종적으로 모든 파일을 합치는 메인 branch
- Merge: 각자의 개별 branch에서 개발한 내용을 병합
- issue: 깃허브에서 협업시 프로젝트의 현황, 수정, 리팩토링 등 공유
- Pull Request(PR): 메인 branch에게 Pull을 받아줄 것을 요청하는 것

### Git 명령어
===
- git clone (repository 주소): 원격 저장소 복사
- git add .: 모든 파일을 staged 상태로 변경
- git commit -m "메시지": staged된 파일들의 변경 사항을 메시지와 함께 기록
- git push origin (브랜치 명): 내 local 레포에 반영된 내용을 GitHub로 전송
- git status: 현재 파일들의 상태 확인
- git switch (브랜치 명): 작업공간(branch) 이동