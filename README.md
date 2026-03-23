# 🏠 家庭健康管理系統

部署在 GitHub Pages，資料儲存於私人 GitHub Gist。

## 🚀 部署步驟

### 第一步：建立 GitHub Repository

1. 登入 [GitHub](https://github.com)
2. 點擊右上角 **New repository**
3. Repository name 填入：`family-health`
4. 選擇 **Public**（GitHub Pages 免費方案需公開，但資料存在私人 Gist，不會外洩）
5. 點擊 **Create repository**

### 第二步：上傳檔案

方法 A（網頁上傳，最簡單）：
1. 進入剛建立的 repository
2. 點 **Add file → Upload files**
3. 將 `index.html` 拖入上傳
4. 點 **Commit changes**

方法 B（使用 Git）：
```bash
git clone https://github.com/你的帳號/family-health.git
cp index.html family-health/
cd family-health
git add .
git commit -m "初始化家庭健康管理系統"
git push
```

### 第三步：啟用 GitHub Pages

1. 進入 repository → **Settings** → 左側選單 **Pages**
2. Source 選 **Deploy from a branch**
3. Branch 選 **main**，資料夾選 **/ (root)**
4. 點 **Save**
5. 等待約 1 分鐘，網址會顯示在頁面上：
   `https://你的帳號.github.io/family-health`

### 第四步：設定 Gist Token（首次使用）

1. 前往 https://github.com/settings/tokens/new?scopes=gist&description=家庭健康管理
2. 勾選 **gist** 權限
3. 點 **Generate token** 並複製
4. 開啟您的健康管理網頁
5. 將 Token 貼入設定欄位，點「連線並初始化」

---

## 📱 跨裝置使用

- **換裝置時**：開啟網頁後，點右上角「☁ 載入」即可從 Gist 同步最新資料
- **每次新增紀錄**後，系統會自動同步到 Gist
- **同一個 Gist Token** 可在多台裝置使用

## 🔒 隱私說明

- Gist 設定為 **Secret（私人）**，只有知道網址的人才能看到
- GitHub Token 僅儲存在您自己的瀏覽器 `localStorage`，不上傳至任何伺服器
- 建議每隔數月更新一次 Token

## 📁 檔案結構

```
family-health/
└── index.html    ← 整個系統（單一檔案）
└── README.md     ← 說明文件
```
