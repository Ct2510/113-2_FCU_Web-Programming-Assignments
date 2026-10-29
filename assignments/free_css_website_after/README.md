# Software Maker｜模板改版練習

## 專案簡介

以 Makar 模板為基礎，將頁面內容調整為軟體開發服務形象頁。原始基準見 [free_css_website_before](https://github.com/Ct2510/free_css_website_before)。

## 開發目的

將既有形象網站模板調整成軟體服務情境，練習需求導向的內容替換、搜尋／分享資訊與前端樣式設定。

## 核心功能與完成範圍

| 項目 | 說明 |
| --- | --- |
| 軟體服務形象頁 | 將標題與主要內容改為 Software Maker 服務介紹。 |
| 搜尋／分享資訊 | 調整頁面 metadata 與 Open Graph 等資訊。 |
| 字型與載入設定 | 加入 Noto Serif、preload 與頁面樣式設定。 |
| 前後版本對照 | 保留 before 連結，便於比較實際原始碼差異。 |

## 技術實作

| 技術／模組 | 用途 |
| --- | --- |
| HTML／metadata | 整理頁面標題、描述及分享資訊。 |
| CSS／字型 | 調整視覺風格及樣式載入配置。 |
| 模板客製 | 在第三方模板基礎修改，保留來源資訊，不宣稱全部版面原創。 |

### 專案資訊

| 項目 | 說明 |
| --- | --- |
| 定位 | 模板客製與前端改版練習 |
| 技術 | HTML、CSS、JavaScript、Bootstrap、jQuery |
| 入口 | [index.html](index.html) |
| 執行方式 | 靜態伺服器，無後端或 npm 建置 |

## 改版內容比較

| 面向 | 修改後內容 |
| --- | --- |
| 網站內容 | 標題改為 Software Maker，內容轉向軟體開發服務 |
| 搜尋／分享資訊 | 調整 title、description、keywords、robots 與 Open Graph metadata |
| 字型 | 加入 Noto Serif 等字型設定 |
| 樣式載入 | 加入 preload、頁面關鍵樣式與動畫設定 |

這些是**程式碼與內容變更**，不是已證實的 SEO 排名或效能提升；目前沒有 Lighthouse、流量或轉換率的前後測數據。也沒有真實公司營運、接案或寄信後端的聲明。

## 本機預覽

下載專案後，於專案根目錄執行（需 Python 3）：

```bash
git clone https://github.com/Ct2510/113-2_FCU_Web-Programming-Assignments.git
cd 113-2_FCU_Web-Programming-Assignments/assignments/free_css_website_after
python -m http.server 8080 --bind 127.0.0.1
```

開啟 <http://127.0.0.1:8080/>；以 `Ctrl+C` 停止。此命令只提供靜態檔案，不是應用程式後端。連接埠被佔用時可將 `8080` 改為 `8081`。

部分外部字型／函式庫需網路。若看到聯絡表單，請只作版面展示，不要填入真實個資。

## 專案結構與驗證

[index.html](index.html)：主要改版內容 · [css/](css/)：樣式 · [js/](js/)：互動 · [images/](images/)：圖片 · [fonts/](fonts/)：字型素材。

建議先對照兩個 Repository 的 `index.html`，再檢查桌機／手機寬度與載入行為。沒有自動測試；本次文件整理未完成瀏覽器或效能驗收。

## 模板與授權

原頁尾保留 **Free Html Templates** 與 [HTML Design](https://html.design/) 來源連結。這是模板客製，不宣稱全部設計與素材為原創；再發布前應確認模板及第三方素材授權。
