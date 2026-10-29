# 113-2_FCU_Web-Programming-Assignments

逢甲大學 113 學年度第 2 學期「Web 程式設計」課程作業與期末專題。

內容涵蓋 HTML、CSS、JavaScript 網頁開發，以及使用 Node.js、Express、SQLite 建立資料查詢與圖表應用。

## 專案結構

```text
113-2_FCU_Web-Programming-Assignments/
├── assignments/
│   ├── D1211137/                  HTML 基礎練習
│   ├── Altas/                     Atlas 網站模板練習
│   ├── clinic_website/            診所形象網站
│   ├── free_css_website_before/   網站模板修改前
│   ├── free_css_website_after/    網站模板修改後
│   ├── waiting_page/             載入動畫與音樂控制
│   ├── bouncing_balls/           Canvas 彈跳球動畫
│   ├── Snake/                    貪食蛇遊戲
│   ├── classic-popcat-click-1134/ POPCAT 點擊互動
│   ├── fetching_data/            JSON 與資料取得練習
│   ├── web_hw4/                  漁產價格圖表
│   └── WebFinalProject/          漁產價格查詢與維護
├── docs/
├── .gitignore
├── THIRD_PARTY_NOTICES.md
└── README.md
```

## 作業內容

| 作業 | 內容 |
| --- | --- |
| [D1211137](assignments/D1211137/) | HTML 頁面結構、文字與圖片。 |
| [Altas](assignments/Altas/) | 使用 Atlas 模板，練習 Bootstrap 版型與 AOS 動畫。 |
| [clinic_website](assignments/clinic_website/) | 使用網站模板製作診所形象頁面，練習多頁導覽與響應式設計。 |
| [free_css_website_before](assignments/free_css_website_before/) | 網站模板修改前的版本。 |
| [free_css_website_after](assignments/free_css_website_after/) | 調整網站內容、字型、樣式與 metadata。 |
| [waiting_page](assignments/waiting_page/) | 模擬載入進度，搭配動畫與背景音樂控制。 |
| [bouncing_balls](assignments/bouncing_balls/) | 使用 Canvas 製作彈跳球動畫，處理移動、邊界與碰撞變色。 |
| [Snake](assignments/Snake/) | 以 DOM 網格與鍵盤事件實作貪食蛇，包含分數、暫停與繼續。 |
| [classic-popcat-click-1134](assignments/classic-popcat-click-1134/) | 練習滑鼠與鍵盤事件、圖片切換及音效播放。 |
| [fetching_data](assignments/fetching_data/) | JSON 資料、Fetch 與 callback 的課堂練習頁面與筆記。 |
| [web_hw4](assignments/web_hw4/) | 將 JSON 匯入 SQLite，透過 Express API 查詢資料，並以 Chart.js 呈現價格走勢。 |
| [WebFinalProject](assignments/WebFinalProject/) | 匯入漁產價格 CSV，提供產品與年份區間查詢、價格圖表及資料新增與更新。 |

## 快速開始

### 下載專案

```bash
git clone https://github.com/Ct2510/113-2_FCU_Web-Programming-Assignments.git
cd 113-2_FCU_Web-Programming-Assignments
```

各作業獨立執行，後端套件請在對應作業資料夾中安裝。

### 靜態網頁作業

安裝 Python 3 後，在專案根目錄啟動本機伺服器：

```bash
python -m http.server 8080 --bind 127.0.0.1
```

在瀏覽器開啟對應作業，例如：

- 貪食蛇：<http://127.0.0.1:8080/assignments/Snake/>
- 彈跳球：<http://127.0.0.1:8080/assignments/bouncing_balls/>
- 網站改版：<http://127.0.0.1:8080/assignments/free_css_website_after/>

字型、圖表套件與其他 CDN 資源需要網路連線。

### web_hw4：漁產價格圖表

需要 Node.js 與 npm。在專案根目錄執行：

```bash
cd assignments/web_hw4
npm ci
node import_json.js
node app.js
```

啟動後開啟 <http://127.0.0.1:3000/>。

首次使用時執行一次 `node import_json.js` 建立資料表並匯入 JSON。之後啟動只需執行 `node app.js`；重複匯入會產生重複資料。

### WebFinalProject：漁產價格查詢與維護

需要 Node.js 與 npm。在專案根目錄執行：

```bash
cd assignments/WebFinalProject
npm ci
npm start
```

啟動後開啟 <http://127.0.0.1:3000/>。首次啟動會在資料表為空時匯入 CSV，請等待匯入完成後再查詢。

兩個後端預設使用連接埠 3000，請分開啟動。課程程式供本機練習使用，請勿直接對外部署。

## 技術棧

- 網頁：HTML、CSS、JavaScript、Bootstrap
- 互動與圖表：DOM、Canvas、Chart.js
- 後端：Node.js、Express
- 資料庫與資料處理：SQLite、JSON、CSV、csv-parser

## 素材來源

網站模板、函式庫、圖片與音樂依各自授權使用，來源與署名詳見 [第三方素材說明](THIRD_PARTY_NOTICES.md)。
