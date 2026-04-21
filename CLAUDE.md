# Skills Repo — Agent Instructions

> **Sync rule**: AGENTS.md · CLAUDE.md · GEMINI.md 內容永遠保持一致。  
> 任何異動這三個檔案時，必須同步更新其餘兩個。  
> 任何新增或修改 SKILL.md 時，必須同步更新 README.md 的 Skills 列表。

## 專案概覽

個人 Claude Code / Cursor / Gemini CLI Skills 庫。  
透過 `npx skills add Nigel-wei-zhe/skills` 安裝至任意專案。

## 目錄結構

```
skills/
├── AGENTS.md / CLAUDE.md / GEMINI.md   ← 本檔（三份內容同步）
├── README.md                            ← 對外說明，含 Skills 列表
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

## SKILL.md 撰寫原則：Progressive Disclosure

以「由淺入深、按需展開」四層結構撰寫，避免一次揭露所有細節：

```markdown
---
name: skill-name
description: 一句話觸發條件 — 何時使用、解決什麼問題
---

<!-- Layer 1 · 摘要（必讀，≤3 行） -->
## TL;DR
最常見用法的一行指令或步驟。

<!-- Layer 2 · 標準流程（多數情境適用） -->
## 使用方式
基本步驟，涵蓋 80% 場景。

<!-- Layer 3 · 進階選項（需要時再看） -->
## 進階

<details>
<summary>選項 / 參數</summary>

詳細參數說明。

</details>

<!-- Layer 4 · 邊界條件（僅特殊情況需要） -->
## 注意事項
已知限制、常見錯誤、回退方案。
```

**原則摘要：**
- `description` 必須讓模型能自動判斷觸發時機
- TL;DR 讓人 10 秒內上手
- 進階內容用 `<details>` 折疊，不干擾主流程
- 每層獨立可讀，不依賴上一層的細節

## 維護規範

### 新增 skill
1. 在對應類別目錄建立資料夾與 `SKILL.md`
2. 更新 `README.md` 的 Skills 列表表格

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
