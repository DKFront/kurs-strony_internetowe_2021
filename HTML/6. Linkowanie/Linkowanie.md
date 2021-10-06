# Linkownanie - zakotwiczenie

Anchor - z ang. kotwica, w ten sposób został wymyślony tag `<a></a>` który odpowiada za linkowanie do innej strony, zdjęcia lub miejsca, które się mu wskaże.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Linki do stron</title>
  </head>
  <body>
    <p>oto link do strony <a href="http://www.wp.pl">www.wp.pl</a></p>
  </body>
</html>
```
<div style="border:1px solid grey">
  <p>oto link do strony <a href="http://www.wp.pl">www.wp.pl</a></p>
</div><br>

Tag `<a>` zawiera wewnętrzną właściwość `href`. Przeanalizujmy zatem jak wygląda poprawne linkowanie do zewnętrznej strony.

Deklaracja:

`<a href="http://www.wp.pl">wp.pl</a>`

* znacznik `<a>` trzeba ręcznie zamykać
* wewnątrz trzeba wpisać słowo kluczowe `href` - z ang. hypertext reference czyli hypertextowe odwołanie.
* po wpisaniu atrybutu `href` należy wpisać miejsce do którego chcemy linkować, zatem dopisujemy znak `=`a po nim w cudzysłowie lub apostrofach wpisujemy adres. W przypadku stron www, należy wpisać przed adresem `http://`
