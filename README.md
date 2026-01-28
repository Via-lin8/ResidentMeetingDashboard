# 住院醫師座談會成效追蹤儀表板

[![GitHub Pages](https://img.shields.io/badge/GitHub-Pages-blue)](https://github.com/features/pages)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## 📊 概述

這是一個基於 Manus 設計的住院醫師座談會成效追蹤儀表板。採用莫蘭迪色系設計，提供實時的座談會成效監控和追蹤管理。

### ✨ 主要特點

- 🎨 **莫蘭迪色系設計** - 專業、優雅的視覺風格
- 📊 **實時資料更新** - 自動從 Google Sheets 同步資料
- 📈 **豐富的圖表** - 柱狀圖展示議題類別統計
- 📋 **完整追蹤詳情** - 每個提案的完整進度記錄
- 📱 **響應式設計** - 完美支援各種設備
- ⚡ **快速載入** - 靜態網站，無伺服器成本
- 🌐 **公開訪問** - 無需登入

---

## 🚀 快速開始

### 部署到 GitHub Pages（5 分鐘）

#### 1. 準備檔案
```bash
mkdir ResidentMeetingDashboard
cd ResidentMeetingDashboard
```

複製以下檔案到此資料夾：
- `index.html` - 主應用程式
- `README.md` - 專案說明

#### 2. 上傳到 GitHub
```bash
git init
git add .
git commit -m "Initial commit: Add resident meeting dashboard"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ResidentMeetingDashboard.git
git push -u origin main
```

#### 3. 啟用 GitHub Pages
- 進入儲存庫 Settings > Pages
- 選擇 "Deploy from a branch" > "main" > "/ (root)"
- 點擊 Save

#### 4. 訪問您的儀表板
```
https://YOUR_USERNAME.github.io/ResidentMeetingDashboard/
```

---

## 📖 功能說明

### 統計卡片
- **整體達成率** - 已結案提案佔比
- **待決議** - 待決議提案數量
- **進行中** - 進行中提案數量
- **已結案** - 已結案提案數量

### 圖表展示
- **議題類別統計** - 柱狀圖展示各類別提案數量

### 追蹤列表
- 所有提案的詳細信息
- 包括提案者、負責窗口、追蹤進度等
- 按狀態分色展示（待決議、進行中、已結案）

---

## 🔄 資料更新

### 自動更新
- 首次載入時更新
- 每 5 分鐘自動更新一次
- 支援手動刷新

### 更新流程
1. 在 Google Sheets 中更新資料
2. Google Apps Script 讀取最新資料
3. 應用程式自動載入並顯示

**更新延遲**：通常不超過 5 分鐘

---

## 📱 響應式設計

| 設備 | 寬度 | 支援 |
|------|------|------|
| 桌面 | ≥ 1024px | ✅ |
| 平板 | 768px - 1023px | ✅ |
| 手機 | < 768px | ✅ |

---

## 🛠️ 技術棧

- **HTML5** - 語義化頁面結構
- **CSS3** - 現代樣式和響應式設計
- **JavaScript (Vanilla)** - 無框架、純原生代碼
- **Chart.js** - 專業圖表庫
- **Google Sheets** - 資料存儲
- **Google Apps Script** - 資料 API
- **GitHub Pages** - 靜態網站託管

---

## 🎨 設計特點

### 色彩方案
- **待決議**：#b8a898（莫蘭迪棕）
- **進行中**：#9ba8b8（莫蘭迪藍）
- **已結案**：#a8b8a0（莫蘭迪綠）

### 排版
- **標題**：Noto Sans TC 700 weight
- **正文**：Noto Sans TC 400 weight
- **強調**：Noto Sans TC 600 weight

### 互動效果
- 卡片懸停效果 - 上升 + 陰影
- 平滑過渡動畫
- 按鈕反饋效果

---

## ⚙️ 配置

### 修改 API URL

編輯 `index.html` 第 353 行：

```javascript
const CONFIG = {
    API_URL: 'https://script.google.com/macros/s/YOUR_DEPLOYMENT_ID/exec',
    REFRESH_INTERVAL: 5 * 60 * 1000
};
```

### 修改更新間隔

改變 `REFRESH_INTERVAL` 值（單位：毫秒）：

```javascript
REFRESH_INTERVAL: 10 * 60 * 1000  // 改為 10 分鐘
```

---

## 🐛 故障排除

### 應用程式無法載入資料

**檢查清單**：
- [ ] 檢查 `API_URL` 是否正確
- [ ] 確保 Google Apps Script Web App 已部署
- [ ] 檢查瀏覽器控制台（F12）是否有錯誤
- [ ] 檢查網路連接

### 圖表無法顯示

**解決方案**：
1. 刷新頁面（Ctrl+F5）
2. 檢查 Google Sheets 中是否有資料
3. 檢查瀏覽器是否支援 JavaScript

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

## 🔐 安全性

### 資料隱私
- 應用程式是公開的
- 任何人都可以訪問
- 不要存放敏感個人信息

### 資料備份
定期備份：
- Google Sheets 資料
- GitHub 儲存庫

---

## 📞 支援

- 📖 [GitHub Pages 官方文檔](https://docs.github.com/en/pages)
- 🐛 [GitHub Issues](../../issues)
- 💬 [GitHub Discussions](../../discussions)

---

## 📝 版本歷史

### 版本 2.0（2026-01-28）
- ✅ 採用 Manus 設計
- ✅ 莫蘭迪色系
- ✅ 優化的追蹤列表
- ✅ 改進的圖表展示

### 版本 1.0（2026-01-26）
- ✅ 初始版本發佈
- ✅ 基本功能實現

---

## 📄 許可證

此專案採用 MIT 許可證。

---

## 🙏 致謝

感謝 Manus 平台提供的優秀設計靈感。

---

**最後更新**：2026-01-28

**官方應用程式**：https://residash-f8ahzkga.manus.space

**GitHub 儲存庫**：https://github.com/Via-lin8/ResidentMeetingDashboard
