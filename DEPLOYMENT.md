# 音樂脈動-Sonic Pulse 入口網站部署指南

## 📁 檔案結構
```
music-portal/
├── index.html          # 主要網頁檔案
├── config.js           # 配置檔案（重要！）
└── DEPLOYMENT.md       # 部署說明檔案
```

## 🚀 快速部署

### 1. Railway 部署
1. 將整個 `music-portal` 資料夾上傳到 Railway
2. Railway 會自動偵測並部署為靜態網站
3. 部署完成後會獲得一個 Railway 網域

### 2. 自定義網域設定
當你想要使用自定義網域時，只需要：

1. **修改 `config.js` 檔案**：
   ```javascript
   const CONFIG = {
       site: {
           domain: 'your-custom-domain.com', // 改為你的網域
           // ... 其他設定
       }
   };
   ```

2. **在 Railway 設定自定義網域**：
   - 進入 Railway 專案設定
   - 點擊 "Domains" 標籤
   - 添加你的自定義網域
   - 按照指示設定 DNS 記錄

## 🔧 配置管理

### 工具連結更新
所有工具連結都在 `config.js` 中集中管理：

```javascript
tools: {
    audioVisualizer: 'https://audio-visualizer-production.up.railway.app/',
    youtubeSEO: 'https://youtube-title-seo-production.up.railway.app/',
    fontEffects: 'https://font-effects-generator-production.up.railway.app/',
    // ... 其他工具
}
```

### 社交連結更新
YouTube 頻道和 PayPal 連結也在配置檔案中：

```javascript
social: {
    youtube: 'https://www.youtube.com/@%E9%9F%B3%E6%A8%82%E8%84%88%E5%8B%95SonicPulse',
    paypal: 'https://www.paypal.com/ncp/payment/PK49RJYSTAV6Y',
    email: 'contact@sonicpulse.com'
}
```

## 📝 更新流程

### 當工具連結改變時：
1. 編輯 `config.js` 檔案
2. 更新對應的 URL
3. 重新部署到 Railway
4. 網站會自動使用新的連結

### 當需要更改網域時：
1. 在 Railway 設定新的自定義網域
2. 更新 `config.js` 中的網域設定
3. 重新部署
4. 設定 DNS 記錄指向 Railway

## 🎨 自定義修改

### 修改統計資料
在 `config.js` 中更新：
```javascript
stats: {
    subscribers: '1000+',
    musicWorks: '50+',
    musicStyles: '18'
}
```

### 修改網站描述
在 `config.js` 中更新：
```javascript
site: {
    title: '你的新標題',
    description: '你的新描述',
    // ...
}
```

## 🔍 SEO 優化

網站已包含完整的 SEO 標籤：
- Meta 描述和關鍵字
- Open Graph 標籤（Facebook 分享）
- Twitter Card 標籤
- 結構化資料

## 📱 響應式設計

網站已針對以下裝置優化：
- 桌面電腦 (1200px+)
- 平板電腦 (768px - 1199px)
- 手機 (320px - 767px)

## 🚀 效能優化

- 使用 CDN 載入字體和圖標
- 圖片優化和延遲載入
- CSS 和 JavaScript 最小化
- 快取策略優化

## 📞 技術支援

如有問題，請檢查：
1. Railway 部署日誌
2. 瀏覽器開發者工具控制台
3. 網路連線狀態
4. 配置檔案格式是否正確

---

**🎵 用 ❤️ 為音樂創作者打造 | 音樂脈動-Sonic Pulse**
