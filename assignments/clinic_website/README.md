# Clinic Website｜診所網站模板練習

## 專案簡介

以 HTML Codex 的 **Klinik - Clinic Website Template** 練習多頁網站、導覽與響應式版面；不是已上線的診所服務。

## 開發目的

以診所的介紹、服務、團隊與預約資訊為情境，練習多頁網站的資訊架構與一致導覽，讓訪客能找到服務內容與聯絡入口。

## 核心功能與完成範圍

| 項目 | 說明 |
| --- | --- |
| 診所資訊展示 | 呈現診所、服務與團隊等分頁內容。 |
| 多頁導覽 | 維持首頁與其他 HTML 分頁之間的連結。 |
| 前端元件 | 整合輪播、動畫與日期時間選擇等互動。 |
| 預約／聯絡版面 | 展示表單入口，尚未串接預約或寄信後端。 |

## 技術實作

| 技術／模組 | 用途 |
| --- | --- |
| Bootstrap 5 | 建立網格、導覽與響應式元件。 |
| CSS／SCSS | 管理頁面樣式與模板樣式來源。 |
| jQuery 與附帶元件 | 處理輪播、動畫及日期選擇；部分依賴從 CDN 載入。 |

### 專案資訊

| 項目 | 說明 |
| --- | --- |
| 技術 | HTML、CSS／SCSS、JavaScript、Bootstrap 5、jQuery |
| 主入口 | [index.html](index.html) |
| 模板說明 | [READ-ME.txt](READ-ME.txt) |
| 授權文件 | [LICENSE.txt](LICENSE.txt) |

## 使用範圍

頁面包含診所介紹、服務、團隊、預約及聯絡等展示內容，並整合動畫、輪播與日期時間選擇等前端元件。

**目前只有靜態頁面**；預約／聯絡表單不代表已串接實際預約、寄信、病患資料庫或會員系統。請勿在示範表單輸入真實醫療或個人資料。

## 本機預覽

下載專案後，於專案根目錄執行（需 Python 3）：

```bash
git clone https://github.com/Ct2510/113-2_FCU_Web-Programming-Assignments.git
cd 113-2_FCU_Web-Programming-Assignments/assignments/clinic_website
python -m http.server 8080 --bind 127.0.0.1
```

開啟 <http://127.0.0.1:8080/>；以 `Ctrl+C` 停止。此命令只提供靜態檔案，不是應用程式後端。連接埠被佔用時可將 `8080` 改為 `8081`。

部分字型與函式庫由 CDN 載入，完整呈現需要網路；本機靜態伺服器不提供任何醫療業務功能。

## 專案結構

| 路徑 | 用途 |
| --- | --- |
| [index.html](index.html) | 首頁，其他 HTML 檔為分頁 |
| [css/](css/)、[scss/](scss/) | 樣式與 SCSS 來源 |
| [js/](js/)、[lib/](lib/) | 頁面互動與第三方元件 |
| [img/](img/) | 模板圖片 |

## 測試與目前限制

未提供自動測試；本次未執行瀏覽器或表單後端驗收。可手動檢查各分頁連結、手機導覽、輪播、日期選擇器與 CDN 載入；表單畫面正常不等於資料已送到後端。

## 來源與授權

作者與來源依 [READ-ME.txt](READ-ME.txt) 及 [LICENSE.txt](LICENSE.txt)。保留 HTML Codex 等原有作者標示；不得把模板或其素材改稱全部自行設計。若要再利用或發布，請先閱讀儲存庫中的授權條件。本次未替換或新增授權。
