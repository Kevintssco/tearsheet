# 公司 PDF 搜尋（Cloudflare R2 + Excel 自動搜尋 + 隱私保護版）

✅ 支援 Excel 超連結自動搜尋  
✅ 防止搜尋引擎收錄  
✅ 可直接部署到 Netlify

---

## 📁 檔案結構
.
├── index.html      ← 主頁（含 meta noindex、Excel 查詢支援）
├── index.json      ← 公司與 PDF 對應資料
├── robots.txt      ← 禁止搜尋引擎爬取
├── _headers        ← Netlify 伺服器層禁止索引
└── README.txt      ← 使用教學

---

## ☁️ 使用步驟

1. 將 PDF 上傳至 Cloudflare R2 並開啟 Public Access  
2. 複製每個 PDF 的 Public URL  
3. 編輯 index.json，將範例網址換成你的實際連結  
4. 上傳整個資料夾到 Netlify → Deploy manually

---

## 🧩 Excel 公式範例

在 Excel B 欄輸入：

=HYPERLINK("https://你的網站.netlify.app/?q=" & ENCODEURL(A2), "搜尋")

→ 點擊後會自動在網站搜尋欄填入 A2 的文字並執行搜尋。
