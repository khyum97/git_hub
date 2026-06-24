<p align="center">
  <img src="./github-rainbow.png" width="180" alt="GitHub Local Manager Logo" />
</p>

<h1 align="center">GitHub Local Manager (GLM)</h1>

<p align="center">
  로컬 Git 저장소들과 GitHub 원격 저장소를 직관적으로 매핑하고, 복잡한 Git 조작을 한곳에서 쉽고 빠르게 실행하는 프리미엄 로컬 웹앱 대시보드입니다.
</p>

<p align="center">
  <a href="#korean">🇰🇷 한국어</a> | 
  <a href="#english">🇺🇸 English</a> | 
  <a href="#japanese">🇯🇵 日本語</a> | 
  <a href="#chinese">🇨🇳 简体中文</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js Badge" />
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" alt="Express Badge" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git Badge" />
  <img src="https://img.shields.io/badge/Windows-0078D6?style=flat-square&logo=windows&logoColor=white" alt="Windows OS" />
</p>

---

<div id="korean"></div>

## 🇰🇷 한국어 가이드

### 🌟 주요 기능
* **🔑 자동 로그인 및 토큰 연동**: GitHub Personal Access Token (PAT)을 1회 연동하면 로컬 보안 캐싱을 통해 이후 앱 실행 시 자동으로 로그인되어 바로 대시보드로 진입합니다.
* **📂 로컬 저장소 원클릭 자동 탐색**: 컴퓨터 내부(C, D, E드라이브 핵심 경로)를 깊이 3까지 고속 스캔하여 GitHub과 연결된 모든 로컬 Git 폴더를 감지해 자동으로 연동합니다.
* **📦 원클릭 클론 & 수동 연동**: 윈도우 네이티브 폴더 브라우저 창(`FolderBrowserDialog`)을 통해 기존 로컬 프로젝트 폴더를 바로 맵핑하거나, 원격 리포지토리를 새 폴더에 깔끔하게 클론할 수 있습니다.
* **⚡ 스마트 푸시 & 자동 커밋**: 번거로운 커밋 과정 없이 현재 시각 기준으로 자동 커밋 메시지를 생성하여 스테이징 ➔ 커밋 ➔ 푸시를 한 번에 처리합니다. (수동 커밋 및 단순 푸시 모드도 제공됩니다.)
* **🔄 다차원 브랜치 융합 (Reconciliation)**: 로컬과 깃허브의 커밋 내역이 다른(Diverged) 특수 상태 감지 시, **Merge, Rebase, Force Push, Reset**의 4가지 병합 액션을 제공하고, 충돌 발생 시 원클릭 되돌리기(`--abort`) 기능을 활성화해 안전한 병합을 유도합니다.
* **🖥️ 실시간 터미널 디버그 콘솔**: 백엔드에서 수행되는 모든 Git 쉘 명령어의 실행 내용과 출력 결과(`stdout`/`stderr`)를 어두운 테마의 실시간 터미널 콘솔을 통해 실시간으로 완벽히 트래킹할 수 있습니다.
* **🚀 바로가기 및 편의성 기능**: `install.bat` 한 번으로 바탕화면에 무지개 옥토캣 로고가 적용된 앱 바로가기 실행 아이콘을 생성하며, 대시보드 내에서 로컬 폴더 주소를 누르면 Windows 파일 탐색기가 즉시 팝업되는 숏컷을 지원합니다.

### 💻 설치 및 준비사항
* **요구 사항**: Node.js (v16.0.0 이상 권장), Git (시스템 환경 변수 `PATH` 등록 필수)
* **설치 방법**:
  1. 저장소를 클론하거나 프로젝트 파일을 내려받습니다.
  2. 프로젝트 루트 폴더에 있는 **`install.bat`** 파일을 더블 클릭하여 실행합니다. (Express 의존성 라이브러리가 자동 설치되고 바탕화면에 바로가기 실행 아이콘이 자동 생성됩니다.)

### 🚀 사용 방법
1. 바탕화면에 생성된 **`GitHub Local Manager`** 바로가기를 더블 클릭하거나, 폴더 내의 `run.bat`를 더블 클릭하여 앱을 실행합니다. (자동으로 브라우저 대시보드 `http://localhost:3000`가 켜집니다.)
2. 최초 실행 시 GitHub Personal Access Token (PAT)을 연동합니다. (`repo`, `user` 권한 필요)
3. **[로컬 저장소 자동 탐색]** 버튼을 클릭해 컴퓨터 내부의 기존 Git 폴더들을 손쉽게 맵핑하여 사용하세요!

---

<div id="english"></div>

## 🇺🇸 English Guide

### 🌟 Key Features
* **🔑 Token Auto-Login**: Link your GitHub Personal Access Token (PAT) once, and secure local caching handles authentication automatically on subsequent launches.
* **📂 One-Click Local Repository Scan**: Scan key paths on your C, D, and E drives up to 3 levels deep to automatically detect and link all local Git repositories configured with GitHub remotes.
* **📦 One-Click Clone & Manual Connect**: Directly map existing local directories or clone remote repositories cleanly into new target paths using native Windows Folder Browser dialogs.
* **⚡ Smart Commit & Push**: Skip the manual commit flow. Generates an auto-commit message containing the current timestamp to Stage ➔ Commit ➔ Push in one click. (Manual commit message entry and standard Push-only modes are also supported.)
* **🔄 Branch Reconciliation**: When local and remote commit histories diverge, GLM offers four actions: **Merge, Rebase, Force Push, and Reset**. In case of merge conflicts, an one-click abort (`--abort`) function becomes dynamically available to roll back safely.
* **🖥️ Real-Time Debug Console**: Monitor all underlying Git shell commands and terminal outputs (`stdout`/`stderr`) in real-time through the built-in dark theme log panel.
* **🚀 Shortcuts & Integrations**: Run `install.bat` once to automatically create a desktop shortcut with a custom rainbow Octocat logo. Clicking a repository's local path on the dashboard immediately opens the Windows File Explorer at that directory.

### 💻 Installation & Requirements
* **Requirements**: Node.js (v16.0.0+ recommended), Git (Must be added to system environment `PATH`)
* **Installation**:
  1. Clone this repository or download the project files.
  2. Double-click **`install.bat`** in the project root directory. (Installs dependencies and creates the desktop shortcut automatically.)

### 🚀 Usage
1. Double-click the **`GitHub Local Manager`** shortcut on your Desktop or run `run.bat` in the project folder to start the backend server (Automatically opens `http://localhost:3000` in your default browser).
2. For the first-time setup, paste your GitHub Personal Access Token (PAT) with `repo` and `user` scopes.
3. Click the **[로컬 저장소 자동 탐색] (Auto Scan Local Repos)** button to scan and map all your pre-existing Git repositories automatically.

---

<div id="japanese"></div>

## 🇯🇵 日本語ガイド

### 🌟 主な機能
* **🔑 トークン自動ログイン**: 初回にGitHubの個人アクセストークン（PAT）を連携すると、ローカルに安全にキャッシュされ、次回以降の起動時には自動ログインして即座にダッシュボードへ遷移します。
* **📂 ワンクリック・ローカルリポジトリ自動スキャン**: C、D、Eドライブなどの主要ディレクトリを深さ3レベルまで高速スキャンし、GitHubと連携されているすべてのローカルGitフォルダを自動検出して一括マッピングします。
* **📦 ワンクリッククローン＆手動連携**: Windowsネイティブのフォルダ選択ダイアログを使用し、既存のローカルプロジェクトを簡単に関連付けたり、リモートリポジトリを新規ディレクトリにクローンしたりできます。
* **⚡ スマートプッシュ＆自動コミット**: 手動コミット作業をスキップし、現在時刻に基づいたコミットメッセージを自動生成して、ステージング ➔ コミット ➔ プッシュまでをワンクリックで実行します。（手動コミットと単純プッシュのみのモードも対応可能）。
* **🔄 ブランチの不一致・融合管理（Reconciliation）**: ローカルとGitHubの履歴が食い違っている（Diverged）場合に、**Merge, Rebase, Force Push, Reset**の4つの操作を提供。競合（Conflict）発生時には、動的に有効化されるキャンセルボタン（`--abort`）で安全な状態にロールバックできます。
* **🖥️ リアルタイム・デバッグコンソール**: バックエンドで実行されているすべてのGitコマンドとその標準出力・エラー出力（`stdout`/`stderr`）を、内蔵のダークテーマログパネルからリアルタイムに監視できます。
* **🚀 デスクトップショートカット＆エクスプローラー連携**: `install.bat`を実行するだけで、デスクトップに虹色のオクトキャットロゴが適用された起動ショートカットを作成します。また、ダッシュボード上のパスをクリックすると、Windowsエクスプローラーでそのフォルダを即座に開くことができます。

### 💻 インストールと準備
* **システム要件**: Node.js (v16.0.0以上推奨), Git (環境変数 `PATH` に登録済みであること)
* **インストール手順**:
  1. このリポジトリをクローンするか、プロジェクトファイルをダウンロードします。
  2. プロジェクトのルートフォルダにある **`install.bat`** をダブルクリックして実行します。（依存ライブラリが自動インストールされ、デスクトップにショートカットアイコンが生成されます。）

### 🚀 使用方法
1. デスクトップの **`GitHub Local Manager`** ショートカットをダブルクリックするか、フォルダ内の `run.bat` をダブルクリックしてサーバーを起動します。（ブラウザで `http://localhost:3000` が自動的に開きます。）
2. 初回起動時に、`repo` と `user` 権限を持つGitHub個人アクセストークン（PAT）を入力します。
3. **[로컬 저장소 자동 탐색] (ローカル自動スキャン)** ボタンをクリックして、コンピューター内部の既存のGitリポジトリを簡単にマッピングして使用開始してください！

---

<div id="chinese"></div>

## 🇨🇳 简体中文指南

### 🌟 核心功能
* **🔑 令牌自动登录**: 首次绑定 GitHub 个人访问令牌 (PAT) 后，本地安全缓存将实现后续启动时的免密自动登录，直达控制面板。
* **📂 一键扫描本地仓库**: 自动高速扫描 C、D、E 盘等主要路径（最大深度 3 层），智能识别并一键绑定所有已关联 GitHub 远程仓库的本地 Git 文件夹。
* **📦 一键克隆与手动关联**: 采用 Windows 原生文件夹浏览器窗口，直接关联现有的本地项目文件夹，或将远程仓库干净地克隆到新的目标路径中。
* **⚡ 智能推送与自动提交**: 免去繁琐的提交步骤，自动生成包含当前时间戳的提交信息，一键完成 暂存 ➔ 提交 ➔ 推送。（同时也支持手动输入提交信息和纯推送模式。）
* **🔄 分支历史融合（冲突恢复）**: 当本地和远程的提交历史不一致（Diverged）时，提供 **Merge（合并）、Rebase（变基）、Force Push（强推）和 Reset（重置）** 四种融合方案。如果发生冲突，可一键取消（`--abort`）以安全恢复状态。
* **🖥️ 实时终端调试控制台**: 通过内置的黑色主题日志面板，实时跟踪后端执行的所有底层 Git 脚本命令以及输出结果（`stdout`/`stderr`）。
* **🚀 快捷桌面图标与管理器联动**: 运行 `install.bat` 即可在桌面上自动生成带有定制彩虹 GitHub 八爪猫标志的快捷启动图标。在面板中点击本地路径，将立即唤起 Windows 文件资源管理器打开对应文件夹。

### 💻 安装与系统要求
* **系统要求**: Node.js (推荐 v16.0.0 及以上版本), Git (必须配置到系统环境变量 `PATH` 中)
* **安装步骤**:
  1. 克隆此仓库或下载项目压缩包。
  2. 双击项目根目录下的 **`install.bat`**。 (此操作将自动安装依赖项并创建桌面快捷方式。)

### 🚀 使用说明
1. 双击桌面上的 **`GitHub Local Manager`** 快捷方式，或双击文件夹内的 `run.bat` 启动服务 (默认浏览器将自动打开 `http://localhost:3000`)。
2. 首次运行需要输入具有 `repo` 和 `user` 权限的 GitHub 个人访问令牌 (PAT)。
3. 点击 **[로컬 저장소 자동 탐색] (自动扫描本地仓库)** 按钮，将您电脑里已有的 Git 项目一键映射至大屏，开始轻松管理！
