# 常見標籤介紹

## 標題 h1, h2, h3, h4, h5, h6

定義標題(headings)

```<h1>```代表最重要的標題，```<h6>```表示最不重要的標題

在主流瀏覽器中，```<h1>```預設顯示的字體大小最大，```<h2>```次之，依此類推

```html
<h1>This is heading 1</h1>
<h2>This is heading 2</h2>
<h3>This is heading 3</h3>
<h4>This is heading 4</h4>
<h5>This is heading 5</h5>
<h6>This is heading 6</h6> 
```

[headings tag reference](https://www.w3schools.com/tags/tag_hn.asp)

## 段落 p

定義段落(paragraph)

```html
<p>
  人生短短幾個秋呀，不醉不罷休。東邊我的美人哪，西邊黃河流。來呀來個酒啊不醉不罷休，愁情煩事別放心頭。
</p>
```

[p tag reference](https://www.w3schools.com/tags/tag_p.asp)

## 超連結 a

定義超連結(hyperlink)，用以跳轉到某個目標資源

```html
<a href="https://www.facebook.com/catfatorange/" target="_blank">肥橘</a>
```

### href屬性
定義該a標籤的跳轉目標，格式為URL

### target屬性
定義從哪裡該起該目標連結

常用target值：
- ```_self```，預設值，在本頁面開啟連結
- ```_blank```，開新分頁，在該分頁開啟連結

[a tag reference](https://www.w3schools.com/tags/tag_a.asp)

## 圖片 img
定義圖片(image)

```html
<img src="圖片URL" alt="替代文字">
```

### src屬性
```<img>```標籤最重要的屬性，必須能正確連結到要顯示的圖片資源，URL格式

### alt屬性
替代文字，如果src屬性定義的目標資源無法正確拿到圖片，瀏覽器會顯示替代文字

- ```<img>```標籤只有頭，沒有尾。不用寫```</img>```。
- src屬性與alt屬性都要定義

```html
<img src="https://scontent.ftpe8-3.fna.fbcdn.net/v/t31.0-8/25438742_380943475692311_4898207953166700082_o.jpg?_nc_cat=106&_nc_ht=scontent.ftpe8-3.fna&oh=6828cc16901681afdefcfb801d7b1f6f&oe=5C81C095" alt="肥橘">
```

[img tag reference](https://www.w3schools.com/tags/tag_img.asp)
