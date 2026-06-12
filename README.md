# GA4 / GSC Analytics Dashboard — Demo（展示用）

這個資料夾是一份 **GA4 + Google Search Console 分析儀表板的展示／作品集版本**，
獨立的 GitHub Pages repo（`GA-Dashboard`），與主專案分開發布。

> ⚠️ **展示用：頁面上所有數字、頁面名稱、品牌名稱、排名都是「虛構／脫敏」的**，
> 僅供作品集 / 面試展示，不代表任何真實企業的數據。

## 線上 Live
https://jason0308p.github.io/GA-Dashboard/

- `dashboard.html` / `dashboard_en.html` — 主儀表板（中 / 英）
- `dashboard_test.html` / `dashboard_en_test.html` — 同內容（保留 test 命名）
- `index.html` — 入口頁

## 這份儀表板展示什麼
- **摘要 KPI 卡**：sessions、互動率、推估詢價、GSC 點擊 / CTR / 平均排名
- **進站頁流量排名**（Top 12 長條圖 + 數值標籤）
- **指標小卡片**：頁面 session 排名、本月 vs 上月成長／下滑（紅漲綠跌、比例條）
- **轉換漏斗**（詢價 / LINE）
- **Google Search Console**：點擊／曝光走勢、**搜尋排名走勢（越低越好）**、熱門頁面、裝置
- **頁面 → 產品分類（B4）對應與大類彙總**
- 表格內建「溫度圖」依數值深淺上色

## 怎麼產生 / 發布（給維護者）
- 這裡的假資料**不是手改**，是由產生器自動脫敏產出。
- 重生 + 發布：在主專案執行 `scripts/sync-ga-dashboard.ps1`
  （它會跑 `gen_fake_dashboard.py` 重生假資料 → 在本資料夾 `git add/commit/push` 到 GA-Dashboard repo 的 `main` 分支）。
- 版面要改：改主專案的 `ga4_420655625_syfgift/scripts/build_dashboard_v2.py`（中英 / 真實 / 展示版共用同一套生成邏輯），不要直接手改這裡的成品 HTML。

_最後更新：2026-06-12_
