# Box Model

每個HTML元素都是長方形! 就像一個box。

**Box Model 在HTML的排版上非常的重要**

每一個HTML元素，看起來都長這樣

![](https://i.imgur.com/mIXtnWJ.png)


- Content 內容
    - 可能為文字或圖片，HTML元素實質要傳達的資訊
- Padding 內距
    - 內容到邊框的距離
    - padding是透明的
- Border 邊框
    - 包著內距，可以調整樣式寬度顏色
- Margin 外距
    - 邊框外的距離，可以用來調整與周圍元素的距離
    - margin是透明的

```html
<style>
    div {
        background-color: lightgrey;
        width: 300px;
        border: 25px solid green;
        padding: 25px;
        margin: 25px;
    }
</style>
<div>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
```

## 四個方向分開設定

margin及padding可以四個方向分開設定

可以利用
- margin-top
- margin-right
- margin-bottom
- margin-left
來分別對上右下左進行設定

padding也是類似
- padding-top
- padding-right
- padding-bottom
- padding-left


## 使用margin屬性，帶入不同個數的參數

margin屬性可以帶入多個參數

### 1個參數：同時設定上下左右
```css
margin: 1em;
```

### 2個參數：設定上下及左右
```css
margin: 3em 1em;
```

### 4個參數：設定上右下左
```css
margin: 1em 2em 3em 4em;
```

等價於
```css
padding-top: 1em;
padding-right: 2em;
padding-bottom: 3em;
padding-left: 4em;
```

> padding也是一樣

## block元素水平置中

block元素無法像文字一樣用```text-align```來置中

不過可以透過，設定左右margin相等的方式來達到置中的效果

```html
<style>
    * {
        margin: 0px;
        padding: 0px;
    }
    .content {
        width: 500px;
        background-color: #EEE;
        margin: 1em auto;
    }
</style>
<div class="content">
    <p>
        This is my paragraph.
    </p>
</div>
```
