# display

display屬性是CSS排版的重要屬性，每個HTML元素都有一個預設的display值。

常見的display值
- block
- inline
- inline-block
- none

以下簡介各個display值

## block

一般會稱display為block的元素為「區塊元素」(block-elements)

```<div>```標籤是一個標準的block元素，一個區塊元素會讓其內容從新的一行開始顯示，並盡可能的撐滿容器。

```<div>```標籤常作為其他HTML元素的容器，搭配id, class來套用CSS樣式。

```html
<style>
    .my-div {
        background-color: #EEE;
    }
</style>
<div class="my-div">
    <h2>This is a h2 tag</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ducimus, nemo itaque? Iusto a consequatur praesentium eos sit impedit iure in eaque, id quod fugiat odio dolor maxime et officia illo.</p>
</div>
```

其他常見的區塊元素，```<p>```、 ```<h1>```、```<form>```等

## inline

一般會稱display為inline的元素為「行內元素」(inline-elements)

```<span>```標籤是一個標準的行內元素。一個行內元素可以在段落中包裹一些文字片段，將其套用CSS樣式。

```html
<style>
    .my-span {
        color: red;
    }
</style>
<p>Lorem ipsum dolor sit amet <span class="my-span">consectetur</span> adipisicing elit. <span class="my-span">Sed</span>, quos!</p>
```

其他常見行內元素，```<a>```

## block 與 inline

若```display: block;``` ，可以設定width、height來設定寬高，及上下左右的margin、padding值。

若```display: inline;```，無法利用width、height來設定寬高，元素的寬高取決於內容(如文字)。

reference: [HTML Block and Inline Elements](https://www.w3schools.com/html/html_blocks.asp)

```html
<style>
    div {
        background-color: lightgray;
    }
    span {
        background-color: yellow;
    }
</style>

<div>Hello</div>
<div>World</div>

<span>Hello</span>
<span>World</span>
```

## inline-block

若```display: inline-block```，該元素可以設定width、height，及上下左右的margin。

reference: [inline-block](https://www.w3schools.com/css/css_inline-block.asp)

```html
<style>
    .a,
    .b,
    .c {
        width: 100px;
        height: 100px;
        padding: 5px;
        border: 1px solid blue;    
        background-color: yellow; 
    }
    .a {
        display: inline;    
    }
    .b {
        display: inline-block;
    }
    .c {
        display: block;
    }
</style>
<h1>The display Property</h1>

<h2>display: inline</h2>
<div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum consequat scelerisque elit sit amet consequat. Aliquam erat volutpat. <span class="a">Aliquam</span> <span class="a">venenatis</span> gravida nisl sit amet facilisis. Nullam cursus fermentum velit sed laoreet. </div>

<h2>display: inline-block</h2>
<div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum consequat scelerisque elit sit amet consequat. Aliquam erat volutpat. <span class="b">Aliquam</span> <span class="b">venenatis</span> gravida nisl sit amet facilisis. Nullam cursus fermentum velit sed laoreet. </div>

<h2>display: block</h2>
<div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum consequat scelerisque elit sit amet consequat. Aliquam erat volutpat. <span class="c">Aliquam</span> <span class="c">venenatis</span> gravida nisl sit amet facilisis. Nullam cursus fermentum velit sed laoreet. </div>
```

## none

none屬性會讓元素消失，該元素不會在畫面中佔有任何空間。

常搭配javascript來動態讓元素消失出現。

```html
<style>
    .bye-bye {
        display: none;
    }
</style>
<p class="bye-bye">
    this is a p-tag
</p>
```

CSS中還有其他display的值，可以參考
https://www.w3schools.com/cssref/pr_class_display.asp

