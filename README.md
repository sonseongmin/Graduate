### 💻 1. Git 설치하기

🔹 Windows

1) 공식 홈페이지 접속: https://git-scm.com/

2) "Download for Windows" 클릭

3) 설치 파일 실행 후 기본값으로 계속 Next

4) 설치 완료 후 Git Bash 실행 또는 VSCode 터미널 사용 가능

🔹 macOS

터미널에서 아래 명령어 입력:

git --version

설치되어 있지 않으면 Xcode Command Line Tools 설치 창이 뜸

또는 https://git-scm.com 에서 수동 다운로드 가능

🔹 Linux (Ubuntu 기준)

sudo apt update
sudo apt install git

✅ 설치 확인

git --version

→ 예시: git version 2.44.0
---
🛠️ 2. Git 사용자 정보 등록 (최초 1회만)
<pre>git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"</pre>
---
📂 3. Git 프로젝트 작업 순서

✅ 1) Git 초기화

git init

✅ 2) 원격 저장소 연결

git remote add origin https://github.com/your-id/your-repo.git

✅ 3) 브랜치 생성 및 이동

자신의 이름이나 파트 이름으로 브랜치 만들어주세요.

git checkout -b your-branch-name

예시:

seongmin/backend

jihyun/frontend

feature/login-page

✅ 4) 파일 추가 및 커밋

git add .
git commit -m "작업 내용 간단히"

✅ 5) 원격 저장소에 브랜치 푸시

git push origin your-branch-name

예시: git push origin seongmin/backend
