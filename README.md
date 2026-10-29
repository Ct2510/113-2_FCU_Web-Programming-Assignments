# Web 程式設計｜作業與期末專案

**逢甲大學 · 113 學年度第 2 學期 · Web 程式設計**

將原本分散的課堂練習、網站模板改版及期末專案，整理為一個課程作品集。內容由 HTML／CSS 基礎、JavaScript 互動，延伸至 Node.js、Express 與 SQLite 的資料查詢應用。

這是 **12 個獨立作業的集合**，不是將所有功能合併成同一個應用程式。各資料夾保留自己的入口、素材、依賴及說明，不需安裝整個作品集的共用套件。

## 建議閱讀順序

- **全端整合**：[WebFinalProject 漁產價格查詢與維護](assignments/WebFinalProject/) → 資料匯入、API、篩選與圖表。
- **前端改版**：[修改前](assignments/free_css_website_before/) → [修改後](assignments/free_css_website_after/) → 比較內容、metadata、字型與樣式設定。
- **互動邏輯**：[Snake](assignments/Snake/) 與 [Bouncing Balls](assignments/bouncing_balls/) → 事件、狀態更新、動畫與碰撞判斷。

## 作業索引

| 作業／資料夾 | 內容與學習重點 | 執行方式／目前範圍 |
| --- | --- | --- |
| [D1211137](assignments/D1211137/) | HTML 起始頁、文字與圖片引用 | 靜態頁；未附齊圖片，沒有計分互動 |
| [Altas](assignments/Altas/) | Atlas 模板、多區塊版型、Bootstrap、AOS | 靜態模板整合練習；沿用原 repo 拼字 |
| [clinic_website](assignments/clinic_website/) | 診所形象網站、多頁導覽與響應式版型 | 第三方模板練習；非真實掛號系統 |
| [free_css_website_before](assignments/free_css_website_before/) | Makar 模板修改前基準 | 靜態模板；內嵌地圖金鑰已換成示意值 |
| [free_css_website_after](assignments/free_css_website_after/) | Software Maker 改版、metadata、字型與樣式 | 模板客製；不宣稱全部版面原創 |
| [waiting_page](assignments/waiting_page/) | 模擬載入進度、動畫與音樂控制 | 靜態互動；不是實際下載進度 |
| [bouncing_balls](assignments/bouncing_balls/) | Canvas、物件狀態、動畫迴圈與碰撞變色 | 前端動畫；非完整物理引擎 |
| [Snake](assignments/Snake/) | DOM 網格、鍵盤輸入、分數與遊戲狀態 | 前端遊戲；包含暫停／繼續 |
| [classic-popcat-click-1134](assignments/classic-popcat-click-1134/) | 指標／鍵盤事件、圖片切換與音效 | 前端互動；計數與保存仍有已知限制 |
| [fetching_data](assignments/fetching_data/) | HTML、JSON 與 Fetch／callback 學習筆記 | 練習骨架，資料取得腳本尚未完成 |
| [web_hw4](assignments/web_hw4/) | Express、SQLite、JSON 匯入與價格圖表 | 全端作業；需先初始化資料庫 |
| [WebFinalProject](assignments/WebFinalProject/) | CSV 匯入、價格區間查詢、資料維護與 Chart.js | 期末全端專案；限受控本機展示 |

## 技術範圍

| 類別 | 本課程作品中使用的技術 |
| --- | --- |
| 網頁結構與樣式 | HTML、CSS、Bootstrap、第三方模板與字型素材 |
| 前端互動 | JavaScript、DOM、Canvas、瀏覽器事件、Fetch、Chart.js |
| 後端 | Node.js、Express、HTTP／JSON API |
| 資料儲存與匯入 | SQLite、JSON、CSV、csv-parser |

技術清單是整個課程作品集的範圍，不表示每個作業都使用全部技術。未完成項目及限制以各作業 README 為準。

## 快速開始

```bash
git clone https://github.com/Ct2510/113-2_FCU_Web-Programming-Assignments.git
cd 113-2_FCU_Web-Programming-Assignments
```

### 靜態作業

需 Python 3。在作品集根目錄執行：

```bash
python -m http.server 8080 --bind 127.0.0.1
```

例如開啟：

- Snake：<http://127.0.0.1:8080/assignments/Snake/>
- Bouncing Balls：<http://127.0.0.1:8080/assignments/bouncing_balls/>
- 改版後網站：<http://127.0.0.1:8080/assignments/free_css_website_after/>
- 資料練習的圖文頁：<http://127.0.0.1:8080/assignments/fetching_data/mycar.html>

以 `Ctrl+C` 停止。8080 被使用時可改為 8081。字型、CDN、外部圖片等資源仍需網路；靜態伺服器不會提供後端 API。

### web_hw4：JSON 匯入與價格查詢

需 Node.js、npm，以及可安裝 `sqlite3` 原生模組的環境。請在全新的資料庫副本操作：

```bash
cd assignments/web_hw4
npm ci
node import_json.js
node app.js
```

開啟 <http://127.0.0.1:3000/>。整合版不附資料庫或 journal，首次需從隨附 JSON 初始化。**匯入程式會追加資料，不可為了重新整理頁面而反覆執行。** 來源的 `npm start` 指向缺少的 `bin/www`，因此此作業以 `node app.js` 啟動；本次整理不改寫原有功能。

### WebFinalProject：期末專案

```bash
cd assignments/WebFinalProject
npm ci
npm start
```

開啟 <http://127.0.0.1:3000/>。等待首次 CSV 匯入完成再查詢。兩個後端都預設使用 3000，請分開啟動，不要同時執行；細節見各自 README。

**安全範圍**：這些後端為課程練習，沒有完整登入／權限控制，且未限制只監聽 loopback。請只在受控本機環境使用，不做公開部署或連接埠轉發。

## 目錄

```text
113-2_FCU_Web-Programming-Assignments/
├─ assignments/                 各自獨立的 12 個作業與期末專案
├─ docs/
│  ├─ MIGRATION.md              來源、整合範圍及已知差異
│  ├─ SOURCE_MANIFEST.json      來源 commit、檔案雜湊與排除清單
│  └─ VALIDATION.md             本次實際檢查結果與未驗證項目
├─ THIRD_PARTY_NOTICES.md       模板、套件及素材署名說明
└─ README.md
```

## 整理與驗證

- 原本的 repo 保留，不刪除、不封存，也不變更原始提交時間。
- 本庫收錄固定來源版本的檔案快照，沒有把舊 commit 改寫成新目錄歷史；來源版本均記錄於 [移轉說明](docs/MIGRATION.md)。
- 已排除 `node_modules`、編輯器設定、資料庫、journal、日誌及執行產物；保留重建所需 JSON／CSV 與鎖檔。
- `phishing_website` 因 GitHub 使用條款封鎖而未收錄，未以新 repo 重發或繞過封鎖。
- 本次檢查與尚未完成的功能驗收，請見 [驗證報告](docs/VALIDATION.md)。整理不代表原有缺陷均已修復。

## 授權與來源

這是課程作業整理，不是可自由套用的模板下載庫。第三方模板、函式庫、圖片、音樂與資料仍依各自授權及使用條件；保留原作者署名與現有授權文件，**不以整包 MIT 授權覆蓋所有素材**。詳見 [第三方來源說明](THIRD_PARTY_NOTICES.md)。
