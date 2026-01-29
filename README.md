# 個人履歷作品集 - 使用說明書

恭喜您！您的個人履歷網站已經建置完成。這份文件將引導您如何修改內容、替換圖片以及日後維護。

## 📁 檔案結構說明

您的網站位於 `d:/anti test/portfolio/` 資料夾中，主要包含三個檔案：

1.  **`index.html`**：網頁的骨架。
    -   用來調整區塊順序、結構。
    -   **替換大頭照**的位置在這裡。
2.  **`script.js`**：網頁的邏輯與**文字內容**。
    -   **注意！** 這是最重要的檔案。因為我們有「中/英切換」功能，所以所有的文字（姓名、經歷、專長詳細說明）都存放在這裡。
    -   若要修改文字，請編輯此檔案。
3.  **`style.css`**：網頁的樣式。
    -   控制顏色、字體大小、版面距離。通常不需要大幅修改。

---

## ✏️ 如何修改文字內容？

請使用任何文字編輯器（如 Notepad, Notepad++, VS Code）打開 **`script.js`**。

找到約第 50 行開始的 **`const translations`** 區塊。您會看到類似這樣的結構：

```javascript
const translations = {
    zh: {
        name: "王小明",  // <--- 修改這裡的名字
        intro: "數位行銷分析師...", 
        // ...其他中文內容
    },
    en: {
        name: "Xiao-Ming Wang", // <--- 修改這裡的英文名字
        // ...其他英文內容
    }
};
```

*   **`zh`** 代表中文內容，**`en`** 代表英文內容。
*   請直接修改引號 `""` 內的文字即可。
*   **小提醒**：小心不要刪掉引號或逗號。

---

## 🖼️ 如何替換大頭照？

請打開 **`index.html`**。

找到約第 16 行的 `profile-pic-placeholder` 區塊：

```html
<div class="profile-pic-placeholder">
    <!-- 之後替換成真實圖片 -->
</div>
```

請將上述整段 `div` 替換成您的圖片標籤 `<img>`：

```html
<!-- 範例：將圖片命名為 photo.jpg 並放在同一個資料夾 -->
<img src="photo.jpg" alt="我的照片" style="width: 150px; height: 150px; border-radius: 50%; object-fit: cover; margin-bottom: 1.5rem;">
```

---

## 🚀 如何開啟網站？

只要直接雙擊 **`index.html`** 檔案，您的瀏覽器就會打開網頁了！
由於這是純靜態網頁，您不需要安裝任何伺服器軟體。

---

## 💡 進階修改

*   **修改顏色**：在 `style.css` 中搜尋 `background-color` 或 `color` 來調整黑白配色。
*   **增加/減少清單**：
    *   若要新增經歷，請在 `index.html` 複製一段 `<div class="job-item ...">...</div>`，並記得在 `script.js` 的 `translations` 中加入對應的 key (例如 `exp_3_role`)。

祝您使用愉快！
