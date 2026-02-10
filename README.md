# Introduction to Git and GitHub - Git 與 GitHub 入門實驗室

這是 IBM 在 Courseran Introduction to Git and GitHub課程的Lab Repository。  
目的是透過實際操作來掌握版本控制的核心概念與 GitHub 協作流程。

## 專案核心主題
- 版本控制系統 (VCS)：學習 Git 的邏輯與運作原理
- 分散式工作流：理解本地儲存庫 ↔ 遠端 GitHub 儲存庫的同步機制
- 分支管理 (Branching)：建立、切換分支，處理Merge與衝突Conflict解決
- 協作功能：Pull Requests (PR)、Forking 工作流、Issue 追蹤
- GitHub Pages：練習將靜態網頁部署到線上環境

## 支援的 HTTP 方法與主要功能
本專案並非 Web 應用，因此**沒有傳統的 HTTP API 路由**。  
Git 的操作主要透過 Git 協定（底層使用 HTTPS 或 SSH）進行，映射動作如下：

- **GET**：對應 `git clone`、`git pull`、瀏覽 GitHub 網頁介面讀取檔案/歷史
- **POST / PUT**：對應 `git push`（推送變更）、建立 Pull Request、更新遠端分支
- **主要功能重點**：程式碼的版本追蹤、歷史記錄、分支合併、團隊協作同步，而非實作後端路由

**常見Git工作流**
1. Fork → 將課程專案複製到自己帳號
2. Clone → 下載到本地
3. Branch → 建立特徵分支進行修改
4. Stage & Commit → 標記變更並建立提交紀錄
5. Push → 推送至遠端
6. Pull Request → 提出合併請求

## API 路由總覽

- **無內部 API 路由**：本專案不包含任何 Express、Flask 或其他後端框架的路由
- **外部 API 概念**：透過 GitHub 網頁介面操作（如點擊 Merge、建立 Issue）時，實際上是呼叫 GitHub REST API，但初學者無需直接撰寫 API 呼叫

## 環境需求

- Git（命令列工具）：Windows → Git Bash / macOS & Linux → 內建 Terminal
- GitHub 帳號
- 文字編輯器：強烈推薦 **Visual Studio Code**（內建 Git 支援與 Live Server 擴充功能）
- 瀏覽器：用於操作 GitHub 網頁介面與查看 GitHub Pages

## 複製專案 (Cloning)

### 先在 GitHub 上 Fork 本專案到你的帳號
### 然後 Clone 你自己 Fork 的版本（請替換 Your_Username）
```git clone https://github.com/Your_Username/jbbmo-Introduction-to-Git-and-GitHub.git```

```cd jbbmo-Introduction-to-Git-and-GitHub```

## Installation
### 本專案無需安裝任何套件（沒有 package.json 或 requirements.txt）。
### 只需完成 Git 基本設定：
```git config --global user.name "你的名字"```
```git config --global user.email "你的email@example.com"```

### 啟動開發伺服器

* 本專案沒有後端伺服器需要啟動
* 包含 HTML/Markdown 檔案，可使用以下方式預覽：VS Code 安裝 Live Server 擴充功能 → 右鍵 HTML 檔案 → Open with Live Server
或使用 Python 內建伺服器：
```python -m http.server 8000```
#### 然後瀏覽 http://localhost:8000

## Structure

*README.md       # 實驗文件指南
*instructions/   ＃ 各Lab的操作說明
*sample_files/   ＃ 練習用的範例檔案（HTML、txt、md等）
*.gitignore     ＃ 忽略不需提交的檔案
*.git/           ＃（隱藏資料夾）Git 版本歷史核心

## 應用方向
DevOps 基礎：所有 CI/CD、自動化部署的起點
開源貢獻：學習 Fork → PR → 參與開源專案的標準流程
團隊協作規範：企業內部程式碼管理、文件版本控制標準
**個人作品集與部落格：用GitHub Pages快速上線靜態網站**

## MVP 方向 
雖然本專案本身不是應用框架，但可發展：
＊ 個人靜態作品集網站（GitHub Pages + 自訂域名）
＊ 文件版本管理系統（合約、規格書、課程筆記的修訂歷史）
＊ 自動化部署小工具（Git Hooks + 簡單腳本，在 push 時更新伺服器）
＊ 團隊知識庫原型（Markdown 文件 + GitHub Wiki / Pages）

## Tool 
＊ Git：版本控制核心工具
＊ GitHub：遠端託管、協作平台、Pages 靜態託管
＊ Markdown：撰寫文件、README、課程筆記
＊ VS Code：內建 Git 圖形介面、Live Server、Markdown 預覽

## Key takeaways
* Git 可隨時回到前一個版本（reset、revert、checkout）
* 小的、單一目的的 commit 最容易追蹤與除錯
* **協作黃金準則：先 pull / fetch 再 push，大幅降低衝突機率**
* 分支是免費的：多用 feature branch，不怕把 main 搞壞
* **版本控制**
