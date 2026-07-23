# 記事本網站

> 收藏與整理優質網站資源的記事本式網站

## 功能特色

| 功能       | 說明                                              |
| ---------- | ------------------------------------------------- |
| 主題分類   | 五大主題卡片，依類別收錄網站資源                  |
| 子分類機制 | 素材蒐集頁支援子分類（Github 專案、AI 3D 建模等） |
| 響應式設計 | Bootstrap 5.3.3，支援桌面與行動裝置               |
| 快速收錄   | 貼入網址後由 Agent 詢問分類並加入對應頁面         |
| 一頁式總覽 | 首頁卡片式導覽，點入即見該主題所有資源            |

## 主題頁面

| 頁面               | 檔案                             | 說明                                  |
| ------------------ | -------------------------------- | ------------------------------------- |
| AI 遊戲製作        | `ai-game-dev.html`             | AI 輔助遊戲開發的工具、教程與資源     |
| AI Agent 筆記      | `ai-agent-notes.html`          | AI Agent 開發筆記、框架比較與實作紀錄 |
| iPAS AI 應用規劃師 | `ipas-ai-planner.html`         | iPAS 認證準備、題庫與學習資源         |
| AI 互動教學網頁    | `ai-interactive-tutorial.html` | AI 互動式教學網站、線上課程與學習平台 |
| 素材蒐集           | `asset-collection.html`        | 圖片、音效、模型、字型等開發素材資源  |

## 技術棧

| 技術       | 版本  | 用途             |
| ---------- | ----- | ---------------- |
| HTML       | 5     | 頁面結構         |
| CSS        | 3     | 樣式與響應式佈局 |
| JavaScript | ES6+  | 陣列資料渲染     |
| Bootstrap  | 5.3.3 | UI 框架          |

## 專案結構

```
notehtml/
├── index.html              # 首頁（主題卡片總覽）
├── ai-game-dev.html        # AI 遊戲製作
├── ai-agent-notes.html     # AI Agent 筆記
├── ipas-ai-planner.html    # iPAS AI 應用規劃師
├── ai-interactive-tutorial.html  # AI 互動教學網頁
├── asset-collection.html   # 素材蒐集
├── AGENTS.md               # 專案藍圖（AI Agent 協作規範）
├── handoff.md              # 交接檔
├── CHANGELOG.md            # 變更歷史
├── docs/
│   └── decisions.md        # 架構決策紀錄
└── .agent/                 # 任務文件資料夾
```

## License

本專案為個人學習資源收藏，未設定特定授權條款。
