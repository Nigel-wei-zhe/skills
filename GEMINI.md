# Skills Repo — Agent Instructions

> **Sync rule**: AGENTS.md · CLAUDE.md · GEMINI.md 內容永遠保持一致。  
> 任何異動這三個檔案時，必須同步更新其餘兩個。  
> 任何新增或修改 SKILL.md 時，必須同步更新 `skills.json`。

## 專案概覽

個人 Claude Code / Cursor / Gemini CLI Skills 庫。  
透過 `npx skills add https://github.com/Nigel-wei-zhe/skills` 安裝至任意專案。

## 目錄結構

```
skills/
├── AGENTS.md / CLAUDE.md / GEMINI.md   ← 本檔（三份內容同步）
├── skills.json                          ← Skills 登錄表（主要維護對象）
├── README.md                            ← 對外說明
└── skills/
    ├── curated/       精選、穩定
    ├── experimental/  實驗性
    ├── dev/           開發工具
    ├── content/       內容創作
    ├── ops/           維運自動化
    └── utils/         通用工具
```

每個 skill 為獨立資料夾，內含一個 `SKILL.md`：
```
skills/dev/my-skill/
└── SKILL.md
```


## 維護規範

### 新增 skill
1. 在對應類別目錄建立資料夾與 `SKILL.md`
2. 在 `skills.json` 的 `skills` 陣列新增一筆 `{ name, description, category, path }`

### 異動 agent 說明檔
修改本檔後，立即同步 AGENTS.md 與 GEMINI.md（內容完全一致）。

### 類別選擇
| 類別 | 適用情境 |
|------|---------|
| `curated` | 經過驗證、長期維護的核心 skills |
| `experimental` | 測試中，API 可能異動 |
| `dev` | 程式開發流程（PR、review、debug） |
| `content` | 文章撰寫、文件、部落格 |
| `ops` | CI/CD、部署、監控 |
| `utils` | 跨類別通用工具 |
