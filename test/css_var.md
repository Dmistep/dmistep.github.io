## Переменные в css


CSS переменные (пользовательские CSS-свойства) это сущности, определяемые автором CSS, хранящие конкретные значения, которые можно повторно использовать в документе. Они устанавливаются с использованием custom property нотации (например. **--main-color: black;**) и доступны через функцию **var()** (например. **color: var(--main-color);**) .

Объявление переменной:

`:root { --main-bg-color: brown; } `

Использование переменной:

`element { background-color: var(--main-bg-color); }`

Пример:

```css
:root { --main-bg-color: brown; } 

.one { 
color: white; 
background-color: var(--main-bg-color); 
margin: 10px; width: 50px; 
height: 50px; 
display: inline-block; 
}
```
### Links:

[![Website](https://img.shields.io/website?label=CSS%2FUsing_CSS_custom_properties&style=for-the-badge&up_color=blue&up_message=https%3A%2F%2Fdeveloper.mozilla.org%2F&url=https%3A%2F%2Fdeveloper.mozilla.org)](https://developer.mozilla.org/ru/docs/Web/CSS/Using_CSS_custom_properties)

[A Complete Guide To CSS](https://www.lambdatest.com/blog/guide-to-css-variables-with-examples/)

[Chota. A micro (~3kb) CSS framework.](https://jenil.github.io/chota/#buttons)

[Переменные CSS](https://habr.com/ru/company/ruvds/blog/523370/)

<style>
body{
    color: #333;
    font-size:18px;
    width: 90%;
    max-width: 800px;
    margin: 0 auto;
}
a{
    text-decoration:none;
}
</style>


