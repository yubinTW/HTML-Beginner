# Three Ways to Insert CSS

在HTML文件中使用CSS有三種方式
- internal
- external
- inline

## Internal Style Sheet

在HTML文件中，用```<style>```標籤定義CSS。

```html
<head>
    <style>
        p {
            background-color: lightgray;
        }
    </style>
</head>
<body>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Rerum, cupiditate.</p></p>
</body>
```

## External Style Sheet

不將CSS寫在HTML文件中，而是將CSS寫在```.css```的外部檔案內，接著在HTML文件中使用```<link>```標籤進行引用。

### 範例

有一個檔案```my-style.css```，內容如下
```css
p {
    background-color: lightgray;
}
```

在同一層目錄的HTML文件中，透過```<link>```標籤，指定href屬性

```html
<head>
    <link rel="stylesheet" href="./my-style.css">
</head>
<body>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Rerum, cupiditate.</p></p>
</body>
```

> ```<link>```標籤的href屬性，定義css檔案的資源在哪，可以寫相對路徑或絕對路徑

External的方式非常重要，可以將HTML與CSS進行分離，也可以讓CSS的定義重複使用在不同HTML文件中。

## inline

所謂的inline指的是將CSS定義在某個標籤的```style```屬性中，該CSS敘述只會對該標籤進行樣式設定

```html
<p style="color: red;">This is p tag.</p>
```

除非有特殊目的，否則一般好的網頁通常不會用這種方式來寫CSS

> 很亂，不易維護、修改、重複使用

# 總結三種方式

- internal style sheet，寫在```<style>```標籤中。
- external style sheet，利用```<link>```標籤引入其他.css文件。
- inline ，在HTML元素的```style```屬性中定義CSS樣式。