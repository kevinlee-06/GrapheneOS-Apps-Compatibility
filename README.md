# GrapheneOS App 相容性紀錄

> **設備：** Pixel 9a (tegu) | **更新日期：** 2026-02-26

---

## 應用程式相容性總表

| App 名稱 | 來源 | 狀態 | Play 服務 | 備註 |
| --- | --- | --- | --- | --- |
| **Play 服務** | GrapheneOS | 🟡 部分 | 需要 |  |
| **Play 商店** | GrapheneOS | 🟡 部分 | 需要 | 須手動點擊授權安裝 |
| **[街口支付](#街口支付)** | Play Store | 🟡 部分 | 需要 | SIM 卡驗證失敗，改用交易密碼驗證 |
| **[一卡通](#一卡通-money)** | Play Store | 🟡 部分 | 需要 |  |
| **Google 文件** | Play Store | 🟡 部分 | 需要 | |
| **Google 訊息** | Play Store | 🟡 部分 | \- | [RCS 設定](https://grapheneos.org/usage#rcs) |
| **[CUBE](#國泰世華-cube)** | Play Store | 🔴 閃退 | 需要 | 顯示設備遭破解，必須禁用「開發人員選項」 |
| **[中國信託](#中國信託)** | Play Store | 🔴 閃退 | 需要 | 無解，顯示連線有風險 |
| **[台灣行動支付](#台灣行動支付)** | Play Store | 🔴 閃退 | \- | 無解，閃退、SIM 卡驗證失敗 |
| **麥當勞** | Play Store | 🔴 閃退 | 需要 | |
| **[Google 錢包](#google-錢包)** | Play Store | 🔴 半殘 | 需要 | |
| **行動郵局** | Play Store | 🟢 正常 | \- | |
| **將來銀行** | Play Store | 🟢 正常 | \- | |
| **icash Pay** | Play Store | 🟢 正常 | 需要 | |
| **國泰證券** | Play Store | 🟢 正常 | 通知 | |
| **全支付** | Play Store | 🟢 正常 | 通知 | |
| **[悠遊付](#悠遊付)** | Play Store | 🟢 正常 | 進階功能 | NFC「嗶乘車」能用 |
| **Line** | Play Store | 🟢 正常 | 通知 | |
| **Line Pay** | Play Store | 🟢 正常 | \- | |
| **Line Bank** | Play Store | 🟢 正常 | \- | |
| **Spotify** | Play Store | 🟢 正常 | \- | 無損音質正常運作 |
| **Netflix** | Play Store | 🟢 正常 | 通知 |  |
| **Proton Mail** | Apk | 🟢 正常 | \- | |
| **Proton Calendar** | Apk | 🟢 正常 | \- | |
| **Aurora Store** | Droid-ify (Apk) | 🟢 正常 | \- | |
| **Brave Browser** | Droid-ify (Apk) | 🟢 正常 | \- | |
| **Fossify\*** | Droid-ify (Apk) | 🟢 正常 | \- | |
| **Google 相機** | Play Store | 🟢 正常 | \- | |
| **Gboard** | Play Store | 🟢 正常 | 進階功能 | |
| **Google 翻譯** | Play Store | 🟢 正常 | 進階功能 | |
| **Galaxy Wearable** | Play Store | 🟢 正常 | 需要 | |

### 國泰世華 (CUBE)
- 狀態：🔴 閃退
- 錯誤代碼：`[AX05]`
- V-Shield：`[ERROR] code:-207, msg:Device is risky [Rooted/Hooked/Simulator/Emulator/Debugger]`
- 調用系統級 GMS 與 Integrity API 異常
> 嘗試重複開關 CUBE App 與開發人員選項，偶爾有機會跳過 `[AX05]` 警告
- 可使用 [CUBE 網銀](https://www.cathaybk.com.tw/mybank)(只能約轉)與[友善個人網路銀行](https://accessibility.cathaybk.com.tw/mybank/Classics)(非約轉 SMS 驗證)

### 中國信託
- 狀態：🔴 閃退
- SELinux 權限遭拒
- 調用系統級 GMS 與 Integrity API 異常
- idgate SDK 報錯
- App 自主退出（顯示連線有風險）

### 將來銀行 (Next Bank)：
- 狀態：🟢 正常
- SELinux 權限遭拒
- 調用系統級 GMS 與 Integrity API 異常
- Log 充滿報錯，但仍放行（App 沒顯示任何警告）

### 一卡通 MONEY
- 狀態：🟡 部分
- 說明：需要 Play 服務，Play Integrity Basic 不強制

### 悠游付
- 狀態：🟢 正常
- 說明：功能正常，啟用 Play 服務才能存店家清單

### 街口支付
- 狀態：🟡 部分
- 說明：無法執行電信 MID 門號驗證，可改用交易密碼驗證

### 台灣行動支付
- 狀態：🔴 閃退
- 說明：無法執行電信 MID 門號驗證

### Google 錢包
- 狀態：🟡 部分
- 無法感應支付
<img src="./GPay.png" style="width: 30%"/>
