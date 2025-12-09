# CourseForge - Data Science Course Generator Agent

一個專門生成「任務導向式 Data Science 課程」的 AI Agent。

## 快速使用

在 Claude Code 中執行：

```bash
/course Survival Analysis
/course "Propensity Score Matching" --scenario "比較微創與傳統手術"
/course "Machine Learning Classification" --lang python
```

## Agent 架構

```
course-agent/
├── README.md           # 本說明文件
├── AGENT.md            # Agent 設計規格
├── SYSTEM_PROMPT.md    # 完整系統提示詞
└── ~/.claude/commands/course.md  # Slash command
```

## 課程設計哲學

### 四大原則

| 原則         | 說明                 | 實踐方式              |
| ------------ | -------------------- | --------------------- |
| **任務導向** | 每個任務 = 一個技能  | 10 個獨立但連貫的任務 |
| **情境模擬** | 貫穿全課程的研究情境 | 模擬真實資料結構      |
| **漸進學習** | 概念 → 技術 → 整合   | 20-40-20-20 時間分配  |
| **即學即用** | 可直接執行的程式碼   | 含替換指引與寫作範例  |

### 標準課程結構

```
Phase 1: Foundation (20%)
├── 任務 1: 概念導論
└── 任務 2: 資料準備

Phase 2: Core Skills (40%)
├── 任務 3: 核心方法 I
├── 任務 4: 核心方法 II
├── 任務 5: 結果視覺化
└── 任務 6: 結果解讀

Phase 3: Advanced (20%)
├── 任務 7: 進階分析 I
└── 任務 8: 進階分析 II

Phase 4: Synthesis (20%)
├── 任務 9: 品質評估
└── 任務 10: 學術報告
```

## 支援主題

### 統計方法

| 主題                  | R 套件              | 產出              |
| --------------------- | ------------------- | ----------------- |
| Meta-analysis         | meta, metafor       | 森林圖、漏斗圖    |
| Network Meta-analysis | netmeta             | 網絡圖、排名      |
| Survival Analysis     | survival, survminer | KM 曲線、Cox 模型 |
| Propensity Score      | MatchIt, cobalt     | Love plot、ATT    |
| Bayesian Analysis     | brms, rstanarm      | 後驗分布、MCMC    |

### 機器學習

| 主題           | R 套件     | 產出               |
| -------------- | ---------- | ------------------ |
| Classification | tidymodels | ROC、混淆矩陣      |
| Regression     | tidymodels | 殘差圖、特徵重要性 |
| Clustering     | factoextra | 輪廓圖、PCA        |
| Time Series    | forecast   | ARIMA、預測圖      |

### 因果推論

| 主題         | R 套件         | 產出         |
| ------------ | -------------- | ------------ |
| DAG Analysis | dagitty, ggdag | 因果圖       |
| DiD          | fixest         | 平行趨勢圖   |
| IV           | ivreg          | 工具變數診斷 |

## 每個任務的 5 個必要元素

```markdown
# 任務 N：[名稱]

## 1. 學習目標

- 用動詞開頭
- 可被驗證

## 2. 概念說明

::: {.callout-tip}

## 比喻

生活化的類比
:::

## 3. 程式碼實作

完整可執行的程式碼

## 4. 結果解讀

解讀標準表格

## 5. 學術寫作範例

英文寫作模板
```

## 輸出檔案

Agent 會生成完整的 Quarto 專案：

```
{topic}-course/
├── _quarto.yml       # 網站設定
├── index.qmd         # 網頁版（完整 10 任務）
├── slides.qmd        # 簡報版（RevealJS）
├── README.md         # 專案說明
└── CLAUDE.md         # AI 輔助指引
```

## 品質保證

每個課程結尾包含三階段檢核清單：

- [ ] **準備階段**：研究問題、納入標準、資料品質
- [ ] **分析階段**：方法選擇、主要分析、敏感度分析
- [ ] **報告階段**：報告指引、圖表、學術寫作

## 擴展方向

- [ ] Python 版本支援（pandas, scikit-learn）
- [ ] Jupyter Notebook 輸出格式
- [ ] 互動式 Shiny/Observable 元素
- [ ] 多語言支援（英文版課程）
- [ ] 自動化測驗題生成

## 相關專案

- [r-meta](https://github.com/htlin222/r-meta) - Meta-analysis 課程範本
- [r-nma](https://github.com/htlin222/r-nma) - Network Meta-analysis 課程範本
