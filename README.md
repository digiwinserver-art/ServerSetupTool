# ServerSetupTool

Windows Server 設定工具的**成品發布儲存庫**，不公開程式原始碼。

## 下載與使用

1. 到 [最新發布版本](https://github.com/digiwinserver-art/ServerSetupTool/releases/latest)。
2. 在 Assets 下載 **ServerSetupTool-win-x64.zip**，完整解壓縮；不要下載 GitHub 自動產生的 Source code ZIP。
3. 執行 `ServerSetupTool.exe`，接受管理員權限提示。先查看說明，再勾選需要的工作。

需求：Windows Server 2016／2019／2022／2025 Desktop Experience 或支援的 Windows 11 x64；.NET Framework 4.8。個別工作仍受作業系統與原則限制。工具不自動重開機。

## 更新與離線使用

從 1.0.29 開始，程式啟動後會在背景查詢此儲存庫，最多等候 2 秒；無法連網直接略過。有新版會顯示提示，由您決定是否下載。新版在獨立資料夾準備，複製設定與 Offline，保留舊版；完成後請關閉舊版，再啟動新版。

離線電腦可從其他電腦取得並複製完整發布包。第三方安裝檔不隨發布包提供；可在有網路的電腦使用「製作離線安裝包」，再將 EXE、exe.config 與 Offline 一起帶到目標電腦。詳細相容性、操作、備份及還原方式見 ZIP 內的 README.md 與使用說明.html。

## 儲存庫內容

- Releases：給使用者下載的正式 ZIP、SHA-256 及更新說明。
- packages：提供給發布流程的已編譯 ZIP 與版本／雜湊資料，不包含原始碼。
- .github/workflows：將已驗證成品建立為 GitHub Release 的流程，不在 GitHub 編譯或執行程式。

程式目前未使用商用程式碼簽章；請只從本儲存庫取得檔案。SHA-256 用於核對下載完整性，不取代對發布者的信任。

從1.0.30起，更新除核對雜湊外，還必須通過程式內嵌公鑰的獨立發布簽章驗證。Release 提供 release.json 與 release.json.sig；GitHub Actions 只驗證與發布，不持有簽署私鑰。首次從1.0.29升級仍由舊版驗證流程處理。
