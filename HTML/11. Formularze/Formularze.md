# Formularze `<form></form>`

Tak jak w przypadku tabeli, znacznik form podaje informację o tworzeniu formularza do przeglądarki.

Do stworzenia wewnętrznych elementów potrzebne są następujące znaczniki:

|ZNACZNIK|ZNACZENIE|PRZYKŁAD|
|----|----|----|
|`<label></label>`|Opis elementu formularza|<label>Opis checkboxa <input type="checkbox"</label>|
|`<input>`|Samodomykający się znacznik który potrzebuje wenętrzne słowa kluczowe jako właściwości czym owy `<input>` ma się "stać"|
|`<input type="text">`|słowo kluczowe `type="text"` powoduje utworzenie elementu z miejscem na wpisanie textu|<input type="text">|
|`<input type="password">`|słowo kluczowe `type="password"` powoduje utworzenie elementu z miejscem na wpisanie hasła, gdzie litery zamieniane są na kropki|<input type="password">|
|`<input type="email">`|`type="email"` daje informację przeglądarce, iż ma się spodziewać w tym miejscu wpisanego mailam wygląd i zachowanie tego znacznika jest takie samo jak znacznika z `type="text"`|<input type="email">|
|`<input type="submit" value="Wyślij">`|słowo kluczowe `type="submit"` powoduje utworzenie elementu odpowiadającego za wysłanie formularza do server, przyjmuje postać przycisku. Słowo kluczowe `value="Wyślij"` powoduje, iż napis wyświetlony na przycisku będzie **Wyślij** |<input type="submit" value="Wyślij">|
|`<input type="checkbox">`|słowo kluczowe `type="checkbox"` powoduje utworzenie pola wielokrotnego wyboru|<input type="checkbox"> <input type="checkbox">|
|`<input type="radio">`|słowo kluczowe `type="radio"` powoduje utworzenie pola jednkrotnego wyboru|<form><input type="radio"></form>|
|`<input type="reset">`|słowo kluczowe `type="reset"` powoduje utworzenie pola przycisku, który resetuje wszystkie pozostałe pola formularzu do wartości pustych lub domyślnych|<form><input type="text"><input type="reset"></form>|

Oprócz poznanych powyżej elementów `<input>`, warto poznać jeszcze następujące:

|ZNACZNIK|ZNACZENIE|PRZYKŁAD|
|-----|-----|-----|
|`<select></select>`|Powoduje utworzenie miejsca dla listy wyboru|<select></select>|
|`<option></option>`|Powoduje utworzenie pola w liście wyboru, deklaracja powinna wyglądać `<select><option>Pierwsza opcja</option><option>Druga opcja</option></select>`|<select><option>Pierwsza opcja</option><option>Druga opcja</option></select>|
|`<textarea></textarea>`|Powoduje utworzenie pola tekstowego|<textarea></textarea>|
|`<button></button>`|Powoduje utworzenie przycisku forumlarzowego|<button>Przycisk</button>|


Oto przykładowy formularz:
```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Formularz</title>
  </head>
  <body>
    <form action="index.html" method="post">
      <input style="display:block" type="text" name="imię"> Wpisz imię
      <input style="display:block" type="text" name="nazwisko"> Wpisz nazwisko
      <input style="display:block" type="password"> Wpisz hasło
      <textarea style="display:block"></textarea>
      <select>
        <option>Pierwsza opcja</option>
        <option>Druga opcja</option>
      </select>
      <label><input type="checkbox">Wybór 1</label>
      <label><input type="checkbox">Wybór 2</label>
      <input type="radio" value="M" name="wybor">M
      <input type="radio" value="K" name="wybor">K
      <input style="display:block" type="reset" value="Reset">
      <input type="submit" value="Wyślij">
    </form>
  </body>
</html>
```
<div style="border:1px solid grey">
  <form style="padding:10px" action="index.html" method="post">
    <input style="display:block" type="text" name="imię"> Wpisz imię
    <input style="display:block" type="text" name="nazwisko"> Wpisz nazwisko
    <input style="display:block" type="password"> Wpisz hasło
    <textarea style="display:block"></textarea>
    <select>
      <option>Pierwsza opcja</option>
      <option>Druga opcja</option>
    </select>
    <label><input type="checkbox">Wybór 1</label>
    <label><input type="checkbox">Wybór 2</label>
    <input type="radio" value="M" name="wybor">M
    <input type="radio" value="K" name="wybor">K
    <input style="display:block" type="reset" value="Reset">
    <input type="submit" value="Wyślij">
  </form>
</div>
