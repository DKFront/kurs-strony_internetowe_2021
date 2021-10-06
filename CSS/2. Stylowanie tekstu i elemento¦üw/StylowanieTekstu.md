# Stylowanie tekstu

Zanim jednak zaczniemy bawić się w zmiany wyglądu elementów HTML warto wspomnieć o kilku ważnych aspektach. Jak już dobrze wiesz CSS oznaczna kaskadowy arkusz styli i kluczowym słowem w tym skrócie jest słowo **kaskadowy**.

Dlaczego? Ano dlatego, iż arkusz CSS jest czytany od góry do dołu, zatem jeżeli zdarzy Ci się zadeklarować dwa razy styl dla tego samego selectora, to ten który będzie na końcu będzie tym, który zostanie wyświetlony.

## Kolory i jednostki
W CSS możemy opisywać wartości kolorów na wiele sposobów:
* nazwa koloru w języku angielskim
* RGB lub RGBa - kolor w formacie RGB, `a` oznacza przezroczystość podawaną w zakresie od 0-1
* HSL lub HSLa -  kolor w formacie HSL, `a` oznacza przezroczystość podawaną w zakresie od 0-1
* wartość heksadecymalna - wartość w formacie szesnastkowym

Poniżej przykład deklaracji koloru na cztery sposoby:

|KOLOR|DEKLARACJA|WYNIK|
|----|----|----|
|White|nazwa koloru<br>**div {<br>background-color: white;<br>}**|<div style="background-color: white; height:50px;"></div>|
|Red |deklaracja RGB i RGBa <br>**div {<br>background-color: rgb(255, 0, 0);<br>}**<br><br>**div {<br>background-color: rgba(255, 0, 0, 0.2);<br>}**|<div style="background-color: rgb(255, 0, 0); height:50px;"></div><br><div style="background-color: rgba(255, 0, 0, 0.2); height:50px;"></div>|
|Green|deklaracja HSL i HSLa <br>**div {<br>background-color: hsl(120, 100%, 25%);<br>}**<br><br>**div {<br>background-color: hsla(120, 100%, 25%, 0.2);<br>}**|<div style="background-color: hsl(120, 100%, 25%); height:50px;"></div><br><div style="background-color: hsla(120, 100%, 25%, 0.2); height:50px;"></div>|
|Yellow|deklaracja heksadecymalna<br>**div {<br>background-color: #FFFF00;<br>}**<br>|<div style="background-color: #FFFF00; height:50px;"></div>|

Strona do dobierania kolorów.
* http://color.hailpixel.com

Strona do tworzenia palet kolorów.
* http://paletton.com

## Jednostki używane w css

Jednostki CSS dzielimy na dwa główne działy:
* absolutne
* relatywne

### Absolutne

Wartości absolutne to takie długości, które są przypisane do fizycznych odległości (np. centymetr, cal).

**Nie są skalowalne!**

Oznacza to, iż w momencie kiedy przyjdzie Ci tworzyć stronę mobilną lub na inny rozmiar niż komputera PC, jednostki absolutne zaczną Ci przeszkadzać. Będą a to za małe, a to za duże.
Jednak aby dobrze posługiwać się jednostkami relatywnymi najpierw musisz dobrze opanować jednostki absolutne.
Najpopularniejszą wartością absolutną jest piksel w skrócie - `px` równy dokładnie 1/96 cala.

### Relatywne

Nie bazują na stałej wielkości, a raczej na stosunku do innych wartości.

Najpopularniejsze z nich to:
* procent - `%`
* `em`
* `rem`

**Procenty**

Najczęściej wyrażamy nimi wielkość elementu w elemencie. **Nie możemy użyć procentów, jeżeli nie mają one swego rodzaju odnośnika względem czego chcemy nadać wartość np. 100%**

**EM**

Jest obliczana na podstawie wielkości czcionki zapisanej `<body>` lub relatwynie do podanej u rodzica elementu.

**`1em` jest zatem równy wartości podanej u rodzica w `px lub w elemencie `BODY` **

**REM**

Wielkość rem liczona jest bezpośrednio od najwyższego elementu naszego dokumentu (zazwyczaj od html), a nie od elementów nadrzędnych.

Wartość rem jest relatywna, jej wartość nadrzędną definiujemy raz, w elemencie html, po czym odnosimy się do niego bezpośrednio definiując wielkość czcionki dla poszczególnych elementów na stronie.

**`1rem` jest zatem równy wartości domyślnej w przeglądarce czyli około `16px` lub jeżeli podamy inną do tagu <html> w arkuszu stylii.**


## Właściwości do stylowania tekstu

Tabelka, którą zobaczysz poniżej ma służyc nauczeniu Cię właściwości jakie możesz nadać selektorom podzczas stylowania. Wartości, które tu zobaczysz są tylko cześciowo wypisane. Wszelakie wartości oraz właściwości jakie możesz używać do manipulowania tekstem znajdziesz [tutaj](https://developer.mozilla.org/pl/docs/Web/CSS/CSS_Reference)


|ZNACZENIE|WŁAŚCIWOŚĆ|POPULARNE WARTOŚCI|DEKLARACJA|PRZYKŁAD|
|-----|-----|-----|-----|-----|
|Nadanie koloru czcionki|`color`|tak jak opisałem wyżej są 4 deklaracje kolorów, najbardziej popularne to nazwa koloru i wartość heksadecymalna| **h1 {<br>color: red;<br>}**|<h1 style="color:red">Tekst</h1>|
|Zmiana stylu czcionki|`font-family`|nazwy czcionek np. `"Times New Roman"` lub rodziny czcionek: <ul><li>serif</li><li>sans-serif</li><li>monospace</li><li>cursive</li><li>fantasy</li></ul>|**h1 {<br>font-family: "Times New Roman", sans-serif;<br>}**<br> wartość po przecinku jest po to, gdyby przeglądarka nie rozpoznała czcionki pierwszej to wczyta kolejną która jest po przecinku|<h1 style="font-family: 'Times New Roman'">Tekst</h1>|
|Zmiana wielkości czcionki|`font-size`|Podajemy wartości w jednostkach relatywnych lub absolutnych|**p {<br>font-size: 45px;<br>}**|<p style="font-size:45px">Tekst</p>|
|Pochylenie tekstu|`font-style`|<ul><li>normal</li><li>italic</li><li>oblique</li><li>inherit</li></ul>|**h1 {<br>font-style: oblique;<br>}**|<h1 style="font-style:oblique">Tekst</h1>|
|Pogrubienie tekstu|`font-weight`|<ul><li>normal</li><li>bold</li>bolder</li><li>inherit</li><li>wartości liczbowe w zakresie 100-900.|**h1 {<br>font-weight: 700;<br>}**|<h1 style="font-weight:700">Tekst</h1>|
|Wyznaczenie odległości między liniami tekstu|`line-height`|Podajemy wartości w jednostkach relatywnych lub absolutnych|**p {<br>line-height: 50px;<br>}**|<p style="line-height:50px">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.<br> Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. </p>|
|Położenie tekstu w poziomie |`text-align`|<ul><li>left</li><li>right</li><li>center</li><li>justify</li><li>inherit</li></ul>|**p {<br>text-align: right;<br>}**|<p style="text-align:right">Tekst</p>|
|Położenie tekstu w pionie|`vertical-align`|<ul><li>baseline</li><li>top</li><li>bottom</li><li>middle</li><li>text-top</li><li>text-bottom</li><li>sub</li><li>super</li><li>top</li></ul><br>**vertical-align używamy najczęściej wewnątrz tabeli lub na elementach z wyświetlaniem table-cell**|**td {<br>vertical-align: bottom;<br>}**|<table><tr style="height:70px; vertical-align:bottom"><td >Tekst1</td><td>Tekst2</td><td>Tekst3</td></tr></table>|
|Podkreślenie lub przekreślanie tekstu UŻYWAMY GDY CHCEMY USUNĄĆ Z LINKÓW TĄ KRESKE POD|`text-decoration`|<ul><li>none</li><li>underline</li><li>overline</li><li>line-through</li><li>inherit</li></ul>|**h1 {<br>text-decoration: line-through;<br>}**|<h1 style="text-decoration: line-through">Tekst</h1>|
|Wysunięcie pierwszego słowa tekście|`text-indent`|Podajemy wartości w jednostkach relatywnych lub absolutnych|**p {<br>text-indent: 20px;<br>}**|<p style="text-indent: 20px">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>|
|Cieniowanie tekstu|`text-shadow`|Atrybut przyjmuje po kolei:<br><ul><li>koordynat x cienia</li><li>koordynat y cienia</li><li>wartość rozmycia w jednostkach relatywnych lub absolutnych</li><li>kolor - wpisany wg standardów opisanych wcześniej</li></ul><br> Wartości są oddzielone spacją i co ciekawe, pierwsze dwie mogą przyjmować wartości ujemne|**h1 {<br>text-shadow: 10px 10px 5px red;<br>}**|<h1 style="text-shadow: 10px 10px 5px red">Tekst</h1>|
|Zmiana wielkości liter w tekście|`text-transform`|<ul><li>none</li><li>capitalize</li><li>uppercase</li><li>lowercase</li><li>inherit</li></ul>|**h1 {<br>text-transform: uppercase;<br>}**|<h1 style="text-transform: uppercase">Tekst</h1>|
|Nadanie odległości między literami|`letter-spacing`|Podajemy wartości w jednostkach relatywnych lub absolutnych|**h1 {<br>letter-spacing: 10px;<br>}**|<h1 style="letter-spacing: 10px">Tekst</h1>|
|Nadanie odległości między wyrazami|`word-spacing`|Podajemy wartości w jednostkach relatywnych lub absolutnych|**h1 {<br>word-spacing: 30px;<br>}**|<h1 style="word-spacing: 30px">Tekst tekst</h1>|
|Definiowanie tła za pomocą kololru|`background-color`|Te same zasady co przy atrybucie `color`|**h1 {<br>background-color: red;<br>}**|<h1 style="background-color: red">Tekst</h1>|
|Przezroczystość tła|`opacity`|Wartości od 0-1. W przypadku wartości pomiędzy należy przedzielić je `.`|**h1 {<br>background-color: red; <br> opacity: 0.3<br>}**|<h1 style="background-color: red; opacity:0.3">Tekst</h1>|
|Obrazek jako tło|`background-image`|url('     ')|**p {<br>background-image: url('http://i.iplsc.com/zdj-ilustracyjne/0006DVXSTLL51M5U-C122-F4.jpg');<br>height: 100px;<br>background-size: contain;<br>background-repeat: no-repeat;<br>}**|<p style="background-image: url('http://i.iplsc.com/zdj-ilustracyjne/0006DVXSTLL51M5U-C122-F4.jpg'); height:100px; background-size:contain;background-repeat:no-repeat"></p>|
|Powtarzalność obrazka na stronie|`background-repeat`|Domyślnie jest on powtarzany na całej stronie. Zatem dostępne wartości to:<ul><li>repeat</li><li>repeat-x</li><li>repeat-y </li><li>no-repeat</li></ul> |**p {<br>background-image: url('http://i.iplsc.com/zdj-ilustracyjne/0006DVXSTLL51M5U-C122-F4.jpg');<br>height: 100px;<br>background-size: contain;<br>background-repeat: repeat;<br>}**|<p style="background-image: url('http://i.iplsc.com/zdj-ilustracyjne/0006DVXSTLL51M5U-C122-F4.jpg'); height:100px; background-size:contain;background-repeat: repeat"></p>|
|Wielkość obrazka względem podanej wielkości elementu|`background-size`|<ul><li>cover</li><li>contain</li><li>Wartości w jednostkach relatywnych lub absolutnych</li></ul>|**p {<br>background-image: url('http://i.iplsc.com/zdj-ilustracyjne/0006DVXSTLL51M5U-C122-F4.jpg');<br>height: 100px;<br>background-size: contain;<br>background-repeat: no-repeat;<br>}**|<p style="background-image: url('http://i.iplsc.com/zdj-ilustracyjne/0006DVXSTLL51M5U-C122-F4.jpg'); height:100px; background-size:contain;background-repeat:no-repeat"></p>|
|Pozycja gdzie obrazek ma być wyświetlony|`background-position`|<ul><li>top</li><li>right</li><li>bottom</li><li>center</li><li>Wartości w jednostkach relatywnych lub absolutnych</li>|||
|Stylowanie list `<ol>` `<ul>` `<dl>` |`list-style-type`| <ul><li>none</li><li>disc</li><li>circle</li><li>square</li><li>decimal</li></ul>|**ul {<br>list-style-type: square;<br>}**|<ul style="list-style-type: square"><li>Tekst1</li><li>Tekst2</li><li>Tekst3</li></ul>|
