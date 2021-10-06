# Listy HTML

## Lista uporządkowana `<ol></ol>`

`<ol>` - z ang. ordered list - lista uporządkowana. Wewnątrz tego tagu wszystko co wpiszemy będzie osobnym elementem listy porządkowej. Wewnętrzne wartości wpisujemy pomiędzy tag `<li></li>` oznaczającym jeden element listy.

Oto przykład :
 ```HTML
 <!DOCTYPE html>
 <html>
   <head>
     <meta charset="utf-8">
     <title>Lista zakupów</title>
   </head>
   <body>
     <h3>Lista zakupów></h3>
     <ol>
       <li>Owoce</li>
       <li>Warzywa</li>
       <li>Mięso</li>
       <li>Nabiał</li>
       <li>Chemia</li>
     </ol>
   </body>
 </html>
 ```
 <div style="border:1px solid grey">
  <h3>Lista zakupów</h3>
   <ol>
     <li>Owoce</li>
     <li>Warzywa</li>
     <li>Mięso</li>
     <li>Nabiał</li>
     <li>Chemia</li>
   </ol>
 </div>


## Lista nieuporządkowana `<ul></ul>`

`<ul>` - z ang. unordered list - lista nieuporządkowana. Wewnątrz tego tagu wszystko co wpiszemy będzie osobnym elementem listy tak jak w przypadku `<ol>`. Wewnętrzne wartości wpisujemy pomiędzy tag `<li></li>` oznaczającym jeden element listy.


Oto przykład :
 ```HTML
 <!DOCTYPE html>
 <html>
   <head>
     <meta charset="utf-8">
     <title>Moja lista zakupów</title>
   </head>
   <body>
     <h3>Lista zakupów></h3>
     <ul>
       <li>Owoce</li>
       <li>Warzywa</li>
       <li>Mięso</li>
       <li>Nabiał</li>
       <li>Chemia</li>
     </ul>
   </body>
 </html>
 ```
 <div style="border:1px solid grey">
   <h3>Lista zakupów</h3>
   <ul>
     <li>Owoce</li>
     <li>Warzywa</li>
     <li>Mięso</li>
     <li>Nabiał</li>
     <li>Chemia</li>
   </ul>
  </div>


## Lista definicji `<dl></dl>`

`<dl>` - z ang. definition list - lista definicji.

Wewnątrz tego tagu deklaracja wartości różni się nieco od poprzednich list. Przede wszystkim, znacznik `<dl>` składa się z
* znacznika `<dt>` - z ang. definition title - tytuł definicji
* znacznika `<dd>` - z ang. definition description - opis definicji

Zatem w przypadku listy definicji nie będziemy już używać znacznika `<li>` ponieważ zastępują go tutaj `<dt></dt>` oraz `<dd></dd>`.

Oto przykład :
```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Lista definicji</title>
  </head>
  <body>
    <h3>Lista definicji</h3>
    <dl>
      <dt>Czym jest &lt;ul&gt;?</dt>
      <dd>Jest to lista nieuporządkowana</dd>
      <dt>Czym jest &lt;ol&gt;?</dt>
      <dd>Jest to lista uporządkowana</dd>
    </dl>
  </body>
</html>
```
<div style="border:1px solid grey">
  <h3>Lista definicji</h3>
  <dl>
    <dt>Czym jest &lt;ul&gt;?</dt>
    <dd>Jest to lista nieuporządkowana</dd>
    <dt>Czym jest &lt;ol&gt;?</dt>
    <dd>Jest to lista uporządkowana</dd>
  </dl>
</div>

<br>

Jak zauważyliście już pewnie w kodzie użyłem takich sformułowań `&lt;` oraz `&gt;`. Z racji tego, iż język HTML posługuje się znacznikami **<** oraz **>** zapisanie w kodzie HTML znacznika `<ul>` bez jego swoistego użycia musi być zapisane inaczej. W tym przypadku z pomocą przychodzą nam kody ASCII oraz zapisane przez programistów skróty - less than czyli `lt` oraz greater than czyli `gt` poprzedzone znaczkiem `&` oraz zakończone `:`. Taki zapis da nam odpowienio znaczek **<** oraz **>**.

Drugą rzeczą na którą powinniście zwrócić uwagę jest sposób zapisywania kodu HTML.
Jak widzicie im więcej jest kodu tym więcej stosuje wcięć w tekście. Ułatwia to poruszanie się po kodzie, jak i rozróżnienie, który element nalezy do którego elementu, na przykład element `<li>` jest dzieckiem elementu `<ul>` a element `<ul>` jest dzieckiem `<body>`.
