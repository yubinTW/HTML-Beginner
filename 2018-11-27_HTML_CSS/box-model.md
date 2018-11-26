# Box Model

每個HTML元素都是長方形! 就像一個box。

*Box Model 在HTML的排版上非常的重要*

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