# Introduction to Git and GitHub

## Simple Interest Calculator

A calculator that calculates simple interest given principal, annual rate of interest and time period in years.

```
Input:
   p, principal amount
   t, time period in years
   r, annual rate of interest
Output
   simple interest = p*t*r
```

_© 2022 XYZ, Inc._


# Introduction to Git and GitHub - Git 與 GitHub 入門實驗室

這是 IBM 在 Coursera / edX 等平台上「Introduction to Git and GitHub」課程的配套實驗室儲存庫（Lab Repository）。  
它並非一個完整的 Web 應用程式，而是一個專門設計給初學者的**教學實驗室**，目的是透過實際操作來掌握版本控制的核心概念與 GitHub 協作流程。

## 專案核心主題

- 版本控制系統 (VCS)：學習 Git 的基礎邏輯與運作原理
- 分散式工作流：理解本地儲存庫 ↔ 遠端 GitHub 儲存庫的同步機制
- 分支管理 (Branching)：建立、切換分支，處理合併 (Merge) 與衝突 (Conflict) 解決
- 協作功能：Pull Requests (PR)、Forking 工作流、Issue 追蹤
- GitHub Pages：練習將靜態網頁部署到線上環境

## 支援的 HTTP 方法與主要功能

本專案並非 Web 應用，因此**沒有傳統的 HTTP API 路由**。  
Git 的操作主要透過 Git 協定（底層使用 HTTPS 或 SSH）進行，映射到常見動作如下：

- **GET**：對應 `git clone`、`git pull`、瀏覽 GitHub 網頁介面讀取檔案/歷史
- **POST / PUT**：對應 `git push`（推送變更）、建立 Pull Request、更新遠端分支
- **主要功能重點**：程式碼的版本追蹤、歷史記錄、分支合併、團隊協作同步，而非實作後端路由

**典型 Git 工作流（本實驗室重點練習內容）**

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
- GitHub 帳號（免費即可）
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

