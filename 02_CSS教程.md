---
marp: true
theme: m_blue
headingDivider: 3
paginate: true
---
# CSS 基礎教學
<!-- _class: trans -->
<!-- _footer: "" -->

## CSS 是什麼？
<!-- _class: cols-2 -->
CSS（層疊樣式表）是一種用於描述HTML（或XML等）文檔呈現方式的樣式語言。它控製網頁的佈局和外觀，允許開發者將樣式（如顔色、字體、間距等）與內容分離。以下是核心特點：
1. 核心作用
	-	控製HTML元素在屏幕上的顯示效果
	-	實現網頁外觀與佈局的精確控製
	- 分離樣式與內容（符合關註點分離原則）
2. 名稱含義
	- Cascading：樣式優先級規則（層疊）
	- Style：定義視覺呈現
	- Sheets：可複用的樣式規則集合
3. 關鍵能力
	- 響應式設計（適配不同設備）
	- 動畫與過渡效果
	- 佈局係統（Flexbox/Grid）
	- 主題切換與樣式複用

## CSS 基本語法

```css
selector {
    property: value;
    property: value;
}
```

- **selector**: 選擇要樣式化的 HTML 元素
- **property**: 要設置的樣式屬性
- **value**: 屬性的值

## CSS 引入方式
<!-- _class: cols-2 -->
<div class="ldiv">

1. 內聯樣式 (Inline)

```html
<p style="color: blue;">藍色文字</p>
```

2. 內部樣式表 (Internal)
```html
<head>
    <style>
        p {
            color: blue;
        }
    </style>
</head>
```
</div>
<div class="rdiv">

3. 外部樣式表 (External) - 最佳實踐
```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

</div>

## CSS 選擇器
<!-- _class: cols-2 -->
<div class="ldiv">

* 元素選擇器
```css
p {
    color: red;
}
```

* Class 選擇器
```css
.highlight {
    background-color: yellow;
}
```
</div>
<div class="rdiv">

* ID 選擇器
```css
#header {
    font-size: 24px;
}
```

</div>

## CSS 盒子模型(Box Model)

![CSS 盒子模型](./img/box-model.gif)

- Margin(外邊距) - 清除邊框外的區域，外邊距是透明的。
- Border(邊框) - 圍繞在內邊距和內容外的邊框。
- Padding(內邊距) - 清除內容周圍的區域，內邊距是透明的。
- Content(內容) - 盒子的內容，顯示文本和圖像。

## CSS 優先級

1. !important：最高優先級 `color: red !important;`
2. 行內樣式： `<div style="color:red;">`（權重=1000）
3. ID 選擇器：`#header`（權重=100）
4. 類/偽類/屬性選擇器：`.btn, :hover, [type="text"]`（權重=10）
5. 元素/偽元素選擇器：`div, ::before`（權重=1）
6. 通用選擇器：`* { margin: 0; }`（權重=0）

## 常用 CSS 屬性
1. 文字與字體
```css
p {
    color: #333;                /* 文字顏色 */
    font-family: Arial, sans-serif; /* 字體 */
    font-size: 16px;            /* 字體大小 */
    font-weight: bold;          /* 字體粗細 */
    text-align: center;         /* 對齊方式 */
    line-height: 1.5;           /* 行高 */
    text-decoration: underline; /* 文字裝飾 */
}
```
## 常用 CSS 屬性
2. 背景
```css
div {
    background-color: #f0f0f0;  /* 背景顏色 */
    background-image: url('bg.jpg'); /* 背景圖片 */
    background-repeat: no-repeat; /* 重複方式 */
    background-position: center; /* 位置 */
    background-size: cover;     /* 尺寸 */
}
```

## 常用 CSS 屬性
3. 盒模型
```css
.container {
    width: 80%;                 /* 寬度 */
    height: 200px;              /* 高度 */
    padding: 20px;              /* 內邊距 */
    margin: 10px auto;          /* 外邊距 */
    border: 1px solid #ccc;     /* 邊框 */
    border-radius: 8px;         /* 圓角 */
    box-shadow: 0 2px 5px rgba(0,0,0,0.1); /* 陰影 */
}
```

## 常用 CSS 屬性
4. 佈局
```css
.flex-container {
    display: flex;              /* 彈性佈局 */
    justify-content: space-between; /* 主軸對齊 */
    align-items: center;        /* 交叉軸對齊 */
    flex-wrap: wrap;            /* 換行 */
}

.grid-container {
    display: grid;              /* 網格佈局 */
    grid-template-columns: 1fr 1fr 1fr; /* 列定義 */
    gap: 10px;                  /* 間距 */
}
```

## 常用 CSS 屬性
5. 定位
```css
.box {
    position: relative;         /* 相對定位 */
    top: 10px;                  /* 上偏移 */
    left: 20px;                 /* 左偏移 */
    z-index: 10;                /* 層級 */
}

.fixed-element {
    position: fixed;            /* 固定定位 */
    bottom: 20px;               /* 底部距離 */
    right: 20px;                /* 右側距離 */
}
```

## 常用 CSS 屬性
<!-- _class: smalltext -->
6. 動畫與過渡
```css
.button {
    transition: all 0.3s ease;  /* 過渡效果 */
}

.button:hover {
    transform: scale(1.1);      /* 縮放 */
    background-color: #007bff;  /* 顏色變化 */
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

.element {
    animation: fadeIn 1s forwards; /* 動畫應用 */
}
```

## 練習
<!-- _class: cols-2 -->
<div class="ldiv">

```html
<!-- html -->
<p>Hi</p>
<div class="box"> <div>2</div> </div>
```

</div><div class="rdiv">

```css
/* css */
p {
  color: red;
  font-size: 40px;
  font-weight: bold;
  text-align: center;
  text-decoration: underline;
}
.box{
  background-color: yellow;
  width: 80%;
  height: 100px;
  border: 1px solid red;
}
.box>div{
  margin: 20px;
  border: 1px solid red;
  padding: 10px 5px;
  border-radius: 15px;
  box-shadow: 5px 5px 10px rgba(0,0,0, 0.5);
}
```

</div>

## 實用資源

- [菜鳥教程 CSS](https://www.runoob.com/css/css-tutorial.html)
- [W3Schools CSS 教程](https://www.w3schools.com/css/)


### 附件
<!-- _class: cols-2 tinytext -->
<div class="ldiv">

###### CSS 動畫屬性

|屬性	|描述	|CSS|
|---|---|---|
|@keyframes	|定義一個動畫,@keyframes定義的動畫名稱用來被animation-name所使用。	|3|
|animation	|複合屬性。檢索或設置對象所應用的動畫特效。	|3|
|animation-name	|檢索或設置對象所應用的動畫名稱 ,必須與規則@keyframes配合使用，因為動畫名稱由@keyframes定義	|3|
|animation-duration	|檢索或設置對象動畫的持續時間	|3|
|animation-timing-function	|檢索或設置對象動畫的過渡類型	|3|
|animation-delay	|檢索或設置對象動畫的延遲時間	|3|
|animation-iteration-count	|檢索或設置對象動畫的循環次數	|3|
|animation-direction	|檢索或設置對象動畫在循環中是否反嚮運動	|3|
|animation-play-state	|檢索或設置對象動畫的狀態	|3|
</div>
<div class="rdiv">

###### CSS 背景屬性

|屬性	|描述	|CSS|
|---|---|---|
|background	|複合屬性。設置對象的背景特性。	|1|
|background-attachment	|設置或檢索背景圖像是隨對象內容滾動還是固定的。必須先指定background-image屬性。	|1|
|background-color	|設置或檢索對象的背景顔色。	|1|
|background-image	|設置或檢索對象的背景圖像。	|1|
|background-position	|設置或檢索對象的背景圖像位置。必須先指定background-image屬性。	|1
|background-repeat	|設置或檢索對象的背景圖像如何鋪排填充。必須先指定background-image屬性。	|1
|background-clip	|指定對象的背景圖像嚮外裁剪的區域。	|3
|background-origin	|設置或檢索對象的背景圖像計算background-position時的參考原點(位置)。	|3
|background-size	|檢索或設置對象的背景圖像的尺寸大小。	|3

</div>

### 附件
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### CSS 邊框(Border) 和 輪廓(Outline) 屬性

|屬性	|描述	|CSS|
|---|---|---|
|border	|複合屬性。設置對象邊框的特性。	|1|
|border-bottom	|複合屬性。設置對象底部邊框的特性。	|1|
|border-bottom-color	|設置或檢索對象的底部邊框顔色。	|1|
|border-bottom-style	|設置或檢索對象的底部邊框樣式。	|1|
|border-bottom-width	|設置或檢索對象的底部邊框寬度。	|1|
|border-color	|置或檢索對象的邊框顔色。	|1|
|border-left	|複合屬性。設置對象左邊邊框的特性。	|1|
|border-left-color	|設置或檢索對象的左邊邊框顔色。	|1|
|border-left-style	|設置或檢索對象的左邊邊框樣式。	|1|
|border-left-width	|設置或檢索對象的左邊邊框寬度。	|1|
|border-right	|複合屬性。設置對象右邊邊框的特性。	|1|
|border-right-color	|設置或檢索對象的右邊邊框顔色。	|1|
</div><div class="rdiv">

###### CSS  邊框(Border) 和 輪廓(Outline) 屬性

|屬性	|描述	|CSS|
|---|---|---|
|border-right-style	|設置或檢索對象的右邊邊框樣式。	|1|
|border-right-width	|設置或檢索對象的右邊邊框寬度。	|1|
|border-style	|設置或檢索對象的邊框樣式。	|1|
|border-top	|複合屬性。設置對象頂部邊框的特性。	|1|
|border-top-color	|設置或檢索對象的頂部邊框顔色	|1|
|border-top-style	|設置或檢索對象的頂部邊框樣式。	|1|
|border-top-width	|設置或檢索對象的頂部邊框寬度。	|1|
|border-width	|設置或檢索對象的邊框寬度。	|1|
|outline	|複合屬性。設置或檢索對象外的線條輪廓。	|2|
|outline-color	|設置或檢索對象外的線條輪廓的顔色。	|2|
|outline-style	|設置或檢索對象外的線條輪廓的樣式。	|2|
|outline-width	|設置或檢索對象外的線條輪廓的寬度。	|2|

</div>

### 附件 
<!-- _class: tinytext -->

###### 邊框(Border) 和 輪廓(Outline) 屬性

|屬性	|描述	|CSS|
|---|---|---|
|border-bottom-left-radius	|設置或檢索對象的左下角圓角邊框。提供2個參數，2個參數以空格分隔，每個參數允許設置1個參數值，第1個參數表示水平半徑，第2個參數表示垂直半徑，如第2個參數省略，則默認等於第1個參數	|3|
|border-bottom-right-radius	|設置或檢索對象的右下角圓角邊框。	|3|
|border-image	|設置或檢索對象的邊框樣式使用圖像來填充。	|3|
|border-image-outset	|規定邊框圖像超過邊框的量。	|3|
|border-image-repeat	|規定圖像邊框是否應該被重複（repeated）、拉伸（stretched）或鋪滿（rounded）。	|3|
|border-image-slice	|規定圖像邊框的嚮內偏移。	|3|
|border-image-source	|規定要使用的圖像，代替 border-style 屬性中設置的邊框樣式。	|3|
|border-image-width	|規定圖像邊框的寬度。	|3|

### 附件 
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### CSS  邊框(Border) 和 輪廓(Outline) 屬性

|屬性	|描述	|CSS|
|---|---|---|
|border-radius	|設置或檢索對象使用圓角邊框。	|3|
|border-top-left-radius	|定義左上角邊框的形狀。	|3|
|border-top-right-radius	|定義右上角邊框的形狀。	|3|
|box-decoration-break	|規定行內元素被摺行	|3|
|box-shadow	|嚮方框添加一個或多個陰影。	|3|

</div><div class="rdiv">

###### CSS 盒子(Box) 屬性

|屬性	|描述	|CSS|
|---|---|---|
|overflow-x	|如果內容溢出了元素內容區域，是否對內容的左/右邊緣進行裁剪。	|3|
|overflow-y	|如果內容溢出了元素內容區域，是否對內容的上/下邊緣進行裁剪。	|3|
|overflow-style	|規定溢出元素的首選滾動方法。	|3|
|rotation	|圍繞由 rotation-point 屬性定義的點對元素進行旋轉。	|3|
|rotation-point	|定義距離上左邊框邊緣的偏移點。	|3|

</div>

### 附件 
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### 顔色(Color) 屬性

|屬性	|描述	|CSS|
|---|---|---|
|color-profile	|允許使用源的顔色配置文件的默認以外的規範	|3|
|opacity	|設置一個元素的透明度級別	|3|
|rendering-intent	|允許超過默認顔色配置文件渲染意嚮的其他規範	|3|

###### 內邊距(Padding) 屬性

|屬性	|描述	|CSS|
|---|---|---|
|padding	|在一個聲明中設置所有填充屬性	|1|
|padding-bottom	|設置元素的底填充	|1|
|padding-left	|設置元素的左填充	|1|
|padding-right	|設置元素的右填充	|1|
|padding-top	|設置元素的頂部填充	|1|

</div><div class="rdiv">

###### CSS 尺寸(Dimension) 屬性

|屬性	|描述	|CSS|
|---|---|---|
|height	|設置元素的高度	|1|
|max-height	|設置元素的最大高度	|2|
|max-width	|設置元素的最大寬度	|2|
|min-height	|設置元素的最小高度	|2|
|min-width	|設置元素的最小寬度	|2|
|width	|設置元素的寬度	|1|

</div>

### 附件 - 媒體頁面內容屬性 
<!-- _class: tinytext  -->

|屬性	|描述	|CSS|
|---|---|---|
|bookmark-label	|指定書簽的標簽	|3|
|bookmark-level	|指定了書簽級別	|3|
|bookmark-target	|指定了書簽鏈接的目標	|3|
|float-offset	|在相反的方嚮推動浮動元素，他們一直具有浮動	|3|
|hyphenate-after	|指定一個斷字的單詞斷字字符後的最少字符數	|3|
|hyphenate-before	|指定一個斷字的單詞斷字字符前的最少字符數	|3|
|hyphenate-character	|指定了當一個斷字發生時，要顯示的字符串	|3|
|hyphenate-lines	|表示連續斷字的行在元素的最大數目	|3|
|hyphenate-resource	|外部資源指定一個逗號分隔的列表，可以幫助確定瀏覽器的斷字點	|3|
|hyphens	|設置如何分割單詞以改善該段的佈局	|3|
|image-resolution	|指定了正確的圖像分辨率	|3|
|marks	|將crop and/or cross標誌添加到文檔	|3|
|string-set	| 	|3


### 附件 - CSS 彈性盒子模型（Flexible Box） 屬性(新)

<!-- _class: tinytext -->

|屬性	|說明	|CSS|
|---|---|---|
|flex	|複合屬性。設置或檢索彈性盒模型對象的子元素如何分配空間。	|3|
|flex-grow	|設置或檢索彈性盒的擴展比率。	|3|
|flex-shrink	|設置或檢索彈性盒的收縮比率。	|3|
|flex-basis	|設置或檢索彈性盒伸縮基準值。	|3|
|flex-flow	|複合屬性。設置或檢索彈性盒模型對象的子元素排列方式。	|3|
|flex-direction	|該屬性通過定義 flex 容器的主軸方嚮來決定 flex 子項在 flex 容器中的位置。	|3|
|flex-wrap	|該屬性控製flex容器是單行或者多行，同時橫軸的方嚮決定了新行堆疊的方嚮。	|3|
|align-content	|在彈性容器內的各項冇有佔用交叉軸上所有可用的空間時對齊容器內的各項（垂直）。	|3|
|align-items	|定義flex子項在flex容器的當前行的側軸（縱軸）方嚮上的對齊方式。	|3|
|align-self	|定義flex子項單獨在側軸（縱軸）方嚮上的對齊方式。	|3|
|justify-content	|設置或檢索彈性盒子元素在主軸（橫軸）方嚮上的對齊方式。	|3|
|order	|設置或檢索彈性盒模型對象的子元素出現的順序。	|3|

### 附件 - CSS 彈性盒子模型（Flexible Box） 屬性(舊)

<!-- _class: tinytext -->

|屬性	|說明	|CSS|
|---|---|---|
|box-align	|指定如何對齊一個框的子元素	|3|
|box-direction	|指定在哪個方嚮，顯示一個框的子元素	|3|
|box-flex	|指定一個框的子元素是否是靈活的或固定的大小	|3|
|box-flex-group	|指派靈活的元素到Flex組	|3|
|box-lines	|每當它在父框的空間運行時，是否指定將再上一個新的行列	|3|
|box-ordinal-group	|指定一個框的子元素的顯示順序	|3|
|box-orient	|指定一個框的子元素是否在水平或垂直方嚮應鋪設	|3|
|box-pack	|指定橫嚮盒在垂直框的水平位置和垂直位置	|3|

### 附件
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### CSS 字體（Font） 屬性

|屬性	|說明	|CSS|
|---|---|---|
|font	|在一個聲明中設置所有字體屬性	|1|
|font-family	|規定文本的字體係列	|1|
|font-size	|規定文本的字體尺寸	|1|
|font-style	|規定文本的字體樣式	|1|
|font-variant	|規定文本的字體樣式	|1|
|font-weight	|規定字體的粗細	|1|
|@font-face	|一個規則，允許網站下載並使用其他超過"Web- safe"字體的字體	|3|
|font-size-adjust	|為元素規定 aspect 值	|3|
|font-stretch	|收縮或拉伸當前的字體係列	|3|

</div><div class="rdiv"></div>

###### 內容生成屬性(Generated Content Properties)


|屬性	|說明	|CSS|
|---|---|---|
|content	|與 :before 以及 :after 僞元素配合使用，來插入生成內容	|2|
|counter-increment	|遞增或遞減一個或多個計數器	|2|
|counter-reset	|創建或重置一個或多個計數器	|2|
|quotes	|設置嵌套引用的引號類型	|2|
|crop	|允許replaced元素隻是作為一個對象代替整個對象的矩形區域	|3|
|move-to	|從流中刪除元素，然後在文檔中後面的點上重新插入。	|3|
|page-policy	|判定基於頁面的給定元素的適用於計數器的字符串值	|3|

</div>

### 附件
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### 網格（Grid） 屬性

|屬性	|說明	|CSS|
|---|---|---|
|grid-column	|設置網格元素列的開始和結束位置	|3|
|grid-row	|設置網格元素行的開始和結束位置。	|3|


###### 超鏈接(Hyperlink) 屬性

|屬性	|說明	|CSS|
|---|---|---|
|target	|簡寫屬性設置target-name, target-new,和target-position屬性	|3|
|target-name	|指定在何處打開鏈接（目標位置）	|3|
|target-new	|指定是否有新的目標鏈接打開一個新窗口或在現有窗口打開新標簽	|3|
|target-position	|指定應該放置新的目標鏈接的位置	|3|

</div>
<div class="rdiv"></div>

### 附件 - 線框(Linebox) 屬性


|屬性	|說明	|CSS|
|---|---|---|
|alignment-adjust	|允許更精確的元素的對齊方式	|3|
|alignment-baseline	|其父級指定的內聯級別的元素如何對齊	|3|
|baseline-shift	|允許重新定位相對於dominant-baseline的dominant-baseline	|3|
|dominant-baseline	|指定scaled-baseline-table	|3|
|drop-initial-after-adjust	|設置下拉的主要連接點的初始對齊點	|3|
|drop-initial-after-align	|校準行內的初始行的設置就是具有首字母的框使用初級連接點	|3|
|drop-initial-before-adjust	|設置下拉的輔助連接點的初始對齊點	|3|
|drop-initial-before-align	|校準行內的初始行的設置就是具有首字母的框使用輔助連接點	|3|
|drop-initial-size	|控製局部的首字母下沈	|3|
|drop-initial-value	|激活一個下拉式的初步效果	|3|

### 附件 - 線框(Linebox) 屬性

<!-- _class: tinytext -->
|屬性	|說明	|CSS|
|---|---|---|
|inline-box-align	|設置一個多行的內聯塊內的行具有前一個和後一個內聯元素的對齊	|3|
|line-stacking	|一個速記屬性設置line-stacking-strategy, line-stacking-ruby,和line-stacking-shift屬性	|3|
|line-stacking-ruby	|設置包含Ruby註釋元素的行對於塊元素的堆疊方法	|3|
|line-stacking-shift	|設置base-shift行中塊元素包含元素的堆疊方法	|3|
|line-stacking-strategy	|設置內部包含塊元素的堆疊線框的堆疊方法	|3|
|text-height	|行內框的文本內容區域設置block-progression維數	|3|

### 附件
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### 列表(List) 屬性

|屬性	|說明	|CSS|
|---|---|---|
|list-style	|在一個聲明中設置所有的列表屬性	|1|
|list-style-image	|將圖象設置為列表項標記	|1|
|list-style-position	|設置列表項標記的放置位置	|1|
|list-style-type	|設置列表項標記的類型	|1|

###### 外邊距(Margin) 屬性  

|屬性	|說明	|CSS|
|---|---|---|
|margin	|在一個聲明中設置所有外邊距屬性	|1|
|margin-bottom	|設置元素的下外邊距	|1|
|margin-left	|設置元素的左外邊距	|1|
|margin-right	|設置元素的右外邊距	|1|
|margin-top	|設置元素的上外邊距	|1|

</div><div class="rdiv">

###### 字幕(Marquee) 屬性

|屬性	|說明	|CSS|
|---|---|---|
|marquee-direction	|設置內容移動的方嚮	|3|
|marquee-play-count	|設置內容移動多少次	|3|
|marquee-speed	|設置內容滾動的速度有多快	|3|
|marquee-style	|設置內容移動的樣式	|3|

</div>

### 附件
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### 多列(Multi-column) 屬性

|屬性	|說明	|CSS|
|---|---|---|
|column-count	|指定元素應該分為的列數	|3|
|column-fill	|指定如何填充列	|3|
|column-gap	|指定列之間的差距	|3|
|column-rule	|對於設置所有column-rule-*屬性的簡寫屬性	|3|
|column-rule-color	|指定列之間的顔色規則	|3|
|column-rule-style	|指定列之間的樣式規則	|3|
|column-rule-width	|指定列之間的寬度規則	|3|
|column-span	|指定元素應該跨越多少列	|3|
|column-width	|指定列的寬度	|3|
|columns	|縮寫屬性設置列寬和列數	|3|

</div><div class="rdiv">

###### 頁面媒體(Paged Media) 屬性

|屬性	|說明	|CSS|
|---|---|---|
|fit	|如果其寬度和高度屬性都不是auto給出一個提示，如何大規模替換元素	|3|
|fit-position	|判定方框內對象的對齊方式	|3|
|image-orientation	|指定用戶代理適用於圖像中的嚮右或順時針方嚮的旋轉	|3|
|page	|指定一個元素應顯示的頁面的特定類型	|3|
|size	|指定含有BOX的頁面內容的大小和方位	|3|

</div>

### 附件 - 定位（Positioning） 屬性

<!-- _class: tinytext -->
|屬性	|說明	|CSS|
|---|---|---|
|bottom	|設置定位元素下外邊距邊界與其包含塊下邊界之間的偏移	|2|
|clear	|規定元素的哪一側不允許其他浮動元素	|1|
|clip	|剪裁絕對定位元素	|2|
|cursor	|規定要顯示的光標的類型（形狀）	|2|
|display	|規定元素應該生成的框的類型	|1|
|float	|規定框是否應該浮動	|1|
|left	|設置定位元素左外邊距邊界與其包含塊左邊界之間的偏移	|2|
|overflow	|規定當內容溢出元素框時發生的事情	|2|
|position	|規定元素的定位類型	|2|
|right	|設置定位元素右外邊距邊界與其包含塊右邊界之間的偏移	|2|
|top	|設置定位元素的上外邊距邊界與其包含塊上邊界之間的偏移	|2|
|visibility	|規定元素是否可見	|2|
|z-index	|設置元素的堆疊順序	|2|

### 附件 
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### 分頁（Print） 屬性
|屬性	|說明	|CSS|
|---|---|---|
|orphans	|設置當元素內部發生分頁時必須在頁面底部保留的最少行數	|2|
|page-break-after	|設置元素後的分頁行為	|2|
|page-break-before	|設置元素前的分頁行為	|2|
|page-break-inside	|設置元素內部的分頁行為	|2|
|widows	|設置當元素內部發生分頁時必須在頁面頂部保留的最少行數	|2|

</div><div class="rdiv">

###### Ruby 屬性

|屬性	|說明	|CSS|
|---|---|---|
|ruby-align	|控製Ruby文本和Ruby基礎內容相對彼此的文本對齊方式	|3|
|ruby-overhang	|當Ruby文本超過Ruby的基礎寬，確定ruby文本是否允許局部懸置任意相鄰的文本，除了自己的基礎	|3|
|ruby-position	|它的base控製Ruby文本的位置	|3|
|ruby-span	|控製annotation 元素的跨越行為	|3|

</div>

### 附件 
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### 語音（Speech） 屬性

|屬性	|說明	|CSS|
|---|---|---|
|mark	|縮寫屬性設置mark-before和mark-after屬性	|3|
|mark-after	|允許命名的標記連接到音頻流	|3|
|mark-before	|允許命名的標記連接到音頻流	|3|
|phonemes	|指定包含文本的相應元素中的一個音標發音	|3|
|rest	|一個縮寫屬性設置rest-before和rest-after屬性	|3|
|rest-after	|一個元素的內容講完之後，指定要休息一下或遵守韻律邊界	|3|
|rest-before	|一個元素的內容講完之前，指定要休息一下或遵守韻律邊界	|3|

</div><div class="rdiv">

######  語音（Speech） 屬性

|屬性	|說明	|CSS|
|---|---|---|
|voice-balance	|指定了左，右聲道之間的平衡	|3|
|voice-duration	|指定應採取呈現所選元素的內容的長度	|3|
|voice-pitch	|指定平均說話的聲音的音調（頻率）	|3|
|voice-pitch-range	|指定平均間距的變化	|3|
|voice-rate	|控製語速	|3|
|voice-stress	|指示著重力度	|3|
|voice-volume	|語音合成是指波形輸出幅度	|3|

</div>

### 附件
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### 表格（Table） 屬性
|屬性	|說明	|CSS|
|---|---|---|
|border-collapse	|規定是否合並表格邊框	|2|
|border-spacing	|規定相鄰單元格邊框之間的距離	|2|
|caption-side	|規定表格標題的位置	|2|
|empty-cells	|規定是否顯示表格中的空單元格上的邊框和背景	|2|
|table-layout	|設置用於表格的佈局算法	|2|

</div><div class="rdiv">

###### 文本（Text） 屬性

|屬性	|說明	|CSS|
|---|---|---|
color	|設置文本的顔色	|1
direction	|規定文本的方嚮 / 書寫方嚮	|2
letter-spacing	|設置字符間距	|1
line-height	|設置行高	|1
text-align	|規定文本的水平對齊方式	|1
text-decoration	|規定添加到文本的裝飾效果	|1
text-indent	|規定文本塊首行的縮進	|1
text-transform	|控製文本的大小寫	|1
unicode-bidi	| 	|2
vertical-align	|設置元素的垂直對齊方式	|1
white-space	|設置怎樣給一元素控件留白	|1
word-spacing	|設置單詞間距	|1

</div>

## 附件
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### 文本（Text） 屬性
|屬性	|說明	|CSS|
|---|---|---|
text-emphasis	|嚮元素的文本應用重點標記以及重點標記的前景色。	|1
hanging-punctuation	|指定一個標點符號是否可能超出行框	|3
punctuation-trim	|指定一個標點符號是否要去掉	|3
text-align-last	|當 text-align 設置為 justify 時，最後一行的對齊方式。	|3
text-justify	|當 text-align 設置為 justify 時指定分散對齊的方式。	|3
text-outline	|設置文字的輪廓。	|3
text-overflow	|指定當文本溢出包含的元素，應該發生什麼	|3
text-shadow	|為文本添加陰影	|3
text-wrap	|指定文本換行規則	|3
word-break	|指定非CJK文字的斷行規則	|3
word-wrap	|設置瀏覽器是否對過長的單詞進行換行。	|3

</div><div class= "rdiv">

###### 2D/3D 轉換屬性

|屬性	|說明	|CSS|
|---|---|---|
transform	|適用於2D或3D轉換的元素	|3
transform-origin	|允許您更改轉化元素位置	|3
transform-style	|3D空間中的指定如何嵌套元素	|3
perspective	|指定3D元素是如何查看透視圖	|3
perspective-origin	|指定3D元素底部位置	|3
backface-visibility	|定義一個元素是否應該是可見的，不對著屏幕時	|3

</div>

## 附件
<!-- _class: tinytext cols-2 -->
<div class="ldiv">

###### 過渡（Transition） 屬性

|屬性	|說明	|CSS|
|---|---|---|
transition	|此屬性是 transition-property、transition-duration、transition-timing-function、transition-delay 的簡寫形式。	|3
transition-property	|設置用來進行過渡的 CSS 屬性。	|3
transition-duration	|設置過渡進行的時間長度。	|3
transition-timing-function	|設置過渡進行的時序函數。	|3
transition-delay	|指定過渡開始的時間。	|3

</div><div class="rdiv">

###### 用戶外觀(User-interface) 屬性
|屬性	|說明	|CSS|
|---|---|---|
appearance	|定義元素的外觀樣式	|3
box-sizing	|允許您為了適應區域以某種方式定義某些元素	|3
icon	|為元素指定圖標	|3
nav-down	|指定用戶按嚮下鍵時嚮下導航的位置	|3
nav-index	|指定導航（tab）順序。	|3
nav-left	|指定用戶按嚮左鍵時嚮左導航的位置	|3
nav-right	|指定用戶按嚮右鍵時嚮右導航的位置	|3
nav-up	|指定用戶按嚮上鍵時嚮上導航的位置a	|3
outline-offset	|設置輪廓框架在 border 邊緣外的偏移	|3
resize	|定義元素是否可以改變大小	|3

</div>