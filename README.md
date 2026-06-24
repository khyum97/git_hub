<p align="center">
  <img src="./github-rainbow.png" width="180" alt="GitHub Local Manager Logo" />
</p>

<h1 align="center">GitHub Local Manager (GLM)</h1>

<p align="center">
  로컬 Git 저장소들과 GitHub 원격 저장소를 직관적으로 매핑하고, 복잡한 Git 조작을 한곳에서 쉽고 빠르게 실행하는 프리미엄 로컬 웹앱 대시보드입니다.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js Badge" />
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" alt="Express Badge" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git Badge" />
  <img src="https://img.shields.io/badge/Windows-0078D6?style=flat-square&logo=windows&logoColor=white" alt="Windows OS" />
</p>

---

## 🌟 주요 기능 (Key Features)

* **🔑 자동 로그인 및 토큰 연동**: GitHub Personal Access Token (PAT)을 1회 연동하면 로컬 보안 캐싱을 통해 이후 앱 실행 시 자동으로 로그인되어 바로 대시보드로 진입합니다.
* **📂 로컬 저장소 원클릭 자동 탐색**: 컴퓨터 내부(C, D, E드라이브 핵심 경로)를 깊이 3까지 고속 스캔하여 GitHub과 연결된 모든 로컬 Git 폴더를 감지해 자동으로 연동합니다.
* **📦 원클릭 클론 & 수동 연동**: 윈도우 네이티브 폴더 브라우저 창(`FolderBrowserDialog`)을 통해 기존 로컬 프로젝트 폴더를 바로 맵핑하거나, 원격 리포지토리를 새 폴더에 깔끔하게 클론할 수 있습니다.
* **⚡ 스마트 푸시 & 자동 커밋**: 번거로운 커밋 과정 없이 현재 시각 기준으로 자동 커밋 메시지를 생성하여 스테이징 ➔ 커밋 ➔ 푸시를 한 번에 처리합니다. (물론 수동 커밋 및 단순 푸시 모드도 제공됩니다.)
* **🔄 다차원 브랜치 융합 (Reconciliation)**: 로컬과 깃허브의 커밋 내역이 다른(Diverged) 특수 상태 감지 시, **Merge, Rebase, Force Push, Reset**의 4가지 병합 액션을 제공하고, 충돌 발생 시 원클릭 되돌리기(`--abort`) 기능을 활성화해 안전한 병합을 유도합니다.
* **🖥️ 실시간 터미널 디버그 콘솔**: 하단에 배치된 어두운 테마의 실시간 터미널 콘솔을 통해 백엔드에서 수행되는 모든 Git 쉘 명령어(`git status`, `git pull` 등)의 실행 내용과 출력 결과(`stdout`/`stderr`)를 가공되지 않은 날것 그대로 완벽히 트래킹할 수 있습니다.
* **🚀 바로가기 및 편의성 기능**: `install.bat` 한 번으로 바탕화면에 무지개 옥토캣 로고가 적용된 앱 바로가기 실행 아이콘을 생성하며, 대시보드 내에서 로컬 폴더 주소를 누르면 Windows 파일 탐색기가 즉시 팝업되는 숏컷을 지원합니다.

---

## 💻 설치 및 준비사항 (Installation)

### 1. 요구 사항
* [Node.js](https://nodejs.org/) (v16.0.0 이상 권장)
* [Git](https://git-scm.com/) (시스템 환경 변수 `PATH` 등록 필수)

### 2. 설치 방법
1. 저장소를 클론하거나 프로젝트 파일을 내려받습니다.
2. 프로젝트 루트 폴더에 있는 **`install.bat`** 파일을 더블 클릭하여 실행합니다.
   * 필요한 라이브러리(`Express`)가 자동으로 설치됩니다.
   * 사용자의 바탕화면에 **`GitHub Local Manager`** 바로가기 실행 파일이 자동 생성됩니다.

---

## 🚀 사용 방법 (Usage)

1. 바탕화면에 생성된 **`GitHub Local Manager`** 바로가기를 더블 클릭하거나, 폴더 내의 `run.bat`를 더블 클릭하여 앱을 실행합니다.
2. 서버가 시작되면 기본 웹 브라우저가 자동으로 켜지며 대시보드 화면(`http://localhost:3000`)이 나타납니다.
   * *만약 `3000`번 포트가 다른 프로그램에 의해 사용 중인 경우, 서버가 에러 없이 다음 빈 포트(3001, 3002...)를 자동으로 찾아가 기동됩니다.*
3. 화면의 가이드에 따라 GitHub Personal Access Token (PAT)을 연동합니다. (`repo`, `user` 권한 필요)
4. 저장소 목록을 조회한 뒤, **[로컬 저장소 자동 탐색]** 버튼을 클릭해 컴퓨터 내부의 기존 Git 폴더들을 손쉽게 맵핑하여 사용하세요!

---

## 🛡️ 보안 안내 (Security)
* 사용자의 GitHub Personal Access Token (PAT)은 프로젝트 루트 폴더 내의 로컬 `config.json` 파일에만 텍스트 파일로 안전하게 캐싱됩니다. 
* 어떠한 외부 서버나 인터넷 망으로도 사용자의 토큰 정보가 유출되지 않으므로 안심하고 사용하셔도 좋습니다.

---

## 📄 라이선스 (License)
이 프로젝트는 MIT 라이선스에 따라 자유롭게 사용, 배포 및 수정할 수 있습니다.
