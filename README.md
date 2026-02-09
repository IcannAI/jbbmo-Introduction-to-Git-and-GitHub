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


## 專案核心主題 (Core Topics)
版本控制系統 (VCS)：學習 Git 的基礎邏輯。

分散式工作流：理解本地儲存庫與遠端 (GitHub) 儲存庫的同步。

分支管理 (Branching)：建立、切換分支以及處理合併 (Merge) 與衝突 (Conflict)。

協作功能：Pull Requests (PR)、Forking 以及 Issue 追蹤。

GitHub Pages：練習如何將靜態網頁部署至線上環境。

## 支援的 HTTP 方法與主要功能
由於這是 Git 練習，它主要透過 Git 協定（底層封裝於 HTTPS 或 SSH）進行操作：

GET：用於 git clone 或瀏覽 GitHub 網頁介面讀取原始碼。

POST/PUT：對應於 git push（將本地變更上傳至伺服器）或建立新的 Pull Request。

功能重點：並非實作 API 路由，而是實作 程式碼的版本追蹤與團隊同步。

## Workflow (Git 工作流)
Fork：將原始專案複製到自己的 GitHub 帳號下。

Clone：將專案下載至本地環境。

Branch：建立特徵分支 (Feature Branch) 進行修改。

Stage & Commit：將修改標記並存入本地紀錄。

Push：將更動推送回雲端。

Pull Request：請求將變更合併回主幹。

## API 路由總覽
無內部 API 路由：本專案不包含 Express 或 Flask 等後端路由。

外部 API 應用：實作中會接觸到 GitHub 的 REST API 概念（例如當你透過介面點擊「Merge」時，實際上是觸發了 GitHub 的 API）。

## 環境需求
* Git Bash / Terminal：必備的命令列工具。

* GitHub 帳號：用於練習遠端操作。

* 文字編輯器：如 VS Code，用於修改練習用的 HTML/Markdown 檔案。

## 複製專案 (Cloning)
在終端機輸入：

Bash
```git clone https://github.com/[Username]/jbbmo-Introduction-to-Git-and-GitHub.git```

### Installation
此專案不需要安裝特定的程式語言套件（如 npm install），它更像是一個文檔與腳本的集散地。主要的安裝步驟是 Git 的安裝與配置：

Bash
git config --global user.name "Name"
git config --global user.email "xxx@email.com"
#### 啟動開發伺服器
#### 本專案通常不包含動態伺服器。
#### 若包含簡單的 HTML，可使用 VS Code 的 Live Server 擴充功能預覽。

## Structure (專案結構)
* README.md：實驗指南。

* sample_files/：供練習用的 HTML 或純文字檔。

* .git/（隱藏）：儲存所有版本歷史的核心目錄。

## 應用方向
* DevOps 基礎：所有 CI/CD 流程的起點。

* 開源貢獻：學習如何參與開源社群。

* 團隊協作標準：建立企業內部開發規範。

## MVP 方向 
* 自動化部署腳本：建立一個利用 Git Hooks 在 Push 時自動更新伺服器的 MVP。

* 個人作品集平台：利用專案中提到的 GitHub Pages 技術，快速上線個人靜態網站。

* 文件管理系統：利用 Git 的版本特性，管理法律合約或技術文件的修訂版本。

## Tool (工具棧)
* Git (核心工具)

* GitHub (雲端平台)

* Markdown (文件撰寫語言)

## Key Takeaways
* 錯誤不可怕：Git 的強大在於能夠隨時「回到過去」(Reset/Revert)。

* 原子化提交 (Atomic Commits)：學會將小的改動分開 Commit，有助於除錯。

* 協作邏輯：理解「先 Pull 後 Push」是避免衝突的黃金準則。
