# HTML i HTML5 - czym jest i jak to zrozumieć?
<img style="position:relative; left:50%; transform:translateX(-50%); width=100%;height=100%" src="./HTML.png">

Język HTML to z ang. HyperText Markup Language – hipertekstowy język znaczników, wykorzystywany do tworzenia dokumentów hipertekstowych.

Dzięki niemu interpretator, czyli przeglądarka WWW jak Chrome czy Firefox, wie co ma nam pokazać.

Ale czym są te znaczniki? O tym dowiesz się za chwilę, najpierw trochę historii.


* **1993 r.** - Hypertext Markup Language, szkic opublikowany przez IETF - Internet Engineering Task Force czyli nieformalne stowarzyszenie osób zaintereoswanych ustalaniem standardów technicznych.

* **1995 r.** - Powstaje standard HTML 3.0 przestawiony do IETF przez formalną organizację W3C.

* **styczeń 1997 r.** - Opublikowany zostaje standard HTML 3.2 przez organizację W3C, która przejmuje od IETF kontrole nad standyracją działań w Internetowym świecie HTML.

* **grudzień 1997 r.** - Opublikowany zostaje standard HTML 4.0 przez W3C. Developerzy oprócz standardu 4.0 dostają 3 opcje tworzenia stron:
  * Bez możliwości używania wcześniejszych standardów
  * Z możliwością użycia wcześniejszych standardów
  * Z możliwością użycia elementów ramkowych

* **1999 r.** - Opublikowany zostaje standard HTML 4.01 przez W3C. Standard ten praktycznie zmienia drobne szczegóły w kodzie, jednak realnie nie ukazuje skoku jaki był zobserwowany w poprzednich latach.

* **2008 r.** - Opublikowany zostaje standard HTML5 przez W3C jako szkic nadchodzącej zmiany.

* **2014 r.** - Opublikowany zostaje w pełni standard HTML5 wraz z rekomendacją do wykorzystywania go przez Developerów


Zatem jak widzicie po tej krótkiej historii, na początku były szybkie a zarazem duże zmiany w małych odstępach czasowych, lecz póżniej organizacja W3C zmieniła strategię rekomendacji widząc jak mocno Internet się rozwija i wiedząc, że możliwości i szybkość wdrażania znacznie spadnie przez rozproszenie.

Do dziś zdarzają się sytuację, gdzie przeglądarki nie są w stanie wyświetlić poprawnie kodu, ze względu na jego nowoczesność w stosunku do rozwoju samej przeglądarki czy systemu operacyjnego.

## Język znaczników

```HTML
<h1> To jest znacznik nagłówka </h1>
```
Jak widzicie na przykładzie powyżej, HTML składa się ze słów kluczowych, w tym wypadku `h1`, które zapisane są w znacznikach czyli znakach mniejszości i większości `<>`. Jak już pewnie zauważyliście znaczniki występują w parze, tj. z lewej otwieramy, z prawej zamykamy dodając przed słowem kluczowym `/`, a wewnątrz wstawiamy interesujące nas treści.

## Struktura Języka HTML5

Dokument HTML, który ma być interpretowany przez przeglądarkę zawiera stały wzór, dzięki któremu interpretator wie z jakim plikiem ma do czynienia i co ma z nim zrobić.
W przypadku HTML wzór ten wygląda następująco.

```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Tytuł strony</title>
  </head>
  <body>
    <!--treśc strony-->
  </body>
</html>
```
Wzór ten możemy w pewien sposób przypisać do części ciała człowieka, lecz najpierw wyjaśnijmy czym jest magiczne `<!DOCTYPE hyml>` na samej górze przykładu

* `<!DOCTYPE html>` - jest to znacznik, który nie ma swojego zamknięcia, służy tylko i wyłącznie do informacji dla interpretatora(przeglądarki WWW), iż dalsza część dokumentu napisana będzie w standardzie HTML5

* `<html></html>` - otwierający dokument html. Wewnątrz zawarte muszą zostać wszystkie znaczniki, które użytkownik musi i chce wpisać.

* `<head></head>` - z ang. głowa. Znacznik ten jest mózgiem HTML, ponieważ pomiędzy nim zawierane są wszystkie najważniejsze kwestie takie jak:
  * tytuł strony `<title>Moja strona</title>`
  * rodzaj kodowania znaków `<meta charset="utf-8">` - obsługa polskich znaków
  * podpinanie / linkowanie kaskadowych arkuszy styli CSS, lub stylowanie dokumentu HTML z poziomu tego dokumentu
  * podpinanie / linkowanie do skryptów języka JavaScript lub np. PHP
  * określanie ustawień dla widoku i skalowania dokumentu np dla użądzeń mobilnych

* `<body></body>` z ang. ciało. Znacznik ten odpowiada za treść wyświetlaną w przeglądarce. O ile wszystko co wpiszemy w `<head>` nie pojawi się na stronie, o tyle w przypadku `<body>` elementy wpisane pomiedzy ten znacznik będą wyświetlane.
