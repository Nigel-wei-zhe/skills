# skills

個人 Claude Code Skills 庫，透過 [skills CLI](https://github.com/vercel-labs/skills) 安裝至本地開發環境。

## 安裝方式

```bash
# 安裝此 repo 所有 skills
npx skills add Nigel-wei-zhe/skills

# 安裝單一 skill（依資料夾路徑）
npx skills add Nigel-wei-zhe/skills/dev/skill-name
```

## Skills 列表

| Skill | 說明 | 類別 |
|-------|------|------|
| _(暫無)_ | | |

## 目錄結構

```
skills/
├── README.md
└── skills/
    ├── .curated/     # 精選、穩定的 skills
    ├── .experimental/ # 實驗性 skills
    ├── dev/          # 開發工具類
    ├── content/      # 內容創作類
    ├── ops/          # 維運自動化類
    └── utils/        # 通用工具類
```

## 開發規範

每個 skill 為一個 `SKILL.md` 檔案，包含 YAML frontmatter：

```markdown
---
name: skill-name
description: 一句話說明此 skill 的用途與觸發時機
---

# Skill 內容

指令說明與執行步驟...
```

### 命名規則

- 資料夾與檔名使用 `kebab-case`
- 每個 skill 單獨一個資料夾，內含 `SKILL.md`
- `description` 須清楚說明觸發條件，讓模型能自動判斷何時使用

## 授權

MIT
