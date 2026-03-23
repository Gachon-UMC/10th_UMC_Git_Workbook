# Git 정리 (1주차)

Git은 파일의 변경 사항을 추적하고 여러 사용자 간에 해당 파일들의 작업을 조율하기 위한 **분산 버전 관리 시스템**입니다.

### 1. 로컬과 원격

- **내 컴퓨터** - 로컬(local)
- **GitHub** - 원격(remote)
- 원격(remote)을 이용해 파일 또는 폴더를 다운 받아 내 컴퓨터(local)에서 확인 가능

- **분산형 VCS (Distributed VCS)**
    - 중앙에서 관리하던 저장소 전체를 복사하여 사용자의 컴퓨터로 가져옴

---

### 2. 저장소와 작업 공간

- **저장소(repository)**: 작업하는 파일들이 저장되는 폴더
    - local repository, remote repository
- **working directory**: 현재 내가 작업하고 있는 공간(폴더)
- **.gitignore**: 추적되지 않는 파일 목록 지정
    ```bash
    touch .gitignore
    ```

    - working directory 내에서 추적되지 않아야 하는 파일들을 지정
    - 처리된 파일들은 변화가 생겨도 추적되지 않고 원격 repository에도 올라가지 않음

---

### 3. Git 작업 흐름

#### 3-1. 파일 상태

- **변경 없음 (unmodified)**: 변경되지 않은 파일
- **변경됨 (modified)**: 변경된 파일
- **스테이지됨 (staged)**: commit을 위한 준비 단계

#### 3-2. Staging Area

- staged 상태의 파일들을 모아두는 공간
- 내가 반영하고 싶은 변경 사항을 `add`로 stage 상태로 만들고, `commit`을 통해 **local repository**에 반영
- 이후 `push`를 통해 local repository의 변경 사항을 **remote repository**에 반영

---

### 4. Git 명령어

#### 4-1. Remote Repository 생성 후 연결

1. **Repository 생성**
    - Repository name: 최상위 폴더 이름
    - Description: 부가 설명 작성
    - Public / Private: 공개 여부 선택

2. **로컬에서 연결**

```bash
git clone (repository 주소)       # 원격 레포 복사
git add .                         # 모든 파일을 staged 상태로 추가
git add (파일이름)                 # 특정 파일만 staged 상태로 추가
git commit -m "커밋 메시지"       # 변경 사항 기록
git push origin (브랜치 이름)     # 원격 레포에 반영
```

---

### 5. 브랜치 (Branch)

- 브랜치는 개발자들이 동시에 작업하면서 서로에게 영향을 주지 않도록 하는 기능입니다.
- 브랜치 관련 주요 명령어:

```bash
git branch <브랜치 이름>    # 브랜치 생성
git switch <브랜치 이름>    # 브랜치 이동
git merge <병합할 브랜치>   # 현재 브랜치에 다른 브랜치 변경 사항 적용
```

---

### 6. 로그 확인 (Log) 및 HEAD

- Git에서 커밋 내역을 확인하고 현재 브랜치의 상태를 보는 방법
- 주요 명령어와 설명:

```bash
git log        # 커밋 내역 확인
git log --oneline  # 한 줄로 간단하게 커밋 내역 확인
git log --graph    # 커밋 히스토리를 그래프로 확인
```
