# GitHub Pages 啟用指南

## 📍 您的儀表板資訊

- **GitHub 用戶名**：Via-lin8
- **儲存庫名稱**：ResidentMeetingDashboard
- **儲存庫 URL**：https://github.com/Via-lin8/ResidentMeetingDashboard
- **儀表板 URL**（部署後）：https://via-lin8.github.io/ResidentMeetingDashboard/

---

## 🚀 啟用 GitHub Pages 的步驟

### 步驟 1：進入儲存庫設定

1. 訪問您的儲存庫：
   ```
   https://github.com/Via-lin8/ResidentMeetingDashboard
   ```

2. 點擊頁面頂部的 **Settings** 標籤

### 步驟 2：找到 Pages 設定

1. 在左側菜單中找到 **Pages**（通常在下方）
2. 點擊 **Pages**

### 步驟 3：配置 GitHub Pages

1. 在 **Source** 部分：
   - 點擊下拉菜單
   - 選擇 **Deploy from a branch**

2. 在 **Branch** 部分：
   - 第一個下拉菜單選擇：**main**
   - 第二個下拉菜單選擇：**/ (root)**

3. 點擊 **Save** 按鈕

### 步驟 4：等待部署完成

1. 頁面會顯示部署狀態
2. 通常需要 1-2 分鐘
3. 部署完成後會顯示綠色勾號和您的網站 URL

---

## ✅ 部署完成後

### 訪問您的儀表板

部署完成後，您可以在以下 URL 訪問儀表板：

```
https://via-lin8.github.io/ResidentMeetingDashboard/
```

### 配置 API URL

1. 進入儲存庫的 **index.html** 檔案
2. 點擊編輯圖標（鉛筆圖標）
3. 找到第 552 行的 `API_URL`：
   ```javascript
   const CONFIG = {
       API_URL: 'https://script.google.com/macros/s/AKfycbwp8wbNQaU0J9SQX6r1EUdhuAvnfDgsyfSXkIjtOHtGeXgu8hSN5_jKQ9_WqpFbvhkR9g/exec',
       REFRESH_INTERVAL: 5 * 60 * 1000
   };
   ```

4. 將 `API_URL` 替換為您的 Google Apps Script Web App URL：
   ```javascript
   const CONFIG = {
       API_URL: 'https://script.google.com/macros/s/YOUR_DEPLOYMENT_ID/exec',
       REFRESH_INTERVAL: 5 * 60 * 1000
   };
   ```

5. 點擊 **Commit changes** 保存

### 驗證部署

1. 訪問您的儀表板 URL
2. 檢查頁面是否正確載入
3. 點擊「重新整理」按鈕測試資料載入

---

## 🎯 完整檢查清單

- [ ] 進入儲存庫設定
- [ ] 找到 Pages 設定
- [ ] 選擇 "Deploy from a branch"
- [ ] 選擇 "main" 分支和 "/ (root)" 資料夾
- [ ] 點擊 Save
- [ ] 等待 1-2 分鐘部署完成
- [ ] 訪問儀表板 URL 驗證
- [ ] 配置 Google Apps Script API URL
- [ ] 測試儀表板功能

---

## 📸 視覺指南

### Settings 頁面
```
Repository → Settings → Pages
```

### Source 配置
```
Source: Deploy from a branch
Branch: main
Folder: / (root)
```

### 部署狀態
```
✓ Your site is published at https://via-lin8.github.io/ResidentMeetingDashboard/
```

---

## 🔧 常見問題

### Q1：部署需要多長時間？

**A**：通常 1-2 分鐘。如果超過 5 分鐘，請檢查設定是否正確。

### Q2：如何知道部署是否成功？

**A**：
- 在 Pages 設定頁面會顯示綠色勾號
- 會顯示您的網站 URL
- 訪問 URL 能看到儀表板

### Q3：部署失敗怎麼辦？

**A**：
1. 檢查是否選擇了 "main" 分支
2. 檢查是否選擇了 "/ (root)" 資料夾
3. 檢查儲存庫是否為 Public
4. 等待 5 分鐘後重試

### Q4：如何更新儀表板？

**A**：
1. 編輯 GitHub 上的檔案
2. 提交更改
3. GitHub Pages 會自動重新部署（通常 1-2 分鐘）

### Q5：如何自訂域名？

**A**：
1. 在儲存庫中建立 `CNAME` 檔案
2. 在檔案中輸入您的域名
3. 在域名提供商配置 DNS 記錄

詳細步驟：https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

---

## 📞 需要幫助？

- 📖 [GitHub Pages 官方文檔](https://docs.github.com/en/pages)
- 🐛 [GitHub 支援](https://support.github.com)
- 💬 [GitHub 社群論壇](https://github.community)

---

## 下一步

1. ✅ 啟用 GitHub Pages
2. ✅ 訪問儀表板 URL
3. ✅ 配置 Google Apps Script API URL
4. ✅ 測試儀表板功能
5. ✅ 分享您的儀表板

祝您使用順利！
