### 1. Git 설치하기

🔹 **Windows**

1) 공식 홈페이지 접속: https://git-scm.com/

2) "Download for Windows" 클릭

3) 설치 파일 실행 후 기본값으로 계속 Next

4) 설치 완료 후 Git Bash 실행 또는 VSCode 터미널 사용 가능

🔹 **macOS**

터미널에서 아래 명령어 입력:

<pre>git --version</pre>

설치되어 있지 않으면 Xcode Command Line Tools 설치 창이 뜸

또는 https://git-scm.com 에서 수동 다운로드 가능

🔹 **Linux (Ubuntu 기준)**

<pre>sudo apt update
sudo apt install git</pre>

✅ **설치 확인**

<pre>git --version</pre>

예시: 
<pre>git version 2.44.0</pre>

※ 각자 개발 하시는 곳에서 터미널 키셔서 Git Bash로 변경하시고 명령어 입력하시면 됩니다.

---

### 2. Git 사용자 정보 등록 (최초 1회만)
<pre>git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"</pre>
---

### 3. Git 프로젝트 작업 순서

✅ 1) Git 초기화

<pre>git init</pre>

✅ 2) 원격 저장소 연결

<pre>git remote add origin https://github.com/your-id/your-repo.git</pre>

✅ 3) 브랜치 생성 및 이동

자신의 이름이나 파트 이름으로 브랜치 만들어주세요.

<pre>git checkout -b your-branch-name</pre>

예시:

<pre>seongmin_backend
princess_seongmin
git checkout -b princess_seongmin # 이런식으로</pre>

✅ **자신이 어디 브랜치에 연결되어있는지 확인하세요(중요)**
<pre>git branch</pre>
※현재 브랜치 앞에 *가 붙습니당.

✅ 이미 있는 브랜치로 이동
<pre>git checkout your-branch-name</pre>
만약에 main이나 다른 브랜치에 있다면 꼭 자신이 만든 브랜치로 이동해주세요(이거 진짜 중요함!)

✅ 4) 파일 추가 및 커밋

<pre>git add .
git commit -m "작업 내용 간단히"</pre>

✅ 5) 원격 저장소에 브랜치 푸시
 (최초 1회만 -u 옵션 사용 권장)

<pre>git push -u origin your-branch-name</pre>

예시: 
<pre>git push -u origin seongmin/backend</pre>

→ 이후부터는 git push만 입력해도 자동으로 해당 브랜치에 푸시됩니다

예시: 
<pre>git push origin seongmin/backend</pre>
---

### 4 .gitignore 파일 생성 꼭해주세요!!!(강조x100)

**- `.gitignore`는 팀원별 환경 차이로 인한 충돌 방지를 위한 필수 설정입니다.**

**- `venv`, `.idea`, `build` 등 불필요한 파일이 올라오지 않도록 확인해주세요.**

**- 파일 push 전 `.gitignore` 설정 여부를 다시 한 번 확인해주세요!**

**- ignore파일 안 만들고 push하면 나중에 병합할 때 정말 곤란해집니다!!**

**예시입니다!! 각자 환경에 맞춰서 작성해주세요!!**
🔸 **Python**
<pre>__pycache__/
*.pyc
.env # 특히 이거는 push되는 순간 진짜 큰일납니다.
venv/
.idea/
.vscode/</pre>

🔸 **flutter**
<pre>build/
.dart_tool/
.packages
.pub-cache/
.idea/
.vscode/
*.iml</pre>
