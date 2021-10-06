# CSS3 - czym jest i do czego służy ?
<img style="position:relative; left:50%; transform:translateX(-50%); width=100%;height=100%" src="./CSS.png">

Język CSS to  ang. Cascading Style Sheets - **kaskadowe arkusze stylów**, wykorzystywane do opisu formy wyświetlania strony WWW. Jak pewnie się już domyślacie, język ten również został opracowany przez organizację W3C.

Dzięki CSS przeglądarka wie jak dany znacznik HTML ma wyglądać wizualnie, czyli jaki ma mieć kolor, w którym miejscu ma się pojawić. Dzięki dokumentom CSS możemy dowolnie manipulować elementami HTML.

HTML może istnieć bez CSS jednak CSS nie może istnieć bez HTML bo nie będzie miał się do czego odwołać w kwestii stylowania.


## Historia CSS

* **1996 r.** - W3C publikuje rekomendację do używania języka CSS1, dzięki któremu możemy manipulować :
  * Czcionkami
  * Kolorami tekstu, tła
  * Wyglądem tekstu - odstępy między litermi, słowami itp.
  * Ustawieniem na stronie tekstu, obrazków, tabel itp.
  * Ustawianiem marginesów, obrysowań, odstępów między marginesem a elementem
  * Rozpoznawaniem przez CSS słów kluczowych `id` oraz `class`

* **1998 r.** - W3C publikuję rekomendację do używania zaktualizowanej wersji CSS1 o nazwie CSS2. Dodane zostają:
  * Możliwość dowolnego umiejscowienia elementów poprzez słowo kluczowe `position`, oraz jego właściwiości.
  * Możliwość wyboru, który element ma być na wierzchu, a który pod.
  * Nowe opcje stylowania czcionek jak i elementów poprzez np. dodawanie cienia.

* **2011 r.** - W3C publikuje aktualizację do pewnych rozwiązań CSS nadając im nazwę CSS2.1. Ciekawostką jest fakt, iż W3C w przypadku języka CSS zaczęło rozwarstwiać aktualizację wypuszczając kolejno nowe możliwości w odstępie miesięcznym lub półrocznym nie zmieniając nazwy kodowej języka.

* **2012-2015 r.** - W3C wypuszczając pomniejsze aktualizację doprowadza do wprowadzenia języka CSS3 lub rzadziej nazywany CSS2.2 dodając choćby możliwości obsługi strony na urządzeniach mobilnych i dostosowując również możliwości wyświetlania stron dla osób niepełnosprawnych.

## Jak wygląda język CSS ?

Jego wygląd możemy podzielić w zależności od sposobu jego deklaracji dla dokumentu HTML.
Dodatkowo musimy sobie powiedzieć jeszcze na temat "mocy" deklaracji języka CSS.

**Czym więc jest ta tajemna "moc"?**

Moc deklaracji CSS wywodzi się bezpośrednio z miejsca deklaracji stylu. Im bliżej znajduje się on miejsca występowania konkretnego znacznika HTML tym większą ma moc nad inną deklaracją tego samego znacznika.

**Trzeba jednak zaznaczyć, iż mamy 3 możliwości deklaracji ów styli**
 * **Deklaracja Inline**- czyli z ang. w linii. Deklaracja ta odbywa się bezpośrednio w znaczniku HTML poprzez dodanie wewnątrz tego znacznika słowa kluczowego `style=""`. Pomiędzy cudzysłowami deklarujemy co chcemy zmienić i jaką wartość chcemy nadać. Przykładowa deklaracja koloru czerwonego dla paragrafu wygląda następująco:
 <br>
 ```html
 <!DOCTYPE html>
 <html>
   <head>
     <meta charset="utf-8">
     <title>Czerwony paragraf</title>
   </head>
   <body>
     <p style="color:red">Jestem czerwony</p>
   </body>
 </html>
 ```
 <p style="color:red">Jestem czerwony</p>

 Oczywiście możemy dodać więcej styli oddzielając ich właściwości znaczkiem `;`. Przykładowo chcemy zmienić tło tego paragrafu na żółty.

 ```html
 <!DOCTYPE html>
 <html>
   <head>
     <meta charset="utf-8">
     <title>Czerwony paragraf na żółtym tle</title>
   </head>
   <body>
     <p style="color:red; background-color:yellow">Jestem czerwony i mam żółte tło</p>
   </body>
 </html>
 ```
 <p style="color:red; background-color:yellow">Jestem czerwony i mam żółte tło</p>

 * **Deklaracja poprzez znacznik `<style></style>` w znaczniku `<head></head>`.**<br> Tak jak opisywałem HTML, znacznik `<head>` przekazuje ważne treści do przeglądarki, w tym wypadku przekazuje jej, aby brała pod uwagę style zadeklarowane w znaczniku `<style>`.<br> Zobaczmy zatem ten sam przykład zadeklarowany poprzez znacznik `<style>` w znaczniku `<head>`

 ```html
 <!DOCTYPE html>
 <html>
   <head>
     <meta charset="utf-8">
     <title>Style w znaczniku &lt;style&gt;</title>
     <style>
        p {
          color: red;
          background-color: yellow;
        }
     </style>
   </head>
   <body>
     <p>Jestem czerwony i mam żółte tło</p>
   </body>
 </html>
 ```
  <p style="color:red; background-color:yellow">Jestem czerwony i mam żółte tło</p>

  Jak już pewnie zauważyliście, deklaracja poprzez tag style wygląda inaczej. Przeanalizujmy ją

  ```html
  <style>
    p {
      color: red;
      background-color: yellow;
    }
  </style>
  ```
Najpierw otwieramy znacznik `<style>`, następnie musimy podać co chcemy ostylować. W tym wypadku chcemy dodać style do elementu `<p>`. Nie potrzebujemy już tutaj znaczników pomiedzy literą `p` ponieważ przeglądarka wie, iż aktualnie analizuje język CSS. Deklaracja tagu odbywa się zatem bez znaczników i fachowo nazywa się `selector`. Następnie otweiermy nawiaz klamrowy i pomiędzy nim deklarujemy właściwości oraz ich wartości.
W naszym wypadku właściowościami są kolejno `color` oraz `background-color` a ich wartościami `red` oraz `yellow;`
<br><br>Na poniższym obrazku mamy przykład deklaracji stylów dla elementu `<h1>` wraz z opisem fachowych nazw poszczególnych elementów deklaracji.
<br>
![selector](./selector.gif)
<br>
Dla lepszego wzorkowego zrozumiena zalecam zapis gdzie każdą deklarację oddzielamy linią tak jak w przykładzie deklaracji dla znacznika `<p>`

* **Deklaracja poprzez zewnętrzny plik CSS.** Ostatnim sposobem deklaracji stylii dla dokumentu HTML jest podlinkowanie zewnętrznego dokumentu CSS o rozszerzeniu `.css` poprzez wpisanie takiego samodomykającego się znacznika `<link>` w znacznik `<head>`:
<br>
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>CSS z zewnętrznego pliku</title>
    <link rel="stylesheet" href="./css/style.css">
  </head>
  <body>
    <p>Jestem czerwony i mam żółte tło</p>
  </body>
</html>
```
Przeanalizujmy go zatem:
```html
<link rel="stylesheet" href="./css/style.css">
```
  * `rel` daję informację przeglądarce czego ma się spodziewać w linkowanym pliku. W tym wypadku `stylesheet` czyli dokumentu ze stylami
  * `href` już znacie. Wskazujemy gdzie ma przeglądarka ma szukać. Opiszmy zatem zapis `"./css/style"`
    * `"./"` oznacza, iż Przeglądarka ma szukać wejściowo w tym samym folderze gdzie jest plik HTML.
    * `/css` oznacza, iż ma znaleźć wejść do folderu o nazwie `css`
    * `/style.css` oznacza, iż ma znaleźć wejść do pliku o nazwie `style` z rozszerzniem `.css`

  A tak wygląda zapis deklaracji w linkowanym pliku CSS
  ```CSS
  p {
    color: red;
    background-color: yellow;
  }
  ```


**W ten sposób poznaliście doklarację CSS oraz jak wygląda jego składnia, ale jak to się ma do wspomnianej "mocy"?**

Otóż ma się następująco:
* **Liniowa deklaracja** jest zawsze najważniejsza przez co nie jest zalecana do stylowania przy dużych projektach
* **Deklaracja poprzez znacznik `<style></style>`** w znaczniku `<head>` w pliku HTML jest druga w hierarchii. Rzadko używana i spotykana.
* **Deklaracja poprzez zewnętrzny plik CSS** jest ostatnia w hierarchi z najmniejszą mocą, ale z największymi możliwościami oraz zawsze rekomendowana przez programistów przede wszystkim ze względu na czytelność kodu.

## Selektory CSS

Selektorem CSS może być:
  * nazwa znacznika
  * nazwa klasy
  * nazwa identyfikatora

  Oto przykłady deklaracji dla każdego z powyższych slektorów


  |SELEKTOR|DEKLARCJA CSS|
  |----|----|
  |`<p>Czerwony paragraf</p>`|p { <br>    color: red;<br>}|
  |`<p class="paragrafKlasa">Czerwony paragraf</p>`|.paragrafKlasa {<br>color: red;<br>}|
  |`<p id="paragrafId">Czerwony paragraf</p>`|#paragrafId {<br> color: red;<br>}|
