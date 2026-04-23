# 資訊安全實務專案：多維度滲透測試與漏洞復現

本專案記錄了在 Kali Linux 環境下，針對 Web 應用程式、伺服器組件及容器化環境進行的各項資安檢測實務作業。

##  專案導覽 (Navigation)
為方便檢閱，本專案之相關證照與詳細技術文件已分類如下：

* **[實作技術文件](./實作文件)**：包含各項漏洞復現、HTB 滲透紀錄之詳細 Writeup。
* **[專業證照專區](./證照)**：包含 Azure AI Fundamentals、Google Analytics 等認證紀錄。
* **[跨領域競賽作品專區](./競賽作品專區)**：包含獲獎專案之說明文件與實作代碼。

---

##  關於此專案與學習聲明 (About & Learning Statement)
* **誠實聲明**：本專案內容主要為課程實作紀錄，過程中有適度參考教材、AI 輔助工具及技術社群資源，旨在透過漏洞復現理解資安攻防流程。
* **AI 輔助學習實踐**：
  在我的學習與專案開發過程中，我將 **Gemini** 等生成式 AI 工具視為輔助學習工具，主要應用於：
  * **技術術語白話化**：像是針對密碼學協議或網路架構進行概念拆解，確保具備正確的底層邏輯。
  * **代碼審計與重構**：在撰寫漏洞修復範例時，透過 AI 進行靜態分析，對比不同修補策略的優劣。
  * **滲透思路擴展**：在靶機挑戰遇到瓶頸時，請 AI 提供可能的列舉 (Enumeration) 方向，訓練系統化的滲透思維。

> **聲明：** 我以「先理解原理，再使用工具」為原則。所有由 AI 生成的代碼或建議，皆經過手動檢測與環境驗證。

---

##  核心技術實踐 (Core Skills)
- **Web 安全檢測**：利用 Burp Suite 進行封包攔截與偽造（Request Interception），成功實作身分驗證繞過（is_admin: true）。
- **漏洞復現與利用 (Exploit)**：針對 CVE-2024-23897 (Jenkins LFI) 編寫 Python 腳本，成功讀取系統敏感檔案（/etc/passwd）。
- **進階權限獲取 (RCE & LPE)**：
  - 在受限防火牆環境下，利用 WingFTP Lua 引擎執行 OS 指令獲取 Root 權限。
  - 實作 Langflow RCE 漏洞鏈，達成全鏈路提權（Full Chain）。
- **自動化與指令拼接**：掌握 Command Chaining 技巧，透過 Base64 編碼規避基礎過濾機制。

---

##  跨領域技術實踐 (Selected Projects)
除了資安研究，我也在不同技術領域進行開發實踐，培養多元的解決問題能力。

> **完整作品展示：[點此進入我的雲端作品集](https://drive.google.com/drive/folders/1vr4uqUVmuv7-guMDREFaYSpqZoikjVvs?usp=drive_link)**
> *(內含：獲獎專案示範影片、競賽成果報告、App 運行錄影與實作代碼)*

| 專案名稱 | 技術棧 | 實作亮點與說明 |
| :--- | :--- | :--- |
| **數位教材 App** | Figma | **獲獎專案**。從零開始製作互動式 App，實踐軟體開發與前端 UI 邏輯。 |
| **自動化控制腳本** | Python (Linux) | **Linux 專題**。開發自動化控制流程，實作google chrome 小恐龍遊戲影像識別與自動模擬操作。 |
| **Web CRUD 應用** | HTML / CSS / JS | 實作基礎後端資料庫操作邏輯，具備 Web 安全（如輸入驗證）之基礎實踐。 |
| **AI 動畫生成** | Generative AI (Gemini) / CapCut | **獲獎專案**。使用跨媒介協同創作，展現 AI 應用能力。 |

---

## 相關證照與環境維護
- **虛擬化技術**：實踐操作 VMware 上的 Kali Linux 滲透測試環境。
- **雲端資安基礎**：持有 **Microsoft Certified: Azure AI Fundamentals**。
- **數據分析**：持有 **Google Analytics (分析) 個人認證**。