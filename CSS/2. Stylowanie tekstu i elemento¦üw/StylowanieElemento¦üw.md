# Stylowanie Elementów

## Box model

Mała powtórka:

W HTML mamy dwa typy znaczników:
* blokowe – zajmują całą dostępną przestrzeń
• i zaczynają się na początku nowej linii (chyba
że stylowanie CSS to zmienia)

* inline – zajmują tylko tyle przestrzeni, ile potrzebują do wyświetlenia swojej zawartości.

Dzięki właściwości `display` możemy zmieniać podstawowe wyświetlanie danego elementu.

`Display` może przyjmować różne wartości, najbardziej popularne to:

* block
* inline-block
* flex
* grid
* table
* none

Czym zatem jest owy **box model**?

Wyobraź sobie, iż każdy element to pudełko, który może mieć swoją wysokość, szerokość, odstęp i przestrzeń jak i pozycje gdzie leży.

Dzięki takiemu zobrazowaniu lepiej zrozumiesz jak możesz manipulować elementami w podanych powyżej wymiarach.

Każdy box składa się z następujących warstw:
* width (całkowita szerokość elementu)
* height (całkowita wysokość elementu)
* padding (odległość od zawartości do obramowania)
* border (obramowanie zawartości)
* margin (odległość od obramowania do następnego boksa lub ramy strony)

**Każdy z tych atrybutów przyjmuje wartość liczbową z jednostką absolutną lub relatywną.**


Opiszmy sobie zatem po kolei każdy z tych atrybutów:
* **width** - Atrybut width ustawia bezwzględną szerokość boksu.

  Przy elementach typu **inline nie jest brany pod uwagę.**

  Dla atrybutów typu **block domyślnie jest ustawiony na 100%.**
* **height** - Atrybut height ustawia bezwzględną wysokość boksa.

  Przy elementach typu **inline nie jest brany pod uwagę**

* **margin** - margines, atrybut ustawiający odległość od obramowania boxa do następnego elementu lub ramy strony. Przy elementach typu **inline działa tylko na szerokość**.
Jeżeli obok siebie są dwa różnie wystylowane elementy, to odległość między nimi będzie równa większej wartości margin.

  Deklaracja atrybutu występuje w różnych odmianach:
  * Poprzez deklaracje każdej strony osobno słowami kluczowymi:
    * `margin-top`
    * `margin-right`
    * `margin-bottom`
    * `margin-left`
  * Poprzez deklarację 4 wartości oddzielonych spacją, które odpowiadają odpowiednim stroną marginesu:
    * górny
    * prawy
    * dolny
    * lewy
  * Poprzez deklarację 3 wartości oddzielonych spacją, które odpowiadają odpowiednim stroną marginesu:
    * górny
    * prawy i lewy
    * dolny
  * Poprzez deklarację 2 wartości oddzielonych spacją, które odpowiadają odpowiednim stroną marginesu:
    * górny i dolny
    * prawy i lewy
  * Poprzez deklarację 1 wartości, która odpowiada za wszystkie strony marginesu



* **padding** - margines wewnętrzny. Atrybut ustawiający odległość od zawartości boksu do jego obramowania.

  **Deklaracja wartości paddingu jest taka sama jak w przypadku marginesu**

* **border** - Atrybut border opisuje, jak zachowuje się obramowanie elementu.

  Deklaracja atrybutu wygląda następująco:
  * grubość obramowania -  wyrażana w wartościach z jednostką relatywną lub absolutną,
  *  styl obramowania:
    * dotted (kropkowane)
    * dashed (kreskowane)
    * solid (ciągłe)
    * double (dwie linie)
  *  kolor obramowania - tak jak w przypadku koloru czcionki

  ```css
  p {
      border: 2px solid red;
  }
  ```

  <div style="border: 1px solid grey; padding:10px">
    <p style="border: 2px solid red">Tekst w ramce</p>
  </div>

## Skoro wiesz już z czego składa się box model, zobaczmy zatem jakie sa opcje samego modelowania strony

W poniższym linku graficznie mamy przedstawione opcje box modelu, które ustalamy poprzez atrybut `box-sizing`

[Graficzny box sizing](https://codepen.io/carolineartz/full/ogVXZj)

## Przepłnienie - Overflow

W CSS możemy kontrolować sposób, w jaki dany element radzi sobie z zawartością, w wypadku gdy przekracza ona dostępną wielkość elementu.
Do tego celu służy nam właściwość overflow.

Właściwość overflow przyjmuje następujące wartości:
* visible
* auto
* scroll
* hidden
* inherit

Zobaczmy zatem jak wygląda `overflow:visible` oraz `overflow:hidden`

**Visible**
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Overflow visible</title>
    <link rel="stylesheet" href="./css/style.css">
  </head>
  <body>
    <div>
    Tekst który wykracza poza ramkę
    </div>
  </body>
</html>
```
```CSS
  div {
    width: 100px;
    height: 40px;
    overflow: visible;
    border: 1px solid red
  }
```

<div style="width:100px;height:40px;overflow:visible;border:1px solid red">
Tekst który wykracza poza ramkę
</div>

<br><br>
**Hidden**

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Overflow visible</title>
    <link rel="stylesheet" href="./css/style.css">
  </head>
  <body>
    <div>
    Tekst który wykracza poza ramkę
    </div>
  </body>
</html>
```
```CSS
  div {
    width: 100px;
    height: 40px;
    overflow: hidden;
    border: 1px solid red
  }
```
<div style="width:100px;height:40px;overflow:hidden;border:1px solid red">
Tekst który wykracza poza ramkę
</div>

## Zakrąglenie ramki czyli border-radius

Dzięki temu atrybutowi możemy ustawiać zaokrąglenie całego boksu.

**Zwykła ramka**
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Zwykłe obramowanie</title>
    <link rel="stylesheet" href="./css/style.css">
  </head>
  <body>
    <div>
    Tekst który jest w ramce
    </div>
  </body>
</html>
```
```CSS
  div {
    width: 200px;
    height: 100px;
    border: 2px solid red;
  }
```
<div style="width:200px;height:100px;border:2px solid red">
Tekst który jest w ramce
</div>

<br>
**Zaokrąglona ramka**
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Zaokrąglone obramowanie</title>
    <link rel="stylesheet" href="./css/style.css">
  </head>
  <body>
    <div>
    Tekst który jest w ramce zaokrąglonej
    </div>
  </body>
</html>
```
```CSS
  div {
    width: 200px;
    height: 100px;
    border: 2px solid red;
    border-radius: 10px 10px 10px 10px;
  }
```

<div style="width:200px;height:100px;border:2px solid red;border-radius: 10px 10px 10px 10px;">
Tekst który jest w ramce zaokrąglonej
</div>

## Cień elementu czyli box-shadow

Atrybut box-shadow służy do tworzenia cieni znajdujących się za elementem.
Przyjmuje on od dwóch do czterech wartości. Dwa pierwsze podają położenie cienia. Trzeci – rozmycie, a czwarty rozszerzanie się cienia.

Deklaruje się go identycznie jak `text-shadow`

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Elementy z cieniowaniem</title>
  </head>
  <body>
    <div></div>
  </body>
</html>
```

```CSS
div {
  height: 100px;
  width: 100px;
  box-shadow: -5px -5px 10px 10px red;
}
```

<div style="height:100px;width:100px;box-shadow: -5px -5px 10px 10px red"></div>

## Opływanie elementów - float

Atrybut float pozwala ustawiać elementy blokowe w jednej linii.
Możemy ustawiać je z lewej strony lub z prawej. Ważne aby suma szerokości wszystkich elementów w jednej linii wraz z ich marginesami i paddingami nie przekroczyła szerokości elementu rodzica bądź ramki strony lub 100% dostępnej szerokości.


```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div class="leftBox">
      Box z lewej strony
    </div>
    <div class="rightBox">
      Box z prawej strony
    </div>
  </body>
</html>
```
```CSS
.leftBox{
   width: 100px;
   height: 100px;
   border: 1px solid red;
   float: left;
}
.rightBox{
  width: 100px;
  height: 100px;
  border: 1px solid red;
  float: right;
}
```
<div style="width:400px;border:1px solid grey;padding:5px;height:110px">
  <div style="float:left;width:100px;height:100px;border:1px solid red">
    Box z lewej strony
  </div>
  <div style="float:right;width:100px;height:100px;border:1px solid red">
    Box z prawej strony
  </div>
</div>

### Clear:both

Powrót do naturalnego biegu dokumentu

Do naturalnego biegu dokumentów powrócimy za pomocą właśności clear:
* left – zsuniemy elementy poniżej wszystkich, które mają być ustawione float: left (ale nie float: right)
* right – zsuniemy elementy poniżej wszystkich,
które mają ustawione float: right (ale nie float: left)
* both – zsuniemy elementy poniżesz wszystkich
z właściwością float,
* none – jest to domyślna wartość, która wyłącza działanie clear


## Position

Position z ang. pozycja.
Domyślnie każdy element ma ustawioną pozycję statyczną – **static.**
Jest to naturalne ułożenie elementów na stronie, czyli od lewej do prawej (inline) i od góry do dołu (block).
Inne wartości position to:
* relative
* absolute
* fixed

### Position: relative

Jest to podobne ułożenie jak static, z tym że możemy przesuwać elementy za pomocą
własności:
* top
* right
* bottom
* left

Wartości jakich używamy powyższych własności to wartości numeryczne z jednostkami absolutnymi lub relatywnymi

### Position: absolute

Elementy z ustawionym position absolute są wyjęte z biegu dokument i akceptują przesunięcie o daną wartość tak jak relative z tym że ich relacja odnosi się albo do całego dokumentu albo do jego najbliższego rodzica, jeżeli posiada on `position:relative`.


Własności:
* top
* right
* bottom
* left

### Position: fixed

Elementy z ustawionym position fixed działają podobnie jak absolute, z tym że są pozycjonowane względem okna przeglądarki.
Podczas przewijania strony element z position fixed jest „przyczepiony” do okna.

Własności:
* top
* right
* bottom
* left

## Element na wierzchu i element pod nimi

`Z-index` to nazwa własności która decyduje w zależności od wartości wpisanej, który element będzie widoczny a który będzie za nim schowany.

`Z-index` przyjmuje wartości liczbowe **bez jednostek**

Domyślnie, zawsze ostatni element patrząc na kod html będzie przysłaniał resztę w sytuacji gdy najdą na siebie.

Oto przykład, gdzie użyjemy własności `position` bez `z-index`

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Position</title>
    <link rel="stylesheet" href="./css/style.css">
  </head>
  <body>

    <div class="container">
      <div id="redBox"></div>
      <div id="blueBox"></div>
    </div>

  </body>
</html>
```
```CSS
  .container {
    position: relative;
    border: 1px solid grey;
    height: 200px;
    width: 500px;
  }

  #redBox{
    position: absolute;
    top: 0;
    left: 0;
    background-color: red;
    width: 100px;
    height: 100px;
  }

  #blueBox{
    position: absolute;
    top: 50px;
    left: 50px;
    background-color: blue;
    width: 100px;
    height: 100px;
  }
```

<div style="position: relative;
padding: 20px;
border: 1px solid grey;
height: 200px;
width: 500px;">
  <div style="position: absolute;
  top: 0;
  left: 0;
  background-color: red;
  width: 100px;
  height: 100px;"></div>
  <div style="position: absolute;
  top: 50px;
  left: 50px;
  background-color: blue;
  width: 100px;
  height: 100px;"></div>
</div>

W przypadku użycia `z-index` sprawimy aby element czerwony był na wierzchu


```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Position</title>
    <link rel="stylesheet" href="./css/style.css">
  </head>
  <body>

    <div class="container">
      <div id="redBox"></div>
      <div id="blueBox"></div>
    </div>

  </body>
</html>
```
```CSS
  .container {
    position: relative;
    border: 1px solid grey;
    height: 200px;
    width: 500px;
  }

  #redBox{
    position: absolute;
    top: 0;
    left: 0;
    background-color: red;
    width: 100px;
    height: 100px;
    z-index:1;
  }

  #blueBox{
    position: absolute;
    top: 50px;
    left: 50px;
    background-color: blue;
    width: 100px;
    height: 100px;
    z-index: 0;
  }
```

<div style="position: relative;
padding: 20px;
border: 1px solid grey;
height: 200px;
width: 500px;">
  <div style="position: absolute;
  top: 0;
  left: 0;
  background-color: red;
  width: 100px;
  height: 100px;z-index:1;"></div>
  <div style="position: absolute;
  top: 50px;
  left: 50px;
  background-color: blue;
  width: 100px;
  height: 100px;z-index:0;"></div>
</div>
