# Git 프로젝트 생성 및 Branch 실습 정리

## 1. 프로젝트 생성

AI(ChatGPT, Gemini 등)를 활용하여 간단한 프로그램을 생성하고 프로젝트 폴더를 만든다.

예시:

* Python 계산기 프로그램 생성
* 파일명: `calculator.py`

```bash
mkdir CalculatorProject
cd CalculatorProject
```

---

## 2. Git 저장소 생성

프로젝트 폴더를 Git 저장소로 초기화한다.

```bash
git init
```

* `.git` 폴더가 생성됨
* Git으로 버전 관리할 수 있는 상태가 됨

---

## 3. 첫 번째 Commit 생성

생성한 코드를 Git에 추가하고 첫 번째 커밋을 생성한다.

```bash
git add .
git commit -m "Initial commit"
```

* `git add` : 변경 파일을 Commit 준비 상태로 추가
* `git commit` : 변경 내용을 저장

---

## 4. Branch 생성

기능 개발을 위한 새로운 Branch를 생성하고 이동한다.

```bash
git branch feature/update
git switch feature/update
```

또는

```bash
git checkout feature/update
```

현재 작업 위치 확인:

```bash
git branch
```

---

## 5. 기능 추가

AI를 활용하여 새로운 기능을 추가하거나 기존 기능을 개선한다.

예시:

* 계산기 프로그램에 뺄셈 기능 추가

변경 후 Commit:

```bash
git add .
git commit -m "feat: add subtraction function"
```

---

## 6. Main Branch 작업

Main Branch로 이동 후 README 파일을 작성한다.

```bash
git switch main
```

README.md 작성 후 저장:

```bash
git add README.md
git commit -m "docs: add README"
```

---

## 7. Branch Merge

`feature/update` Branch의 작업 내용을 `main` Branch에 병합한다.

```bash
git merge feature/update
```

Merge 메시지 입력 화면이 나타날 경우:

```
Esc
:wq
Enter
```

순서로 저장하고 종료한다.

---

## 8. Commit 로그 확인

Commit 기록을 한 줄 형태로 확인한다.

```bash
git log --oneline
```

출력 예시:

```text
a1b2c3d Merge branch 'feature/update'
9f8e7d6 feat: add subtraction function
5e4d3c2 docs: add README
8d76dcf Initial commit
```

---

# 전체 Git 작업 흐름

```
프로젝트 생성
      ↓
git init
      ↓
git add + git commit
      ↓
Branch 생성
      ↓
기능 추가 및 Commit
      ↓
main 이동
      ↓
README 작성 및 Commit
      ↓
Branch Merge
      ↓
git log --oneline 확인
```
