# Git 기초 정리 (CLI 기준)

## 1. Git 사용 목적
- 코드 변경 이력을 기록하고 관리하기 위함  
- 여러 사람이 동시에 협업할 수 있도록 지원  
- 이전 버전으로 복구 및 변경사항 비교 가능  

---

## 2. Git 레포지토리 사용

### GitHub에서 레포 생성
- GitHub → New repository 클릭  
- 저장소 이름 입력 후 생성  
- 생성된 레포지토리 URL 복사  

### 로컬에서 clone
```bash
git clone https://github.com/yongjaeee/project.git
cd project
```

### .gitignore 사용법
- Git이 추적하지 않을 파일 설정  

```bash
touch .gitignore
```


---

## 3. git add / commit / push

### 파일 스테이징
```bash
git add .
```

### 커밋
```bash
git commit -m "커밋 메시지"
```

### 원격 저장소로 업로드
```bash
git push origin main
```

---

## 4. 브랜치란 + 사용법

### 브랜치란?
- 독립적인 작업 공간 (코드 분기)  
- 메인 코드에 영향 없이 개발 가능  

### 브랜치 생성 및 이동
```bash
git checkout -b feature
```

---

## 5. merge란? + 사용법

### merge란?
- 다른 브랜치의 변경사항을 현재 브랜치에 합치는 것  

### 사용법
```bash
git checkout main
git merge feature
```

---

## 6. git log 사용법
```bash
git log
```
---

## 7. PR (Pull Request)란?
- 작업한 브랜치를 메인 브랜치에 병합 요청하는 것  