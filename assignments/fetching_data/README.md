# Fetching Data｜前端資料取得學習骨架

## 專案簡介

整理 Fetch API 與 callback 練習頁的起點。**目前資料取得邏輯尚未完成**，不是已串接外部 API 的應用程式。

## 開發目的

建立前端資料取得練習的檔案骨架，後續可用同一份 JSON 比較 Fetch、Promise 與 callback 的處理方式；目前不宣稱資料讀取已完成。

## 核心功能與完成範圍

| 項目 | 說明 |
| --- | --- |
| Fetch API 筆記 | 提供 fetch_info.txt 學習內容。 |
| 練習頁面 | 保留 Fetch 與 callback HTML 入口，script 尚空。 |
| 本機 JSON | products.json 可作後續資料讀取練習。 |
| 靜態圖文頁 | mycar.html 展示文字與圖片，與資料 API 無關。 |

## 技術實作

| 技術／模組 | 用途 |
| --- | --- |
| HTML／JSON | 準備練習頁與資料範例。 |
| Fetch／callback | 屬待完成項目，目前沒有自動取得並渲染資料的程式。 |

## 專案結構與完成狀態

| 檔案 | 目前內容 |
| --- | --- |
| [fetch_info.txt](fetch_info.txt) | Fetch API 學習筆記 |
| [fetch_api.html](fetch_api.html) | 練習頁，script 內容尚空 |
| [fetch_callback.html](fetch_callback.html) | callback 練習頁，script 內容尚空 |
| [products.json](products.json) | 可供後續練習的本機 JSON 資料 |
| [mycar.html](mycar.html) | 靜態圖片與文字展示 |
| [index.html](index.html) | 空白入口，未完成導覽 |
| [img_car.jpg](img_car.jpg) | 靜態展示圖片 |

## 本機預覽

下載專案後，於專案根目錄執行（需 Python 3）：

```bash
git clone https://github.com/Ct2510/113-2_FCU_Web-Programming-Assignments.git
cd 113-2_FCU_Web-Programming-Assignments/assignments/fetching_data
python -m http.server 8080 --bind 127.0.0.1
```

開啟 <http://127.0.0.1:8080/>；以 `Ctrl+C` 停止。此命令只提供靜態檔案，不是應用程式後端。連接埠被佔用時可將 `8080` 改為 `8081`。

首頁目前為空白；可直接開啟 <http://127.0.0.1:8080/fetch_api.html> 或 <http://127.0.0.1:8080/mycar.html> 閱讀目前頁面。啟動靜態伺服器不會自動補上 Fetch 功能。

## 後續練習方向（未實作）

1. 以 Fetch 讀取 `products.json`，顯示載入中、成功、空資料與錯誤狀態。
2. 將相同流程分別以 Promise／async-await 與 callback 寫法比較。
3. 補齊首頁導覽、修正 HTML 結構並加入資料解析測試。

## 測試、限制與素材

未提供自動測試；本次未執行瀏覽器驗收。圖片與引用文字的來源／授權須另行確認，不因公開儲存庫而視為可自由再利用。
