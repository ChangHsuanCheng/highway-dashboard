# 🚗 國道與快速道路極簡即時儀表板 (Highway Real-time Dashboard)

一個專為駕駛設計、高對比、極簡且具備 PWA 離線/全螢幕支援的國道與快速道路即時路況儀表板。

點擊開啟網頁：[https://ghsuancheng.github.io]([https://ghsuancheng.github.io](https://changhsuancheng.github.io/highway-dashboard/)) *(請替換為你的實際 GitHub Pages 網址)*

---

## ✨ 核心特色 (Features)

* **🗺️ 全台國道與快速道路涵蓋**
  * 完整收錄 **國道 1 號 (中山高)** 與 **國道 3 號 (福爾摩沙高)** 全線南北雙向重點交流道與系統交流道。
  * 支援台 64 線等快速道路切換。
* **🧭 GPS 道路與方向自動辨識**
  * 透過 Haversine 球面距離演算法，自動判斷距離最近的道路並切換。
  * 獨立判定方向標籤（南下/北上、東向/西向），無需手動調整。
* **🟢 TDX 交通部即時路況連線**
  * 結合交通部 TDX 平台 Open Data，每 2 分鐘動態更新段路車速。
  * 以顏色標示路況（綠色：順暢 $\ge 80$ km/h、黃色：車多 $50\sim79$ km/h、紅色：壅塞 $<50$ km/h）。
* **📱 駕駛導航視覺與動態平滑進度**
  * **駕駛視角底線**：最下方的綠色橫線即為目前車輛行駛位置，無多餘雜訊。
  * **前方閘道平滑靠攏**：隨著 K 數推進，前方交流道卡片與黃色圓點會平滑向下推進，當距離為 `0.00 km` 時剛好扣壓於底線上，無縫過站重置。
* **🎮 物理模擬測試模式 (Simulation Mode)**
  * 內建 100~120 km/h 物理時速推進模擬器，可在室內或開發時完整測試路線切換、距離倒數與 UI 動畫。
* **💡 螢幕常亮支援 (Screen Wake Lock)**
  * 開啟網頁自動申請喚醒鎖，防止行車過程中手機螢幕自動休眠。

---

## 🛠️ 技術架構 (Tech Stack)

* **前端框架**：HTML5, Tailwind CSS (CDN), Vanilla JavaScript (原生 JS 無框架依賴)
* **資料來源**：[交通部 TDX 數位平台 Basic Open Data API](https://tdx.transportdata.tw/)
* **跨域處理**：CORS Proxy 代理轉接 (完全零 API Key 硬編碼，確保開源安全性)
* **部署方式**：GitHub Pages 單頁應用 (SPA)

---

## 🚀 快速開始 / 本地開發 (Quick Start)

由於本專案為純前端單頁應用（Single Page Application），無需安裝任何 `npm` 套件或架設 Server：

1. **Clone 本專案**：
   ```bash
   git clone [https://github.com/ghsuancheng/ghsuancheng.github.io.git](https://github.com/ghsuancheng/ghsuancheng.github.io.git)
   cd ghsuancheng.github.io
