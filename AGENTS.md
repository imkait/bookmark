# 記事本網站（專案藍圖 / AGENTS.md）

> 本檔為跨 Agent 通用的專案說明書，遵循 AGENTS.md 開放標準——Claude Code、Codex、Gemini CLI 等都讀得懂。任何 Agent 開工前都應先讀本檔 + `handoff.md`。內容保持精簡，詳細內容放 `docs/decisions.md`、`CHANGELOG.md`、`.agent/`。

## 專案簡介
將網路上看到不錯的網站列表紀錄，建立一個記事本式的網站收藏與列表管理頁面。

## 技術棧與版本
HTML / CSS / JavaScript（純前端靜態頁面）

## 常用指令
<!-- 待補充 -->

## 三層邊界
- **永遠要做**：
  - 貼入網址時，先詢問要加到哪一個主題卡片，確認後才加入
- **要先問我**：
- **絕對不要做**：

## 目標與路線圖
- [x] 階段一：建立基礎頁面結構
- [x] 階段二：實作網站列表紀錄功能
- [ ] 階段三：優化與完善

## 資料夾結構
```
notehtml/
├── AGENTS.md
├── handoff.md
├── CHANGELOG.md
├── .gitignore
├── index.html
├── ai-game-dev.html
├── ai-agent-notes.html
├── ipas-ai-planner.html
├── ai-interactive-tutorial.html
├── asset-collection.html
├── skills-collection.html
├── docs/
│   └── decisions.md
└── .agent/
    └── _templates/
        ├── implementation_plan.template.md
        └── walkthrough.template.md
```

## Session 開始時必讀
每次開始新任務前，依序讀取：
1. `handoff.md`（上次做到哪、誰在哪台電腦、哪個 Agent 收工）
2. `CHANGELOG.md`（最近的變更歷史，摘要即可）
3. `docs/decisions.md`（過去的架構決策與取捨原因，摘要即可）
4. `.agent/` 底下最近 2-3 個任務資料夾（若任務與過去決策相關）

純文字修改、小型單檔調整可略過此步驟。

## 任務文件工作流程
只要任務符合以下任一情況，開始前必須先在 `.agent/<YYYY-MM-DD>_<task-slug>/` 建立 `implementation_plan.md`，**等待使用者審核或修正後才能開始執行**：
- 預期會修改 3 個以上檔案
- 涉及架構、資料庫結構、API 設計的變更
- 使用者明確要求「先規劃再做」

任務完成後，在同一資料夾寫 `walkthrough.md`（做了什麼、改了哪些檔案、怎麼驗證的）。範本在 `.agent/_templates/`。

單純的 bug 修復、格式調整、小型單檔修改可略過此流程，直接記一行進 `CHANGELOG.md` 即可。

## 收工紀律
收工（或 session 結束前）時：
1. 更新本檔「目標與路線圖」勾選進度
2. 改寫 `handoff.md`（整份重寫，不是往下堆）
3. `CHANGELOG.md` 補一行本次摘要
4. 若本次涉及架構或技術方案決策，`docs/decisions.md` 補一條（背景／決定／考慮過的替代方案／影響）
5. 若本次任務有開 `.agent/` 資料夾，確認 `walkthrough.md` 已寫完

## 工作約定
- 任何 Agent、任何電腦：**開工先讀 `handoff.md`，收工必更新 `handoff.md`**
- 修改共用檔案前先讀最新內容，避免覆蓋其他 Agent 的變更
- 所有回應與文件使用繁體中文
- 修改前先確認計畫，優先保留原有資料結構
