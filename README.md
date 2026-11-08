# SEO Audit Reports — carolkao-fin

自動化 SEO 稽核報告庫，由 `/seo-report` skill 自動執行並匯入。

## 資料夾結構

```
audits/
  seo_YYYYMMDD/
    seo-audit-report-zh.html   # 中文互動式 HTML 報告
    seo-audit-report-en.html   # 英文互動式 HTML 報告
    SEO報告_<網站名>.docx       # 中文 Word 報告
    SEO_Report_<Name>_EN.docx  # 英文 Word 報告
    audit-info.json            # 稽核摘要（分數、發現數量、URL）
```

## 稽核記錄

| 資料夾 | 網站 | 分數 | 嚴重 | 高 | 中 | 低 | 互動報告 |
|--------|------|------|------|----|----|----|----------|
| [seo_20261108](audits/seo_20261108/) | startup.sme.gov.tw/sitaiwan/ 社會創新平台 | 23/100 | 6 | 7 | 6 | 4 | [中文](https://claude.ai/artifact/5FugDxSgRAn2PmV5mqeUVy) · [EN](https://claude.ai/artifact/KYk9rYp4EKChwdeopiRDXn) |

## 使用方式

在 Claude Code 中輸入：

```
/seo-report https://example.com
```

Skill 會自動：
1. 執行完整 SEO 稽核（含流量策略建議）
2. 生成**中文**互動式 HTML 報告（`seo-audit-report-zh.html`）
3. 生成**英文**互動式 HTML 報告（`seo-audit-report-en.html`）
4. 生成中文 Word 報告
5. 生成英文 Word 報告
6. 建立 `audits/seo_YYYYMMDD/` 資料夾
7. Commit 並 push 到本 repo
