# position

position屬性設定元素的定位方式

position值有
- static
- relative
- fixed
- absolute
- sticky

## static

HTML元素的position預設值。

若元素的postiion為static，則不會受top、bottom、left、right屬性所影響。

不會被特別定位，以瀏覽器的預設為主。

```html
<style>
.static {
    position: static;
    border: 3px solid #73AD21;
}
</style>

<h2>position: static;</h2>

<p>An element with position: static; is not positioned in any special way; it is 
always positioned according to the normal flow of the page:</p>

<div class="static">
This div element has position: static;
</div>
```

## relative

若元素```position: relative;```，則會定位在預設位置的相對位置上。

利用top、bottom、left、right屬性來進行相對位置的設定。其他元素不會受該元素的影響。

```html
<style>
    div {
        width: 100px;
        height: 100px;
        display: inline-block;
        background-color: yellow;
    }
    #my-relative-div {
        position: relative;
        background-color: green;
        top: 20px;
        left: 50px;
    }
</style>
</head>
<body>

<div></div>
<div></div>
<div></div>
<div id="my-relative-div"></div>
<div></div>
```

## fixed

若元素```position: fixed;```則該元素會被定位在可視畫面的相對位置上。 即使滾動頁面也不改變顯示位置。

利用top、bottom、left、right屬性來進行相對位置的設定。

```html
<style>
    #my-fixed {
        width: 100px;
        height: 100px;
        background-color: greenyellow;
        position: fixed;
        left: 0px;
        bottom: 0px;
    }
</style>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos, ad.</p>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos, ad.</p>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos, ad.</p>
<div id="my-fixed"></div>
```

## absolute

若元素```position: absolute;```，則該元素會被定位在**最靠近且有被定位的父元素**的相對位置上。

有被定位：若該元素的position屬性不為static，則視為有被定位(positioned)。


```html
<style>
    .relative {
        width: 300px;
        height: 300px;
        background-color: yellow;
        position: relative;
    }
    .absolute {
        width: 50px;
        height: 50px;
        background-color: green;
        position: absolute;
        right: 25px;
        bottom: 25px;
    }
</style>
<div class="relative">
    <div class="absolute"></div>
</div>
```

若設定```position: absolute;```的元素找不到符合定位條件的父元素，會以```<body>```標籤來定位。

## sticky

若元素```position: sticky;``` ，則該元素會根據使用者捲動的位置來定位。

sticky元素會根據捲動的位置來切換```relative ```及```fixed```屬性。

```html
<style>
#my-sticky {
  position: sticky;
  top: 10px;
  padding: 5px;
  background-color: yellowgreen;
}
p {
height: 500px;
}
</style>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus, harum.</p>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus, harum.</p>
<div id="my-sticky">
    Hey, this is sticky!
</div>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus, harum.</p>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus, harum.</p>
```

reference: [W3c: The position Property](https://www.w3schools.com/css/css_positioning.asp)

reference: [關於 position 屬性](http://zh-tw.learnlayout.com/position.html)