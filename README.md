# 住院醫師座談會成效追蹤系統

[![GitHub Pages](https://img.shields.io/badge/GitHub-Pages-blue)](https://github.com/features/pages)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![Last Updated](https://img.shields.io/badge/Last%20Updated-2026--01--26-blue)]()

## 📊 概述

住院醫師座談會成效追蹤系統是一個完整的互動式多頁面應用程式，用於實時監控座談會提案進度與成效。

### ✨ 主要特點

- 🎯 **2 個互動頁面** - 首頁儀表板 + 詳細分析頁面
- 🔄 **實時資料更新** - 自動從 Google Sheets 同步資料
- 📈 **豐富的圖表** - 圓餅圖、柱狀圖、進度條等多種可視化
- 📋 **完整追蹤詳情** - 每個提案的完整進度記錄
- 👥 **出席人員管理** - 座談會與會人員資訊展示
- 📱 **響應式設計** - 完美支援各種設備
- ⚡ **快速載入** - 靜態網站，無伺服器成本
- 🌐 **公開訪問** - 無需登入

---

## 🚀 快速開始

### 最快的部署方式（5 分鐘）

#### 1. 準備檔案
```bash
mkdir resident-meeting-dashboard
cd resident-meeting-dashboard
```

複製以下檔案到此資料夾：
- `index.html`
- `README.md`

#### 2. 上傳到 GitHub
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/resident-meeting-dashboard.git
git push -u origin main
```

#### 3. 啟用 GitHub Pages
- 進入儲存庫 Settings > Pages
- 選擇 "Deploy from a branch" > "main" > "/ (root)"
- 點擊 Save

#### 4. 配置 API URL
編輯 `index.html` 第 552 行，將 `API_URL` 替換為您的 Google Apps Script Web App URL

#### 完成！
訪問：`https://YOUR_USERNAME.github.io/resident-meeting-dashboard/`

詳細步驟請參考 [GITHUB_MULTIPAGE_DEPLOYMENT.md](GITHUB_MULTIPAGE_DEPLOYMENT.md)

---

## 📖 頁面功能

### 📊 首頁儀表板

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

### 📈 詳細分析頁面

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

## 🎨 設計特點

### 色彩方案
- 主色調：藍色（#4a90e2）
- 成功色：綠色（#27ae60）
- 警告色：橙色（#f39c12）
- 危險色：紅色（#e74c3c）

### 排版
- 標題：大號、加粗、深色
- 正文：中等大小、易讀、灰色
- 標籤：小號、加粗、彩色背景

### 互動效果
- 卡片懸停效果 - 上升 + 陰影
- 平滑頁面轉換 - 淡入動畫
- 按鈕反饋 - 顏色變化
- 圖表動畫 - 平滑繪製

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

## 📋 檔案結構

```
resident-meeting-dashboard/
├── index.html                          # 主應用程式（HTML + CSS + JS）
├── README.md                           # 專案說明
├── GITHUB_MULTIPAGE_DEPLOYMENT.md      # 詳細部署指南
├── GITHUB_QUICK_START.md               # 快速開始指南
├── DASHBOARD_USER_GUIDE.md             # 使用指南
└── [其他文檔]
```

---

## 🎯 使用方式

### 基本操作

1. **訪問應用程式**
   - 在瀏覽器中輸入應用程式 URL

2. **瀏覽首頁儀表板**
   - 查看統計卡片
   - 查看圖表
   - 向下滾動查看詳細列表

3. **切換到詳細分析頁面**
   - 點擊導航欄的「2025/12/24 成效分析」按鈕

4. **更新資料**
   - 點擊「重新整理」按鈕
   - 或等待自動更新

### 進階操作

- **搜尋內容** - 使用瀏覽器的查找功能（Ctrl+F）
- **列印頁面** - 使用瀏覽器的列印功能（Ctrl+P）
- **截圖** - 使用瀏覽器的截圖工具

---

## ⚙️ 配置

### 修改 API URL

編輯 `index.html` 第 552 行：

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

### 修改顏色

編輯 `index.html` 中的 `COLORS` 物件

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

### 頁面切換不工作

**解決方案**：
1. 檢查瀏覽器控制台是否有錯誤
2. 確保 JavaScript 已啟用
3. 清除瀏覽器快取

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
- 不要存放敏感個人信息
- 如需限制訪問，使用 GitHub 私有儲存庫

### 資料備份
定期備份：
- Google Sheets 資料
- GitHub 儲存庫

---

## 🤝 貢獻

歡迎提交 Issue 和 Pull Request！

### 報告問題
在 GitHub 上提交 Issue，包含：
- 問題描述
- 重現步驟
- 預期結果
- 實際結果

### 提交改進
1. Fork 此儲存庫
2. 建立新分支
3. 提交更改
4. 提交 Pull Request

---

## 📝 許可證

此專案採用 MIT 許可證。

---

## 📞 支援

- 📖 [詳細部署指南](GITHUB_MULTIPAGE_DEPLOYMENT.md)
- 👥 [使用指南](DASHBOARD_USER_GUIDE.md)
- 🐛 [GitHub Issues](../../issues)

---

## 🎯 未來計劃

- [ ] 新增篩選和搜尋功能
- [ ] 新增資料匯出功能（PDF、Excel）
- [ ] 新增深色模式
- [ ] 新增多語言支援
- [ ] 新增通知功能
- [ ] 新增更多分析圖表

---

## 📊 統計

- 📄 代碼行數：~2000 行
- 🎨 CSS 類別：60+ 個
- 📦 外部依賴：1 個（Chart.js）
- ⚡ 首屏加載時間：< 3 秒

---

## 🙏 致謝

感謝所有貢獻者和使用者的支持！

---

## 📅 更新日誌

### 版本 1.0（2026-01-26）

- ✅ 初始版本發佈
- ✅ 2 個互動頁面
- ✅ 首頁儀表板
- ✅ 詳細分析頁面
- ✅ 圓餅圖和柱狀圖
- ✅ 進度條視覺化
- ✅ 響應式設計
- ✅ 自動資料更新
- ✅ GitHub Pages 部署

---

**最後更新**：2026-01-26

**維護者**：[您的名稱]

**官方應用程式**：[您的應用程式 URL]

---

## 快速連結

- 🌐 [應用程式首頁](https://your-username.github.io/resident-meeting-dashboard/)
- 📖 [部署指南](GITHUB_MULTIPAGE_DEPLOYMENT.md)
- 👥 [使用指南](DASHBOARD_USER_GUIDE.md)
- 🐛 [報告問題](../../issues)
- 💬 [討論](../../discussions)
