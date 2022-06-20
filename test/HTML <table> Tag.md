
[![Badge site](https://img.shields.io/badge/table-html5book.ru-red.svg)](https://html5book.ru/html-table/)

[![Badge site](https://img.shields.io/badge/shpargalka-html5book.ru-teal.svg)](https://html5book.ru/shpargalka-po-tablicam/)

[![Badge site](https://img.shields.io/badge/изучение_таблиц-developer.mozilla.org-teal.svg)](https://developer.mozilla.org/ru/docs/Learn/HTML/Tables/Basics)

[Изучения таблиц](https://developer.mozilla.org/ru/docs/Learn/HTML/Tables/Basics)
<br>
[Шпаргалка по работе с таблицами](https://html5book.ru/shpargalka-po-tablicam/)

Таблица создаётся при помощи парного тега `<table></table>`. Данный тег является контейнером для элементов таблицы и все элементы должны находиться внутри него. Например, с помощью данной разметки можно создать таблицу, состоящую из двух столбцов и двух строк:

```html
<table>
<tr>
<th>текст заголовка</th>
<th>текст заголовка</th></tr> <!--ряд с ячейками заголовков-->
<tr><td>данные</td>
<td>данные</td>
</tr> <!--ряд с ячейками тела таблицы-->
</table>
```
По умолчанию таблица и ячейки не имеют видимых границ. Границы задаются с помощью свойства `border`:

```css
/* внешние границы таблицы серого цвета толщиной 1px */
table {border: 1px solid grey;} 
/* границы ячеек первого ряда таблицы */
th {border: 1px solid grey;}
/* границы ячеек тела таблицы */
td {border: 1px solid grey;} 
```
## Стили для таблицы
С помощью стандартных способов оформления можно задать стиль для таблицы и всех её строк. Но как быть, если требуется, например, выделить отдельную ячейку? Чтобы не задавать для ячейки class, можно воспользоваться комбинацией селекторов и псевдоклассов.
В данном уроке приведены различные варианты отбора элементов таблицы с помощью структурных псевдоклассов.

## Разметка HTML
```html
<table>
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>
```
 <br>

### Table1:Первая строка таблицы.
```css
th {background: #C9E3FE;}
table {border: 1px solid grey;} 
```

<table class="table1">
<tr>
  <th style="background: #C9E3FE;">Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table2:Последняя строка таблицы.
```css
tr:last-child {background: #C9E3FE}
```
<table class="table2">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table3:Третья строка таблицы.
```css
tr:nth-child(3){background:#C9E3FE}
```
<table class="table3">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table4:Таблица-зебра. Каждая четная строка.
```css
tr:nth-child(even) {background: #C9E3FE}
```
<table class="table4">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table5:Таблица-зебра. Каждая нечетная строка таблицы.
```css
tr:nth-child(odd) {background: #C9E3FE}
```
<table class="table5">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table6:Первая ячейка первой строки таблицы.
```css
th:first-child {background: #c9e3fe;}
```
<table class="table6">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table7:Последняя ячейка первой строки таблицы. 
```css
th:last-child {background: #C9E3FE}
```
<table class="table7">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table8:Первая ячейка последней строки таблицы. 
```css
tr:last-child td:first-child {background: #C9E3FE}
```
<table class="table8">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table9:Последняя ячейка последней строки таблицы. 
```css
tr:last-child td:last-child {background: #C9E3FE}
```
<table class="table9">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table10:Третья ячейка третьей строки таблицы. 
```css
tr:nth-child(3) td:nth-child(3) {background: #C9E3FE}
```
<table class="table10">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table11:Первый столбец таблицы. 
```css
th:first-child, td:first-child {background: #C9E3FE}
```
<table class="table11">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table12:Третий столбец таблицы. 
```css
td:nth-child(3), th:nth-child(3) {background: #C9E3FE}
```
<table class="table12">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>

<br>

### Table13:Последний столбец таблицы. 
```css
th:last-child, td:last-child {background: #C9E3FE}
```
<table class="table13">
<tr>
  <th>Company</th>
  <th>Q1</th>
  <th>Q2</th>
  <th>Q3</th>
  <th>Q4</th>
</tr>
<tr>
  <td>Microsoft</td>
  <td>20.3</td>
  <td>30.5</td>
  <td>23.5</td>
  <td>40.3</td>
</tr>
<tr>
  <td>Google</td>
  <td>50.2</td>
  <td>40.63</td>
  <td>45.23</td>
  <td>39.3</td></tr>
<tr>
  <td>Apple</td>
  <td>25.4</td>
  <td>30.2</td>
  <td>33.3</td>
  <td>36.7</td>
</tr>
</table>






<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto+Flex:opsz,wght@8..144,100;8..144,200;8..144,300;8..144,400;8..144,500;8..144,600;8..144,700;8..144,800;8..144,900;8..144,1000&display=swap'); 

body{
    width: 90%;
    max-width: 960px;
    box-sizing: border-box;
    margin: 0 auto;
    font-size: 18px;
    color: #444;
    font-family: 'Roboto Flex', sans-serif !important;
}
h1,h2,h3,h4{ 
    color:#354361; 
    
}

a{
    color:#034ad8;
    text-decoration: none;
    font-weight: 500;
            
        }

table{
  border-collapse: collapse;
  width: 100%;
  }
 
 .table1 th {background: #C9E3FE;
      }
/* .table1 {border: 1px solid grey;
      } 
 .table1 td {border: 1px solid grey;
      } */
 .table2 tr:last-child {background: #C9E3FE;
      }
 .table3 tr:nth-child(3){background:#C9E3FE;
      }
 .table4 tr:nth-child(even) {background: #C9E3FE;
      }
 .table5 tr:nth-child(odd) {background: #C9E3FE;
      }
 .table6 th:first-child {background: #c9e3fe;
      }
 .table7 th:last-child {background: #C9E3FE;
      }
 .table8 tr:last-child td:first-child {background: #C9E3FE;
      }
 .table9 tr:last-child td:last-child {background: #C9E3FE;
      }
 .table10 tr:nth-child(3) td:nth-child(3) {background: #C9E3FE;
      } 
 .table11 th:first-child, .table11 td:first-child {background: #C9E3FE;
      }
 .table12 td:nth-child(3), .table12 th:nth-child(3) {background: #C9E3FE;
      }
 .table13 th:last-child, .table13 td:last-child {background: #C9E3FE;
      }
</style>
