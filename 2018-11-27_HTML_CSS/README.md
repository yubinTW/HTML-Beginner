# HTML and CSS basic

2018-11-27 HTML第二次上課

今天會講一些HTML標籤，然後介紹CSS要怎麼使用及常見的CSS屬性

## 常見標籤

[清單ol,ul、iframe、div、span](tag_ol,ul,iframe,div,span.md)

# CSS 基本語法

在HTML文件中，可以透過```<style>```標籤定義CSS。

```html
<style>
  h1 {
      color: blue;
  }
</style>
```

```css
h1 { color: blue; font-size: 12px; }
```
![](https://i.imgur.com/1DtqKZh.png)

- Selector
    - 對誰做效果
        - tag name
        - id
        - class
- 大括號內為CSS樣式宣告
- property : value，指定某個樣式為某個值
- 分號結尾
- 可多行定義

```css
h1 {
    color: blue;
    font-size: 12px;
}
```

善用縮排，增加可讀性。

# CSS Selector

基本的三種selector，用來指定要對那些元素套用CSS的樣式

- Element Selector
- Id Selector
- Class Selector

## Element Selector

根據標籤來套用效果，套用CSS樣式到所有相同標籤上。

```css
p {
    color: blue;
}
```

## Id Selector

套用CSS樣式到某個具有特定id的元素上。

```html
<style>
    #first {
        color: blue;
    }
</style>
<p id="first">This is my first paragraph.</p>
```

- HTML中要先定義好id的屬性
- 一個HTML文件中，id必須唯一，不可重複
- 利用井字號(```#```)加上id名稱作為selector

## Class Selector

套用CSS樣式到某些具有特定class的元素上

```html
<style>
    .my-p {
        color: blue;
    }
</style>
<p class="my-p">This is my paragraph.</p>
<p >This is not my paragraph.</p>
<p class="my-p">This is my paragraph.</p>
```

- 有相同class的元素會套用該class所設定的樣式
- 可以多個元素具有相同class
- 利用點(```.```)加上class名稱作為selector

# CSS 註解 /* */

```/* */```標籤定義CSS的註解

```html
<style>
    /* 這個class用來表示警告 */
    .alert {
        color: red;
    }
</style>
```

- 多利用註解，解釋你的想法
- 可以多行註解
- 被註解敘述，瀏覽器會無視
- 注意開始(```/*```)及結束(```*/```)的標籤都要存在，中間定義註解的文內容

# CSS 常用樣式介紹

[一些常用的](css.md)