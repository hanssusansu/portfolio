# Personal Portfolio Website - User Guide

Congratulations! Your personal portfolio website is ready. This document will guide you on how to modify content, replace images, and maintain the site.

## 📁 File Structure

Your website is located in the `d:/anti test/portfolio/` folder. It primarily contains three files:

1. **`index.html`**: The skeleton of the webpage.
   - Used to adjust the order and structure of sections.
   - This is where you **replace the profile picture**.

2. **`script.js`**: The logic and **text content** of the webpage.
   - **Note!** This is the most important file. Since we have a "Chinese/English toggle" feature, all text (name, experience, details) is stored here.
   - Please edit this file to modify any text.

3. **`style.css`**: The style of the webpage.
   - Controls colors, font sizes, and layout spacing. It usually does not require major modifications.

---

## ✏️ How to Modify Text Content?

Please use any text editor (such as Notepad, Notepad++, or VS Code) to open **`script.js`**.

Find the **`const translations`** section starting around line 50. You will see a structure similar to this:

```javascript
const translations = {
    zh: {
        name: "王小明",  // <--- Modify the name here
        intro: "Digital Marketing Analyst...", 
        // ...other Chinese content
    },
    en: {
        name: "Xiao-Ming Wang", // <--- Modify the English name here
        // ...other English content
    }
};

