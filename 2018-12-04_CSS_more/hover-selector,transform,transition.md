# 利用CSS製作互動感覺

簡單利用```:hover```來進行互動，搭配```transform```及```transition```來讓HTML元素有動畫的樣子

- :hover Selector
- transform
- transition

## :hover Selector

在CSS中，除了之前提過的3種Selector外，還有許多Selector，目前Ｗ3C的文件中有50多種。

reference: [W3C: CSS Selector](https://www.w3schools.com/cssref/css_selectors.asp)

然而為了增加網頁的互動性，來看一下 ```:hover```這個Selector。

```:hover``` selector 用來指定某元素**滑鼠指標放上去時候**的樣式

每個元素都可以指定```:hover```，不只有```<a>```標籤可以

```html
<style>
    .my-div {
        width: 100px;
        height: 100px;
        background: yellowgreen;
    }
    .my-div:hover {
        width: 300px;
    }
</style>
<div class="my-div"></div>
```

reference: [:hover Selector](https://www.w3schools.com/cssref/sel_hover.asp)

## transform

transform這個屬性可以讓元素進行2D或3D的轉變。

參考W3C的文件，尋找需要的transform值來使用。

reference: [CSS transform Property](https://www.w3schools.com/cssref/css3_pr_transform.asp)

```html
<style>
    img {
        transform: rotate(30deg);
    }
</style>
<img src="https://scontent.ftpe3-1.fna.fbcdn.net/v/t1.0-1/c13.0.200.200a/p200x200/25498269_380943475692311_4898207953166700082_n.jpg?_nc_cat=106&_nc_ht=scontent.ftpe3-1.fna&oh=03de467a8aab27e36a8700f4508cf5c3&oe=5CA521BF" alt="fat-cat">
```

## transition

transition屬性可以設定樣式轉變的時間，搭配前面提到的```:hover```Selector，可以製造動畫效果。

### 基本格式

```html
transition: 要設定的屬性 持續時間;
```

要設定的屬性，假設要讓```width```設定transition，就寫```width```。如果想要指定所有屬性，可以寫```all```。

持續時間，轉變過程持續的時間，沒有設定的話預設為0秒。

### 範例

```html
<style>
    img:hover {
        transform: scale(1.5,1.5);
        transition: transform 3s;
    }
</style>
<img src="https://scontent.ftpe3-1.fna.fbcdn.net/v/t1.0-1/c13.0.200.200a/p200x200/25498269_380943475692311_4898207953166700082_n.jpg?_nc_cat=106&_nc_ht=scontent.ftpe3-1.fna&oh=03de467a8aab27e36a8700f4508cf5c3&oe=5CA521BF" alt="fat-cat">
```