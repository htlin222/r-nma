# AI 輔助網絡統合分析教學

Network Meta-analysis with R 課程專案

## 專案結構

```
r-nma/
├── _quarto.yml      # Quarto 設定檔
├── index.qmd        # 網頁版主內容
├── slides.qmd       # 簡報版內容
├── README.md        # 專案說明
└── CLAUDE.md        # AI 輔助說明
```

## 課程架構

10 個學習任務：

1. 基本概念（直接/間接證據）
2. 網絡幾何（Network Geometry）
3. 網絡統合分析執行
4. 一致性評估（Consistency）
5. 異質性評估（Heterogeneity）
6. 排名分析（P-score/SUCRA）
7. 次群體分析與網絡統合迴歸
8. 發表偏誤評估
9. 敏感度分析
10. 學術報告撰寫（PRISMA-NMA）

## 相依套件

```r
install.packages(c("netmeta", "meta", "dplyr"))
```

## 開發指令

```bash
# 預覽
quarto preview

# 渲染
quarto render
```

## 參考專案

<https://github.com/htlin222/r-meta>
