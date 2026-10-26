# 沖繩藍海慢活五日｜網站 v1.6

這是 2026/11/15–11/19 沖繩家族自駕行程網站的完整靜態網站套件。包含首頁、五日行程資料、插畫、Google Maps 導航與資料暫放控制台。

## v1.6 圖片對應修正

- Day 1：抵達機場主圖放在機場行程前；晚餐插畫對應「福州園 Garden Cafe」；超商採買插畫放在飯店入住項目前；泡澡插畫保留在當日最後。
- Day 2：取車主圖、玉泉洞、奧武島玻璃船、JA やんばる市場、晚餐／夕陽、唐吉訶德與泡澡收尾依各自的行程名稱對應。
- Day 1 與 Day 2 的插畫觸發條件改為比對行程名稱，而不是 stop 陣列索引；日後在前面新增行程時，不會再把後面的插畫整批推移。
- 一般行程頁不顯示更新網站的浮動按鈕；管理入口集中在「資料暫放控制台」。
- 控制台改連到 GitHub 專案與 Actions 部署紀錄，不再引導使用 Netlify。

## 部署到 GitHub Pages

此 ZIP 是完整網站素材包。若要透過本專案的 GitHub Actions 自動部署：

1. 將這個 ZIP 下載到手機，於 GitHub 專案首頁選 **Add file → Upload files**。
2. 把 ZIP 上傳到儲存庫根目錄，檔名必須是 `site-bundle.zip`，不要先在手機解壓縮。
3. Commit 到 `main`。`.github/workflows/deploy-pages.yml` 會把網站解壓到 Pages 發布資料夾並部署。
4. 第一次部署前，若 GitHub 提示尚未啟用 Pages，開啟 Settings → Pages，將 Build and deployment 的 Source 設為 **GitHub Actions**。
5. 到 Actions 頁面確認 `Deploy Okinawa Trip Website` 工作成功。成功後，公開網址會顯示在部署工作紀錄內。

注意：這份網站套件本身沒有部署至任何線上網站；GitHub Pages 的實際網址與狀態以該儲存庫的 Pages 設定及 Actions 執行結果為準。
