# Różnica między znacznikiem `<div></div>` a `<span></span>`

Jako, że język HTML służy do tworzenia stron, a typów stron jest wiele, utarło się takie przekonanie, aby ustrukturyzować wygląd strony w jakiś konkretny sposób.

W czasach królowania HTML3 całość strony była oparta o tabele. Uzupełniając konkretne komórki uzupełnialiśmy tym samym menu, treści, linki, praktycznie wszystkie elementy i układ naszej strony był stały i bezproblemowy.

Z czasem kiedy popularne stały się telefony i tablety rekomendacji stawiania stron na tabelach odeszły do lamusa. Pojawił się swoisty następca - znacznik `<div>`.

`<div>` z ang. division - oddział, dywizja. W języku HTML bardziej można go określic jako sekcja. `<div>` wymyślono w jednym konkretnym celu - aby opakować w niego wszystkie potrebne elementy które chcemy poustawiać na stronie.

Zatem jak się już pewnie domyślacie `<div>` jest elementem blokowym. Nie ma on jakiejś konkretnej definicji tak jak `<p>` czy `<h1>`, pełni on po prostu rolę każdą jaką mu zadamy. Może przechowywać tekst bezpośrednio w sobie, choć to nie jest zalecane, może być przyciskiem jak go dobrze ostylujemy, może być banerem, menu ale przede wszystkim jest opakowaniem dla elementów wewnętrznych.


Czym więc jest `<span>`??

Jest on elementem liniowym i służy do łączenia lub rozdzielania ciągłego tekstu. O ile przykład dla ukazania dobroci jaką niesie za sobą korzystanie z `<div>` jest skomplikowane, o tyle dla `<span>` zraz wam pokażę.

Załóżmy, iż w paragrafie mamy tekst ciągły i chcemy aby poszczególne wyrazy były napisane kursywą i miały np. kolor czerwony. Nie będziemy przecież dzielić `<p>` na mniejsze bo nie ma to sensu. Z pomocą przychodzi span.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Span</title>
  </head>
  <body>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. <span>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</span>. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  </body>
</html>
```
```css
    span {
      font-style: oblique;
      color: red;
    }
```

<div style="border: 1px solid grey">
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. <span style="color: red;font-style: oblique">Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</span>. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
</div>
