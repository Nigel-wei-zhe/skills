# skills

個人 Skills 庫， 安裝至本地開發環境。

## 安裝方式

```bash
# 安裝此 repo 所有 skills
npx skills add https://github.com/Nigel-wei-zhe/skills

# 安裝單一 skill（依資料夾路徑）
npx skills add https://github.com/Nigel-wei-zhe/skills/tree/main/skills/<category>/<skill-name>
```

## Skills 列表

完整列表見 [skills.json](skills.json)。

## 目錄結構

```
skills/
├── README.md
└── skills/
    ├── curated/      # 精選、穩定的 skills
    ├── experimental/ # 實驗性 skills
    ├── dev/          # 開發工具類
    ├── content/      # 內容創作類
    ├── ops/          # 維運自動化類
    └── utils/        # 通用工具類
```

# Skill 內容

```

### 命名規則

- 資料夾與檔名使用 `kebab-case`
- 每個 skill 單獨一個資料夾，內含 `SKILL.md`

## 注意事項

- **敏感資訊勿上傳**：Token、帳號、URL 等私密設定請自行維護，並存於本地像是 `.claude/settings.local.json`（已 gitignore），SKILL.md 內只寫變數名稱
- **設定檔有作用域**：僅在本專案目錄下執行 LLM 時才會載入，從其他專案呼叫不會套用本 repo 的設定檔

```
