# 資訊安全實務專案：多維度滲透測試與漏洞復現

本專案記錄了在 Kali Linux 環境下，針對 Web 應用程式、伺服器組件及容器化環境進行的各項資安檢測實務作業。

## 核心技術實踐
- **Web 安全檢測**：利用 Burp Suite 進行封包攔截與偽造（Request Interception），成功實作身分驗證繞過（is_admin: true）。
- **漏洞復現與利用 (Exploit)**：針對 CVE-2024-23897 (Jenkins LFI) 編寫 Python 腳本，成功讀取系統敏感檔案（/etc/passwd）。
- **進階權限獲取 (RCE & LPE)**：
  - 在受限防火牆環境下，利用 WingFTP Lua 引擎執行 OS 指令獲取 Root 權限。
  - 實作 Langflow RCE 漏洞鏈，達成全鏈路提權（Full Chain）。
- **自動化與指令拼接**：掌握 Command Chaining 技巧，透過 Base64 編碼規避基礎過濾機制。

## 作業實作細節
### 1. 權限提升與邏輯漏洞 (Broken Access Control)
- **實作目標**：繞過前端驗證取得管理員權限。
- **技術手段**：使用 Burp Suite 修改伺服器回傳值，成功開啟隱藏的「報名管理」功能。

### 2. 服務漏洞串聯
- **環境**：Docker 容器化部署之 DVWA / WingFTP 靶機。
- **成果**：在無法建立反向 Shell (Reverse Shell) 的極端環境下，改用 In-band 方式輸出執行結果，證明 RCE 存在。

## 相關證照與環境維護
- **虛擬化技術**：熟練操作 VMware 上的 Kali Linux 滲透測試環境。
- **雲端資安基礎**：持有 Microsoft Certified: Azure AI Fundamentals。
