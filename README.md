# Pitch Tracker｜投球球速追蹤器

生成式 AI 課程 Week 5 作品。透過與 AI 討論規格、實作、瀏覽器測試及修改完成。目標是讓個別球員記錄球速，並探索真實公開資料中的樣本比較。

正式網站：https://han020305.github.io/pitch-tracker/

## 開啟

直接以 Edge、Chrome 或 Firefox 開啟 `index.html`。CSS、JavaScript、參考資料均內嵌，操作不需安裝套件或連線；點擊外部資料來源連結才需要網路。個人資料只在目前瀏覽器保存，不需帳號。瀏覽器的本機檔案儲存行為可能不同，換成 GitHub Pages 後應重新確認保存功能，並自行匯出 CSV 備份。

## 功能

- 手動新增、編輯、刪除與清除投球紀錄；球速超過 130 km/h 時確認。
- 顯示最高、平均、最近球速與紀錄數；圖表呈現每球及每日平均。
- CSV 範本、加入／取代匯入、錯誤列提示、匯出備份。
- 獨立範例體驗模式，包含虛構紀錄；操作不影響個人資料。
- 公開成年大專投手樣本比較、身材篩選與樣本內 PR；一般成年人資料不足或指標不符時不計算 PR。
- 電腦、手機可用的深色運動科技介面。

## 資料與授權

來源：Driveline Baseball Research & Development 的 [OpenBiomechanics Project](https://github.com/drivelineresearch/openbiomechanics)。開發與資料重建檔案隨作業本機資料夾保存；下載來源及雜湊見 `reference_audit.json`。資料 411 次直球、100 位球員；本作品選成年大專球員 75 人，每人計算所提供試投平均，並轉成 km/h。不是一般人常模、台灣投手常模、個人生理上限或經過外部驗證的預測模型。原作者未替本作品背書。

原資料及本作品中的衍生資料依 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 與原始 [LICENSE-DATA.md](https://github.com/drivelineresearch/openbiomechanics/blob/main/LICENSE-DATA.md) 額外限制分享。來源禁止商業用途，另對職業運動組織、財務分析公司相關人員設有使用限制。不得宣稱僅因公開就可任意商用。資料重建程式為 `build_reference.py`，不需第三方 Python 套件。

## GitHub Pages 發布方式

1. 在自己的 GitHub 帳號建立公開 repository，例如 `pitch-tracker`。
2. 上傳 `index.html`、本 README 與實作版規格書，按 Commit changes。保留 README 與網頁內的資料歸屬、授權說明。
3. Repository → Settings → Pages → Build and deployment，選 Deploy from a branch、main、/(root)，儲存。
4. 等待 GitHub 顯示正式網站網址，再開啟檢查。網址應以 GitHub 實際提供的結果為準。
5. 在公開網站測試範例、紀錄、CSV、刷新保存及手機版，再截取正式網站畫面。

上傳時不需要瀏覽器測試腳本、下載的原始 CSV 或開發工具；網站本身只需 index.html。規格與 README 可以作為審閱資料。勿把個人測試紀錄或私人資料上傳到 repository。

## 驗證

`check_site.cjs` 為開發用瀏覽器測試，使用本機 bundled Playwright 與 Edge；測試結果寫入 `browser_test_results.json`。截圖是實際執行頁面的範例模式，資料明確標示為虛構。這些測試使用獨立暫存瀏覽器，不操作使用者的瀏覽器資料。

網站已於 2026-10-17 公開並驗證範例、PR、新增紀錄、CSV 部分匯入與錯誤提示；課程繳交尚未完成。繳交仍需正式網站連結、實際介面截圖及規格文字，標題內的學校、學號、系級、姓名須由本人確認。
