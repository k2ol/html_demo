---
marp: true
theme: gaia
style: |
    pre[class*="language-font-18px"] code,
    code[class*="language-font-18px"],
    pre:has(code.language-font-18px),
    code.language-font-18px {
        font-size: 18px !important;
    }
    pre[class*="language-font-12px"] code,
    code[class*="language-font-12px"],
    pre:has(code.language-font-12px),
    code.language-font-12px {
        font-size: 12px !important;
    }
        /* 設定幻燈片邊框 */
    section {
        padding: 0px 50px;
    }

---

# HTML 基礎教學

---

## HTML 是什麼？

- HTML 代表 **H**yper**T**ext **M**arkup **L**anguage
- 是用於建立網頁的標準標記語言
- 描述網頁的結構
- 由一系列的元素（elements）組成
- 這些元素告訴瀏覽器如何顯示內容

---

## HTML 文件結構

```html
<!DOCTYPE html>
<html>
<head>
    <title>頁面標題</title>
    <meta charset="UTF-8">
</head>
<body>
    <h1>我的第一個標題</h1>
    <p>我的第一個段落。</p>
</body>
</html>
```

---

## HTML 元素解析

- `<!DOCTYPE html>`: 聲明文件類型
- `<html>`: 根元素
- `<head>`: 包含文檔的元信息
- `<title>`: 定義文檔的標題
- `<meta>`: 提供關於 HTML 文檔的元數據
- `<body>`: 包含可見的頁面內容

---

## 常用 HTML 標籤

### 標題標籤
```html
<h1>這是標題 1</h1>
<h2>這是標題 2</h2>
<h3>這是標題 3</h3>
<h4>這是標題 4</h4>
<h5>這是標題 5</h5>
<h6>這是標題 6</h6>
```

---

## 段落與文本格式

```html
<p>這是一個段落。</p>
<br> <!-- 換行 -->
<hr> <!-- 水平線 -->
<strong>粗體文本</strong>
<em>斜體文本</em>
<mark>標記文本</mark>
<del>刪除線文本</del>
<ins>下劃線文本</ins>
<sub>下標</sub>
<sup>上標</sup>
```

---

## 連結與圖片

```html
<!-- 連結 -->
<a href="https://www.example.com">這是一個連結</a>

<!-- 圖片 -->
<img src="image.jpg" alt="圖片描述" width="300" height="200">
```

---

## 列表

### 無序列表
```html
<ul>
    <li>項目 1</li>
    <li>項目 2</li>
    <li>項目 3</li>
</ul>
```

### 有序列表
```html
<ol>
    <li>第一項</li>
    <li>第二項</li>
    <li>第三項</li>
</ol>
```

---

## 表格

```html
<table border="1">
    <tr>
        <th>表頭 1</th>
        <th>表頭 2</th>
    </tr>
    <tr>
        <td>行 1, 列 1</td>
        <td>行 1, 列 2</td>
    </tr>
    <tr>
        <td>行 2, 列 1</td>
        <td>行 2, 列 2</td>
    </tr>
</table>
```

---

## 表單

```html
<form action="/submit-form" method="post">
    <label for="name">姓名:</label>
    <input type="text" id="name" name="name"><br><br>
    
    <label for="email">電子郵件:</label>
    <input type="email" id="email" name="email"><br><br>
    
    <label for="message">留言:</label><br>
    <textarea id="message" name="message" rows="4" cols="50"></textarea><br><br>
    
    <input type="submit" value="提交">
</form>
```

---

## 區塊與內聯元素

### 區塊元素
- 總是從新行開始
- 佔據全部可用寬度
- 例如：`<div>`, `<h1>-<h6>`, `<p>`, `<form>`

### 內聯元素
- 不從新行開始
- 只佔用必要的寬度
- 例如：`<span>`, `<a>`, `<img>`, `<strong>`

---

## 語義化元素

```html
<header>頁面頂部區域</header>
<nav>導航區域</nav>
<main>主要內容區域</main>
<article>獨立的內容區域</article>
<section>文檔中的一個區段</section>
<aside>側邊欄內容</aside>
<footer>頁面底部區域</footer>
```

---

## HTML5 新特性

- 語義化標籤（如上述）
- 音頻和視頻支持
  ```html
  <audio controls>
      <source src="audio.mp3" type="audio/mpeg">
  </audio>
  
  <video width="320" height="240" controls>
      <source src="movie.mp4" type="video/mp4">
  </video>
  ```
- Canvas 繪圖
- 本地存儲
- 表單新元素

---

## HTML 最佳實踐

- 使用小寫標籤名
- 關閉所有 HTML 元素
- 使用引號包裹屬性值
- 添加 alt 屬性到圖片
- 避免不必要的空格和縮進
- 使用語義化標籤
- 確保文檔類型聲明
- 驗證您的 HTML 代碼

---

## 實用資源

- [W3Schools HTML 教程](https://www.w3schools.com/html/)
- [MDN Web Docs](https://developer.mozilla.org/zh-TW/docs/Web/HTML)
- [HTML 驗證器](https://validator.w3.org/)
- [HTML 參考手冊](https://www.w3schools.com/tags/default.asp)