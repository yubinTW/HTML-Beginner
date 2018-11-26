# CSS 常見樣式

- color
- background-color
- font-family
- font-size
- text-align
- border

## color 顏色 

定義元素顯示的顏色，顏色的格式可以為color names, RGB, HEX, HSL, RGBA, 或 HSLA values

### color name

https://www.w3schools.com/colors/colors_names.asp


```html
<style>
    p {
        color: red;
    }
</style>
<p>This is red.</p>
```

### RGB

rgb(red, green, blue)

value range: 0~255

```html
<style>
    p {
        color: rgb(123,11,22);
    }
</style>
<p>color test</p>
```

### HEX

#rrggbb

value range: 00~FF

```html
<style>
    p {
        color: #7b0b16;
    }
</style>
```

> tool: [Color Picker](https://www.google.com.tw/search?q=color+picker)

## background-color 背景顏色

```html
<style>
    p {
        background-color: yellow;
    }
</style>
<p>早安，我的朋友</p>
```

## font-family 字型

```html
<style>
    #test {
        font-family:'微軟正黑體';
    }
</style>
<p id="test">早安，我的朋友</p>
<p>晚安，我的朋友</p>
```

- 可輸入多個字型，會以第一個為主
- 第一個不存在，往後找，依此類推
- 都不存在或未定義，以瀏覽器預設為主

## font-size 字體大小

```html
<style>
    #p1 {
        font-size: 20px;
    }
    #p2 {
        font-size:150%
    }
    #p3 {
        font-size:2em
    }
</style>
<p id="p1" style="font-size:20px">早安，我的朋友</p>
<p id="p2" style="font-size:150%">午安，我的朋友</p>
<p id="p3" style="font-size:2em">晚安，我的朋友</p>
```
[font-size reference](https://www.w3schools.com/cssref/pr_font_font-size.asp)

- 絕對大小:
    - 某個絕對的數值
    - 不允許使用者隨意更改
    - 已知輸出尺寸時使用

- 相對大小:
    - 相對於周圍元素的大小
    - 允許使用者進行更改

> 未設定時，瀏覽器會有預設值。例如```<p>```標籤預設大小為16px

### 單位
- px 
    - pixel
- %
    - 父元素font-size的百分比大小
- em
    - W3C建議使用的單位
    - 1em 代表目前的font-size. 瀏覽器預設的font-szie為16px，所以1em=16px
    - pixel與em數值可以互相轉換
    - 支援小數點，如```1.5em```

## text-align

指定文字水平對齊的方式

- left
- right
- center
- justify
    - 拉伸至每行有相同的長度(像報紙或雜誌)

```html
<style>
div.a {
    text-align: center;
}
div.b {
    text-align: left;
}
div.c {
    text-align: right;
} 
div.d {
    text-align: justify;
} 
</style>

<div class="a">
    <h2>text-align: center:</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam semper diam at erat pulvinar, at pulvinar felis blandit. Vestibulum volutpat tellus diam, consequat gravida libero rhoncus ut.</p>
</div>

<div class="b">
    <h2>text-align: left:</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam semper diam at erat pulvinar, at pulvinar felis blandit. Vestibulum volutpat tellus diam, consequat gravida libero rhoncus ut.</p>
</div>

<div class="c">
    <h2>text-align: right:</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam semper diam at erat pulvinar, at pulvinar felis blandit. Vestibulum volutpat tellus diam, consequat gravida libero rhoncus ut.</p>
</div>

<div class="d">
    <h2>text-align: justify:</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam semper diam at erat pulvinar, at pulvinar felis blandit. Vestibulum volutpat tellus diam, consequat gravida libero rhoncus ut.</p>
</div>
```

reference: [text-align](https://www.w3schools.com/cssref/pr_text_text-align.asp)

## border

border屬性定義邊框

```html
<style>
    P {
        border: 1px red solid;
    }
</style>
<p>This is a paragraph.</p>
```

border: 寬度 顏色 樣式

- 寬度
    - 數值、單位
- 顏色
    - 顏色的格式 color code
- 樣式
    - dotted
    - dashed
    - solid
    - double
    - groove
    - ridge
    - inset
    - outset
    - none
    - hidden

border上下左右可以分開設定

reference: [border](https://www.w3schools.com/css/css_border.asp)

## border-radius

讓邊框有圓角

```html
<style>
p {
    border: 2px solid red;
    border-radius: 5px;
}
</style>
<p>This is a paragraph.</p>
```

> 設定50%就變橢圓形

## Box Model

每個HTML元素都是長方形! 就像一個box。

[Box Model](box-model.md)