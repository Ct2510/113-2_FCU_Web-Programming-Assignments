# 整合範圍與來源

整理日期：2026-10-29。課程學期為使用者確認的 **113-2 Web 程式設計**；不以本次整理日期推定當年的作業繳交日期。

## 收錄範圍

使用者確認原本誤算為 14 個，實際公開清單為 13 個。`phishing_website` 由 GitHub 回報 `Repository access blocked`、原因 `tos`，經使用者同意不收錄；沒有嘗試規避該限制。本庫整合其餘 **12 個**可正常讀取的 repo，全部放在 `assignments/<原 repo 名稱>/`。

原始 repo 均保留，不刪除、不轉移擁有權、不封存，也不修改其公開設定或歷史。

## 匯入方式與歷史

本庫採用各來源預設分支的固定版本快照，而非把多個獨立 Git 歷史混接。原作者、提交日期與歷史仍可到原 repo 查閱；本庫的新提交反映這次整合，不回填日期，也不保證 GitHub 的新檔案「最後編輯時間」顯示為舊日期。

每個來源的分支、commit SHA、完整檔案清單與雜湊見 [SOURCE_MANIFEST.json](SOURCE_MANIFEST.json)。該清單亦記錄實際排除的安裝套件、編輯器設定與資料庫產物。

## 保留與調整

- 保留 HTML、CSS、JavaScript、圖片、字型、音效、JSON／CSV、package.json、package-lock.json 及現有授權文件。
- 不改寫原有應用功能；各作業仍獨立執行，不把兩個 Express 服務合併為一個 API。
- 作業 README 的下載／切換目錄指令改成整合庫路徑。原有功能限制與模板來源保留，不把學習骨架寫成完成品。
- `free_css_website_before/index.html` 的內嵌 Google Maps API 金鑰以 `YOUR_GOOGLE_MAPS_API_KEY` 示意值取代，避免再次公開。地圖需要合法、妥善限制的自有設定；本次未驗證此功能。
- 未收錄舊 `node_modules`、`.idea`、SQLite 資料庫及 journal、日誌、原生執行檔等；來源的既有依賴可由鎖檔重新安裝。
- 隨附漁產 JSON／CSV 是程式使用的初始化資料，並非日誌或可刪除的執行產物，故保留。

## web_hw4 的資料庫差異

來源曾直接追蹤 `db/sqlite.db` 及 journal，整合版不再複製它們。全新副本需先以 `node import_json.js` 建表並匯入 JSON，再以 `node app.js` 啟動。

這不保證重建結果包含舊資料庫中的人工修改；原資料仍在舊 repo。本庫沒有刪除或覆寫使用者原本的資料庫。匯入程式會追加資料，重複執行可能造成重複列。

`web_hw4` 的來源 `npm start` 指向不存在的 `bin/www`。整合文件提供實際可用的 `node app.js` 入口，本次未藉整理修改 package scripts 或其他功能。

## 已知限制

- D1211137 缺少引用的本機圖片；fetching_data 的資料取得 script 尚未完成。
- POPCAT 計數／保存、模板內既有資源路徑等問題依原作業狀況保留；整理不是全面修復。
- CDN、字型、遠端圖片及第三方服務可能需要網路或獨立設定。
- 兩個後端缺少完整權限控制，不應直接公開部署。
- 掃描未發現高信度金鑰，不等於完整資安稽核；實際驗證範圍見 [VALIDATION.md](VALIDATION.md)。
