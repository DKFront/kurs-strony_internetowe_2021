# Dodawnie obrazków na stronie

Pliki graficzne jakie możemy dodać na strone muszą posiadać któreś z podanych niżej rozszerzeń:
* jpg, jpeg
* png
* gif

Za dodawnie obrazków do dokumentu HTML odpowiada znacznik `<img>`, który jest znacznikiem samodomykającym się.

Jednak sam znacznik `<img>` nie spowoduje, że doda się ten konkretny obrazek. Aby wskazać lokalizację na dysku lub w internecie obrazka, którego chcemy użyć, służy słowo kluczowe `src=""`. Pełna deklaracja wygląda zatem:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Obrazek</title>
  </head>
  <body>
    <img src="http://i.iplsc.com/zdj-ilustracyjne/0006DVXSTLL51M5U-C122-F4.jpg" alt="Kotek">
  </body>
</html>
```
<img src="http://i.iplsc.com/zdj-ilustracyjne/0006DVXSTLL51M5U-C122-F4.jpg" alt="Kotek">

Jak pewnie zauważyliście dodane zostało również słowo kluczowe `alt=""` służy ono do nazwania miejsca gdzie powinien się wyświetlić obrazk na wypadek gdyby jednak się nie pojawił.
