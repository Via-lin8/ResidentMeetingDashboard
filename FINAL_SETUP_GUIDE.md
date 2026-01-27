# 住院醫師座談會成效追蹤儀表板 - 完整設定指南

## ✅ 部署完成狀態

### 已完成的工作

1. **GitHub 儲存庫建立** ✅
   - 儲存庫名稱：ResidentMeetingDashboard
   - 用戶名：Via-lin8
   - 儲存庫 URL：https://github.com/Via-lin8/ResidentMeetingDashboard
   - 設定：Public

2. **儀表板代碼上傳** ✅
   - 2 頁面互動式應用程式
   - 首頁儀表板
   - 2025/12/24 座談會成效分析頁面

3. **Google Apps Script 整合** ✅
   - API URL 已配置
   - Google Sheets 連接已設定

4. **Google Sheets 連接** ✅
   - 試算表 ID：1tR0U9RFSTyc1O5qD-owWnbLqlHuWHm6KUoVxcKziSR0
   - 分頁：現況追蹤、出席名單
   - 資料已驗證

---

## 🚀 啟用 GitHub Pages（必須完成）

### 步驟 1：進入儲存庫設定
訪問：https://github.com/Via-lin8/ResidentMeetingDashboard
點擊 **Settings** 標籤

### 步驟 2：配置 GitHub Pages
1. 在左側菜單找到 **Pages**
2. **Source** 選擇：**Deploy from a branch**
3. **Branch** 選擇：**main**
4. **Folder** 選擇：**/ (root)**
5. 點擊 **Save**

### 步驟 3：等待部署完成
- 通常需要 1-2 分鐘
- 部署完成後會顯示綠色勾號和您的網站 URL

---

## 📍 您的儀表板 URL

部署完成後，您的儀表板將可以在以下 URL 訪問：

```
https://via-lin8.github.io/ResidentMeetingDashboard/
```

---

## 📊 儀表板功能

### 首頁儀表板

**統計卡片**
- 待決議提案數
- 進行中提案數
- 已結案提案數
- 完成率百分比

**圖表展示**
- 議題類別圓餅圖 - 各類別提案分布
- 提案狀態柱狀圖 - 各狀態提案數量

**詳細列表**
- 追蹤項目詳情 - 每個提案的完整信息
- 出席人員名單 - 座談會與會人員資訊

### 2025/12/24 座談會成效分析頁面

**統計概覽**
- 總提案數
- 待決議數量
- 進行中數量
- 已結案數量

**分析展示**
- 議題類別分析 - 帶進度條的類別統計
- 議題分布圓餅圖 - 視覺化類別比例
- 提案詳細分析 - 完整的提案信息

---

## 🔄 資料流程

```
Google Sheets（資料來源）
        ↓
Google Apps Script（資料 API）
        ↓
GitHub Pages（儀表板）
        ↓
使用者瀏覽器（顯示應用程式）
```

### 資料更新流程

1. **在 Google Sheets 中更新資料**
2. **Google Apps Script 自動讀取最新資料**
3. **儀表板每 5 分鐘自動更新一次**
4. **使用者可手動點擊「重新整理」按鈕立即更新**

---

## 🎯 使用方式

### 訪問儀表板

1. 在瀏覽器中輸入您的儀表板 URL
2. 首次載入時會自動從 Google Sheets 讀取資料
3. 頁面會顯示所有統計信息和圖表

### 頁面切換

- 點擊導航欄的按鈕在 2 個頁面之間切換
- **首頁儀表板** - 總體成效監控
- **2025/12/24 成效分析** - 詳細座談會分析

### 更新資料

- **自動更新**：每 5 分鐘自動從 Google Sheets 同步
- **手動更新**：點擊「重新整理」按鈕立即更新

---

## ⚙️ 配置選項

### 修改更新間隔

編輯 GitHub 上的 `index.html` 檔案，找到第 837 行：

```javascript
const CONFIG = {
    API_URL: 'https://script.google.com/macros/s/AKfycbwp8wbNQaU0J9SQX6r1EUdhuAvnfDgsyfSXkIjtOHtGeXgu8hSN5_jKQ9_WqpFbvhkR9g/exec',
    REFRESH_INTERVAL: 5 * 60 * 1000  // 改為其他值（單位：毫秒）
};
```

例如改為 10 分鐘：
```javascript
REFRESH_INTERVAL: 10 * 60 * 1000
```

### 修改顏色配置

編輯 `index.html` 中的 `COLORS` 物件（約第 840 行）

---

## 🐛 故障排除

### 儀表板無法載入資料

**檢查清單**：
1. 確保 GitHub Pages 已啟用
2. 檢查 Google Apps Script Web App 是否正常工作
3. 在瀏覽器控制台（F12）查看是否有錯誤訊息
4. 檢查網路連接

### 圖表無法顯示

**解決方案**：
1. 刷新頁面（Ctrl+F5）
2. 檢查 Google Sheets 中是否有資料
3. 檢查瀏覽器是否支援 JavaScript

### 頁面切換不工作

**解決方案**：
1. 檢查瀏覽器控制台是否有錯誤
2. 確保 JavaScript 已啟用
3. 清除瀏覽器快取後重試

---

## 📱 響應式設計

應用程式支援以下設備：

| 設備 | 寬度 | 支援 |
|------|------|------|
| 桌面 | ≥ 1024px | ✅ |
| 平板 | 768px - 1023px | ✅ |
| 手機 | < 768px | ✅ |

---

## 🔐 安全性

### 資料隱私
- 應用程式是公開的
- 任何人都可以訪問
- 不要在 Google Sheets 中存放敏感個人信息

### 資料備份
建議定期備份：
- Google Sheets 資料
- GitHub 儲存庫

---

## 📈 效能

### 載入時間
- 首次載入：< 3 秒
- 資料更新：< 1 秒
- 圖表渲染：< 2 秒

### 優化建議
1. 使用最新的瀏覽器
2. 清除瀏覽器快取
3. 確保網路連接穩定
4. 限制 Google Sheets 資料行數（建議 < 100 行）

---

## 📋 檢查清單

### 部署前
- [ ] GitHub 儲存庫已建立
- [ ] 儀表板代碼已上傳
- [ ] Google Apps Script URL 已配置

### 部署中
- [ ] GitHub Pages 已啟用
- [ ] 等待 1-2 分鐘部署完成

### 部署後
- [ ] 訪問儀表板 URL 驗證
- [ ] 測試資料載入
- [ ] 測試頁面切換
- [ ] 測試圖表顯示
- [ ] 測試手動更新

---

## 🎯 後續步驟

1. **立即進行**：按照上述步驟啟用 GitHub Pages
2. **部署完成後**：訪問您的儀表板 URL
3. **測試功能**：驗證所有功能是否正常工作
4. **分享儀表板**：將 URL 分享給其他人

---

## 📞 技術支援

### 常見問題
- 查看本指南的「故障排除」部分

### 需要幫助
- 檢查 GitHub 儲存庫中的文檔
- 查看瀏覽器控制台的錯誤訊息
- 驗證 Google Sheets 和 Google Apps Script 的設定

---

## 📊 系統資訊

### 技術棧
- HTML5 + CSS3 + JavaScript (Vanilla)
- Chart.js（圖表庫）
- Google Sheets（資料來源）
- Google Apps Script（資料 API）
- GitHub Pages（靜態網站託管）

### 儲存庫資訊
- **URL**：https://github.com/Via-lin8/ResidentMeetingDashboard
- **分支**：main
- **設定**：Public

### Google Sheets 資訊
- **試算表 ID**：1tR0U9RFSTyc1O5qD-owWnbLqlHuWHm6KUoVxcKziSR0
- **分頁**：現況追蹤、出席名單
- **分享設定**：公開

---

## 🎉 恭喜！

您已成功建立了一個完整的互動式儀表板系統。現在只需要：

1. 啟用 GitHub Pages
2. 訪問您的儀表板 URL
3. 開始使用！

祝您使用順利！

---

**最後更新**：2026-01-26

**儀表板 URL**：https://via-lin8.github.io/ResidentMeetingDashboard/

**GitHub 儲存庫**：https://github.com/Via-lin8/ResidentMeetingDashboard
