# Chapter 1. 개발을 위한 Git과 Github

## Git이란?

파일의 변경 사항을 추적하고 여러 사용자 간 작업을 조율하기 위한 **분산 버전 관리 시스템(DVCS)**

- **파일 변경 사항 추적**: 언제, 어떤 변화가 있었는지 기록 → 특정 시점으로 되돌아갈 수 있음
- **협업 지원**: Github(원격 저장소)를 통해 여러 사용자가 동일한 파일을 공유하고 작업
- **분산**: 원격 레포의 내용을 각자의 로컬에 내려받아 개별 작업 후 반영

---

## 파일 관리 구조

```
Working Directory → (git add) → Staging Area → (git commit) → Local Repository → (git push) → Remote Repository
```

| 영역 | 설명 |
|------|------|
| Working Directory | 현재 작업 중인 폴더. `.gitignore`에 등록된 파일은 추적 제외 |
| Staging Area | 커밋 준비 단계. `add`된 파일이 올라오는 곳 |
| Local Repository | 커밋이 기록되는 로컬 저장소 |
| Remote Repository | Github 등 인터넷 상의 원격 저장소 |

---

## 주요 Git 명령어

### 기본 명령어

```bash
git add .                    # 모든 변경 파일 staging
git add <파일명>              # 특정 파일만 staging
git commit -m "커밋 메시지"  # 로컬 레포에 기록
git push origin <브랜치명>   # 원격 레포에 반영
git status                   # 현재 파일 상태 확인
git log                      # 커밋 기록 조회
```

### .gitignore

추적하지 않을 파일을 지정하는 파일

```bash
temp.txt        # 특정 파일 제외
*.txt           # 특정 확장자 전체 제외
folder_name/    # 특정 폴더 제외
```

---

## Branch

서로에게 영향을 주지 않고 독립적으로 작업하기 위한 개념. 보통 **기능 단위**로 분리.

```bash
git branch <브랜치명>         # 브랜치 생성
git switch <브랜치명>         # 브랜치 이동 (Git 2.23+)
git checkout <브랜치명>       # 브랜치 이동 (구버전)
git merge <병합할 브랜치>     # 현재 브랜치에 병합
```

> 협업 시에는 직접 `merge`하지 않고 **Pull Request**를 통해 병합

### HEAD

현재 브랜치의 **가장 최신 커밋**을 가리키는 포인터

---

## Issue & Pull Request

### Issue
- 기능 구현 / 버그 수정 / 리팩토링 등 작업 단위를 팀원과 공유하기 위한 것
- 구성: 제목, 내용, Assignees, Labels, Development 등

### Pull Request (PR)
- 기능 브랜치의 작업을 메인 브랜치에 반영해달라는 요청
- 코드 리뷰(Code Review) 가능
- **Merge는 PR 승인 후 진행** (과제에서는 Merge 금지!)

---



