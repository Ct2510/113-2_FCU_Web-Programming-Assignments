# Altas｜Bootstrap 形象網站練習

## 專案簡介

以既有 Atlas Bootstrap 模板練習多區塊形象頁、導覽與動畫效果。Repository 名稱沿用 `Altas`；頁面原始模板名稱為 Atlas。

## 開發目的

將產品介紹、方案與聯絡資訊放在一頁式網站中，練習用版面層次、導覽與動畫組織形象頁內容。

## 核心功能與完成範圍

| 項目 | 說明 |
| --- | --- |
| 一頁式形象展示 | 以不同區塊呈現產品特色、方案與聯絡資訊。 |
| 圖文與圖示 | 搭配圖片與 Font Awesome 圖示表達內容。 |
| 捲動動畫 | 使用 AOS 為區塊加入進場效果。 |

## 技術實作

| 技術／模組 | 用途 |
| --- | --- |
| HTML／CSS | 組織區塊與客製樣式；以 Bootstrap 建立網格版面。 |
| JavaScript／AOS | 處理頁面互動與捲動動畫。 |
| 素材整合 | 沿用模板附帶圖像與圖示，保留原作者資訊。 |

### 專案資訊

| 項目 | 說明 |
| --- | --- |
| 定位 | 模板導向的靜態前端練習 |
| 技術 | HTML、CSS、JavaScript、Bootstrap、Font Awesome、AOS |
| 入口 | [index.html](index.html) |
| 後端／建置 | 無後端，無需 npm 建置 |

## 功能範圍

- 產品介紹、特色、方案與聯絡區塊，搭配頁面捲動及動畫效果。
- 本案展示版面與前端整合，不是資安產品；沒有垃圾郵件偵測、防釣魚、付款或聯絡表單寄信服務。

## 本機預覽

下載專案後，於專案根目錄執行（需 Python 3）：

```bash
git clone https://github.com/Ct2510/113-2_FCU_Web-Programming-Assignments.git
cd 113-2_FCU_Web-Programming-Assignments/assignments/Altas
python -m http.server 8080 --bind 127.0.0.1
```

開啟 <http://127.0.0.1:8080/>；以 `Ctrl+C` 停止。此命令只提供靜態檔案，不是應用程式後端。連接埠被佔用時可將 `8080` 改為 `8081`。

## 專案結構

| 路徑 | 用途 |
| --- | --- |
| [index.html](index.html) | 頁面結構與內容 |
| [css/](css/) | 樣式 |
| [js/](js/) | 前端互動與第三方腳本 |
| [img/](img/) | 頁面素材 |
| [font-awesome-4.7.0/](font-awesome-4.7.0/) | 圖示資源 |

## 測試與目前限制

尚無自動測試或建置流程；本次整理未執行瀏覽器驗收。手動檢查時可確認導覽、捲動動畫、手機寬度與素材是否載入，並查看瀏覽器主控台錯誤。

## 模板與素材來源

原始 HTML 標示「Bootstrap Template Atlas」，頁尾保留 `Copyright © 2018 Chen,Yi-Ya`。這是模板練習，不宣稱全部版面或素材為自行原創。第三方程式與素材須依各自授權使用；此整理不另行授予模板再散布權。
