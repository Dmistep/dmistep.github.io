---
#layout: post
#tags: []
#categories: []
date: 2019-06-25 13:14:15
#excerpt: ''
#image: 'BASEURL/assets/blog/img/.png'
#description:
#permalink:
title: 'Свойство word-wrap'
---


Свойство word-wrap позволяет разбивать длинные слова и переносить их на следующую строку. Свойство имеет два значения: **normal** и **break-word**. 

В нижеуказанном примере свойство **word-wrap** имеет значение **break-word**.

```css
p {
    width: 210px; 
    height: 100px;
    border: 1px solid #000000;
    word-wrap: break-word;
}
```
*Результат:*

<p class="wrap">This paragraph has a long word: thisisaverylongwordbutyoucantfinditinthedictionary.</p>


Когда свойство **word-wrap** имеет значение **break-word**, браузер разбивает слово, если оно не помещается по ширине в заданную область.

<style>
 .wrap {
    width: 210px; 
    height: 100px;
    border: 1px solid #000000;
    word-wrap: break-word;
}
header {
  display: none;
}
</style>
