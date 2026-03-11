# GrapheneOS App 相容性紀錄
## App 清單
### 更新日期：2026/03/11
> Pixel 9a (tegu) | 2026030701
- ✅ 中國信託
- ✅ 國泰世華
- ✅ 王道銀行
- ✅ 台灣銀行
- ✅ 台新銀行
- ✅ Richart
- ✅ 台北富邦銀行
- ✅ 兆豐銀行
- ✅ 永豐銀行
- ✅
- ✅
- ✅ 玉山 Wallet
- 🈲 玉山銀行
- 🈲 星展 Card+ TW
### 更新日期：2026/02/26
> Pixel 9a (tegu)
- ✅ 街口支付：SIM 卡驗證失敗，改用交易密碼驗證
- ✅ 一卡通
- ✅ 行動郵局
- ✅ 悠遊付
- ✅ icash Pay
- ✅ 全支付
- ✅ Line
- ✅ Line Pay
- ✅ Line Bank
- ✅ 將來銀行
- ✅ 國泰證券
- ✅ 全支付
- ✅ Netflix
- ✅ Spotify
- ✅ Galaxy Wearable
- ✅ Google 訊息：[RCS 設定](https://grapheneos.org/usage#rcs)
- 🈲 台灣行動支付：不支援，SIM 卡驗證失敗
- 🈲 麥當勞：不支援，Integrity 沒過
- 🈲 Google 錢包：不支援
- ~~🈲 國泰世華：不支援，顯示設備遭破解~~
- ~~🈲 中國信託：不支援，顯示連線有風險~~

## 詳細紀錄 
### 更新日期：2026/03/11
#### 國泰世華 (CUBE)
- 狀態：🟢 運作正常
- SELinux 權限遭拒
- 可成功成功建立加密連線，log 中並未出現風險評估失敗的紀錄

#### 中國信託
- 狀態：🟢 運作正常
- SELinux 權限遭拒
- 調用系統級 GMS 與 Integrity API 異常
- 可成功成功建立加密連線，有大量錯誤但放行

### 更新日期：2026/02/26
#### 國泰世華 (CUBE) (已過期)
- 狀態：🔴 閃退
- 錯誤代碼：`[AX05]`
- V-Shield：`[ERROR] code:-207, msg:Device is risky [Rooted/Hooked/Simulator/Emulator/Debugger]`
- 調用系統級 GMS 與 Integrity API 異常
> 嘗試重複開關 CUBE App 與開發人員選項，偶爾有機會跳過 `[AX05]` 警告
- 可使用 [CUBE 網銀](https://www.cathaybk.com.tw/mybank)(只能約轉)與[友善個人網路銀行](https://accessibility.cathaybk.com.tw/mybank/Classics)(非約轉 SMS 驗證)

#### 中國信託 (已過期)
- 狀態：🔴 閃退
- SELinux 權限遭拒
- 調用系統級 GMS 與 Integrity API 異常
- idgate SDK 報錯
- App 自主退出（顯示連線有風險）
