# 整合驗證報告

執行日期：2026-10-29。這是整合檢查，不等於所有作業通過功能驗收。

| 檢查 | 實際結果 |
| --- | --- |
| 作業資料夾與 README | 12 個作業、12 份 README 路徑更新完成 |
| 來源檔案完整性 | 512 個來源檔核對；僅 README 與已記錄的地圖金鑰去識別化有差異 |
| 排除清單 | 1628 個安裝套件、設定或執行產物未收錄 |
| 高信度金鑰／私鑰模式掃描 | 整合後收錄檔案未檢出；不代表完整資安稽核 |
| JavaScript 語法 | 80 個外部／行內 script 檢查，失敗 0 個；Node v24.19.0 |
| 靜態入口 HTTP | 10 個入口回傳 HTTP 200；不代表互動功能驗收 |
| 初始化資料 | JSON 8777 列、CSV 243 列，必要欄位及數值格式可讀取 |
| HTML 本機素材引用 | 14 筆既有缺檔警示，列於下方 |
| npm 安裝／原生 SQLite／後端 API | 本次未執行，未聲稱已通過 |
| 瀏覽器互動／行動版／第三方 CDN | 本次未執行完整驗收 |

## 素材引用警示

| 頁面 | 找不到的本機資源 |
| --- | --- |
| `assignments/clinic_website/404.html` | `img/favicon.ico` |
| `assignments/clinic_website/about.html` | `img/favicon.ico` |
| `assignments/clinic_website/appointment.html` | `img/favicon.ico` |
| `assignments/clinic_website/contact.html` | `img/favicon.ico` |
| `assignments/clinic_website/feature.html` | `img/favicon.ico` |
| `assignments/clinic_website/index.html` | `img/favicon.ico` |
| `assignments/clinic_website/service.html` | `img/favicon.ico` |
| `assignments/clinic_website/team.html` | `img/favicon.ico` |
| `assignments/clinic_website/testimonial.html` | `img/favicon.ico` |
| `assignments/D1211137/index.html` | `imgs/popcat.svg` |
| `assignments/free_css_website_after/index.html` | `images/fevicon.png` |
| `assignments/free_css_website_before/index.html` | `images/fevicon.png` |
| `assignments/waiting_page/index.html` | `sounds/click.mp3` |
| `assignments/waiting_page/index.html` | `sounds/error.mp3` |

## 驗證界線

- JavaScript 檢查只解析語法，沒有執行或驗證 UI、資料庫、音效、地圖及第三方服務。
- 靜態 HTTP 只確認入口可取得，不提供 Express API，也未把未完成的 Fetch 練習當成完成品。
- 根目錄及說明文件的相對連結另由整合檢查核對；來源既有問題不藉整理改成功能已完成。
- 原 repo、來源 commit 與移轉差異見 [MIGRATION.md](MIGRATION.md) 及 [SOURCE_MANIFEST.json](SOURCE_MANIFEST.json)。
