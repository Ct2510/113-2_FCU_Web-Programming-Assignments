# Makar Template｜修改前基準

## 專案簡介

保留 **Makar** 網站模板的修改前版本，作為前端調整的比較基準。修改後版本見 [free_css_website_after](https://github.com/Ct2510/free_css_website_after)。

## 開發目的

保留同一份模板的改版前基準，方便對照內容、metadata、字型與樣式載入方式的差異，而不是只展示最後結果。

## 核心功能與完成範圍

| 項目 | 說明 |
| --- | --- |
| 原始版面基準 | 呈現 Makar 模板的區塊、導覽與附帶元件。 |
| 前後版比較 | 與 after 儲存庫對照 HTML 內容與載入設定。 |
| 靜態展示 | 不含會員、寄信、交易或資料庫後端。 |

## 技術實作

| 技術／模組 | 用途 |
| --- | --- |
| Bootstrap／jQuery | 使用原模板的版面與前端元件。 |
| CSS、圖片與字型 | 保留改版前的資源配置作比較。 |
| 比較方法 | 以原始碼差異為依據，不以未量測的 SEO 或效能分數宣稱成果。 |

### 專案資訊

| 項目 | 說明 |
| --- | --- |
| 定位 | 第三方模板基準，不是從零設計的完整產品 |
| 技術 | HTML、CSS、JavaScript、Bootstrap、jQuery 及模板附帶元件 |
| 入口 | [index.html](index.html) |
| 後端 | 無 |

## 比較重點

- 觀察模板的導覽、內容區塊、字型、圖片與前端互動。
- 與修改後版本比較內容、metadata、字型與樣式載入方式。
- 這裡沒有會員、交易、寄信或資料庫功能；聯絡區塊不等於已可送信。

## 本機預覽

下載專案後，於專案根目錄執行（需 Python 3）：

```bash
git clone https://github.com/Ct2510/113-2_FCU_Web-Programming-Assignments.git
cd 113-2_FCU_Web-Programming-Assignments/assignments/free_css_website_before
python -m http.server 8080 --bind 127.0.0.1
```

開啟 <http://127.0.0.1:8080/>；以 `Ctrl+C` 停止。此命令只提供靜態檔案，不是應用程式後端。連接埠被佔用時可將 `8080` 改為 `8081`。

外部字型與服務可能需要網路。頁面中的地圖整合含公開範例金鑰設定；**不要沿用、轉貼或視為自己的有效金鑰**。若未來要接地圖服務，應改用自己管理且限制來源／配額的設定；本次文件整理未變動程式碼或驗證地圖可用性。

## 專案結構

[index.html](index.html)：頁面 · [css/](css/)：樣式 · [js/](js/)：互動 · [images/](images/)：圖片 · [fonts/](fonts/)：字型素材。

## 測試、限制與來源

沒有自動測試或效能基準，本次未執行瀏覽器驗收。手動檢查可涵蓋導覽、不同寬度、圖片、主控台與第三方服務載入。

原頁尾標示 **Free Html Templates** 並連至 [HTML Design](https://html.design/)。保留作者標示；模板與附帶素材的再利用須確認各自授權，不宣稱全數為自行原創，也不另加 MIT 授權。
