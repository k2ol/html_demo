---
marp: true
theme: m_blue
headingDivider: 2
paginate: true
---

# HTML 基礎教學
<!-- _class: trans -->
<!-- _footer: "" -->

## HTML 是什麼？
- HTML 代表 **H**yper**T**ext **M**arkup **L**anguage
- 是用於建立網頁的標準標記語言
- 描述網頁的結構
- 由一係列的元素（elements）組成
- 這些元素告訴瀏覽器如何顯示內容



## HTML 文件結構

```html
<!DOCTYPE html>
<html>
<head>
    <title>頁麵標題</title>
    <meta charset="UTF-8">
</head>
<body>
    <h1>我的第一個標題</h1>
    <p>我的第一個段落。</p>
</body>
</html>
```



## HTML 元素解析

- `<!DOCTYPE html>`: 聲明文件類型
- `<html>`: 根元素
- `<head>`: 包含文檔的元信息
- `<title>`: 定義文檔的標題
- `<meta>`: 提供關於 HTML 文檔的元數據
- `<body>`: 包含可見的頁麵內容



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

## 連結與圖片

```html
<!-- 連結 -->
<a href="https://www.example.com">這是一個連結</a>

<!-- 圖片 -->
<img src="image.jpg" alt="圖片描述" width="300" height="200">
```

## 列表

<!-- _class: cols-2 -->

<div class=ldiv>

#### 無序列表
```html
<ul>
    <li>項目 1</li>
    <li>項目 2</li>
    <li>項目 3</li>
</ul>
```

</div>

<div class=rdiv>

#### 有序列表
```html
<ol>
    <li>第一項</li>
    <li>第二項</li>
    <li>第三項</li>
</ol>
```

</div>

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

## 練習
<!-- _class: cols-2 -->

<div class="ldiv">

```html
01 <h1>hi h1</h1>
02 <h2>hi h2</h2>
03 <h3>hi h3</h3>
04 <h4>hi h4</h4>
05 <h5>hi h5</h5>
06 <p>text</p>
07 <a href="https://www.gogole.com">Google</a>
08 <img src="https://www.python.org/static/img/psf-logo.png" />
09 <ul>
10 <li>item 1</li>
11 <li>item 2</li>
12 </ul>
13 <ol>
14 <li>item 1</li>
15 <li>item 2</li>
16 </ol>
```
</div>
<div class="rdiv">

```html
17 <table border="1">
18  <tr>
19    <th>1</th> 
20    <th>2</th>
21    </tr>
22 <tr>
23    <td>3</td> 
24    <td>4</td>
25    </tr>
26 </table>
27 <form action="" method="">
28 <label>Name</lable> <input type="text"><br>
29 <label>E-mail</lable> <input type="email"><br>
30 <input type="password"><br>
31 <input type="submit" value="Submit">
32 </form>

```
</div>

## 區塊與內聯元素

### 區塊元素
- 總是從新行開始
- 佔據全部可用寬度
- 例如：`<div>`, `<h1>-<h6>`, `<p>`, `<form>`

### 內聯元素
- 不從新行開始
- 隻佔用必要的寬度
- 例如：`<span>`, `<a>`, `<img>`, `<strong>`



## 語義化元素

```html
<header>頁麵頂部區域</header>
<nav>導航區域</nav>
<main>主要內容區域</main>
<article>獨立的內容區域</article>
<section>文檔中的一個區段</section>
<aside>側邊欄內容</aside>
<footer>頁麵底部區域</footer>
```

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

## HTML 關鍵字

<!-- _class: cols-3 -->

<div class="ldiv">

- `<!DOCTYPE html>`
- `<html>`
- `<head>`
- `<title>`
- `<meta>`
- `<body>`
- `<h1>-<h6>`
- `<p>`
- `<a>`

</div>

<div class="mdiv">

- `<img>`
- `<ul>`
- `<ol>`
- `<li>`
- `<table>`
- `<tr>`
- `<th>`
- `<td>`
- `<form>`
- `<input>`

</div>

<div class="rdiv">

- `<button>`
- `<div>`
- `<span>`
- `<header>`
- `<nav>`
- `<main>`
- `<article>`
- `<section>`
- `<aside>`
- `<footer>`

</div>

## HTML5 新元素

- `<canvas>` 標簽定義圖形，比如圖表和其他圖像。該標簽基於 JavaScript 的繪圖 API

**新多媒體元素**
- `<audio>` 定義音頻內容
- `<video>` 定義視頻（video 或者 movie）
- `<source>` 定義多媒體資源 `<video>` 和 `<audio>`
- `<embed>` 定義嵌入的內容，比如插件。
- `<track>` 為諸如 `<video>` 和 `<audio>` 元素之類的媒介規定外部文本軌道。

**新表單元素**
- `<datalist>` 定義選項列表。請與 input 元素配合使用該元素，來定義 input 可能的值。
- `<keygen>` 規定用於表單的密鑰對生成器字段。
- `<output>` 定義不同類型的輸出，比如腳本的輸出。

## HTML5 新元素

**新的語義和結構元素**
- `<article>` 定義頁麵獨立的內容區域。
- `<aside>` 定義頁麵的側邊欄內容。
- `<bdi>` 允許您設置一段文本，使其脫離其父元素的文本方嚮設置。
- `<command>` 定義命令按鈕，比如單選按鈕、複選框或按鈕
- `<details>` 用於描述文檔或文檔某個部分的細節
- `<dialog>` 定義對話框，比如提示框
- `<summary>` 標簽包含 details 元素的標題
- `<figure>` 規定獨立的流內容（圖像、圖表、照片、代碼等等）。
- `<figcaption>` 定義 `<figure>` 元素的標題
- `<footer>` 定義 section 或 document 的頁腳。
- `<header>` 定義了文檔的頭部區域

## HTML5 新元素

**新的語義和結構元素**
- `<mark>` 定義帶有記號的文本。
- `<meter>` 定義度量衡。僅用於已知最大和最小值的度量。
- `<nav>` 定義導航鏈接的部分。
- `<progress>` 定義任何類型的任務的進度。
- `<ruby>` 定義 ruby 註釋（中文註音或字符）。
- `<rt>` 定義字符（中文註音或字符）的解釋或發音。
- `<rp>` 在 ruby 註釋中使用，定義不支持 ruby 元素的瀏覽器所顯示的內容。
- `<section>` 定義文檔中的節（section、區段）。
- `<time>` 定義日期或時間。
- `<wbr>` 規定在文本中的何處適合添加換行符。
- `<meter>` 定義度量衡。僅用於已知最大和最小值的度量。
- `<nav>` 定義導航鏈接的部分。

## HTML5 新元素
**新的語義和結構元素**

- `<progress>` 定義任何類型的任務的進度。
- `<ruby>` 定義 ruby 註釋（中文註音或字符）。
- `<rt>` 定義字符（中文註音或字符）的解釋或發音。
- `<rp>` 在 ruby 註釋中使用，定義不支持 ruby 元素的瀏覽器所顯示的內容。
- `<section>` 定義文檔中的節（section、區段）。
- `<time>` 定義日期或時間。
- `<wbr>` 規定在文本中的何處適合添加換行符。

## 實用資源

- [菜鳥教程 HTML 教程](https://www.runoob.com/html/html-tutorial.html)
- [W3Schools HTML 教程](https://www.w3schools.com/html/)