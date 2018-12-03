# CSS priority

在CSS的使用上，常常會對元素的樣式重複定義，那瀏覽器會依照哪個定義來做樣式的設定，取決於以下幾點。

## 不同引用方式

設定在```style```屬性中的CSS，會大於```<style>```或```<link>```中所定義的

```html
<style>
    p {
        color: green;
    }
</style>
<p style="color: red;">This is p tag.</p>
<!-- 結果顯示紅色，因為inline的優先度最高 -->
```

## 若相同的Selector，後面定義的會覆蓋前面定義的屬性

```html
<style>
    p {
        color: red;
    }
    p {
        color: green;
    }
</style>
<p>This is p tag.</p>
<!-- 結果顯示綠色，因為後面的color覆蓋掉前面的color設定 -->
```

## 若不同的Selector作用於同一元素

id-selector > class-selector > tag-name-selector

```html
<style>
    p {
        color: red;
    }
    #my-id-p {
        color: blue;
    }
    .my-class-p {
        color: green;
    }
</style>
<p class="my-class-p">This is p tag.</p>
<p class="my-class-p">This is p tag.</p>
<p>This is p tag.</p>
<!-- 底下這個p標籤為藍色，因為id-selector優先度為高 -->
<p id="my-id-p" class="my-class-p">This is p tag.</p>
```

> 作用目標越少的，擁有越高的優先度