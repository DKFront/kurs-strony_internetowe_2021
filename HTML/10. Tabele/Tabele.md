# Tabele `<table><table>`

Znacznikiem odpowiadającym za rozpoczęcie tworzenia tabeli w dokumencie HTML jest `<table>`. Samo użycie znacznika nie wyrysuje jednak tabeli. Znacznik ten daje informację przeglądarce, iż teraz będzie się tworzyła tabela do wyświetlenia.

Do utworzenia tabeli potrzebujemy zatem kolejnych znaczników:

|ZNACZNIK|ZNACZENIE|
|----|----|
|`<thead></thead>`|znacznik nagłówka tabeli|
|`<tbody></tbody>`|znacznik ciała tabeli|
|`<tfoot></tfoot>`|znacznik stopki tabeli|
|`<tr></tr>`|znacznik odpowiadający za stworzenie wiersza|
|`<th></th>`|znacznik odpowiadający za komórkę nagłówka|
|`<td></td>`|znacznik odpowiadający za zwykłą komórkę|


Przykład tabeli z danymi:
```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Tabele</title>
  </head>
  <body>
    <table>
      <thead>
        <tr>
          <th>Nazwa książki</th>
          <th>Autor</th>
          <th>Ilość sprzedanych sztuk</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Don Quixote</td>
          <td>Miguel de Cervantes</td>
          <td>500 millionów</td>
        </tr>
        <tr>
          <td>Harry Potter and the Philosopher's Stone</td>
          <td>J. K. Rowling</td>
          <td>107 millionów</td>
        </tr>
        <tr>
          <td>The Hobbit</td>
          <td>J. R. R. Tolkien</td>
          <td>100 millionów</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td></td>
          <td></td>
          <td>707 millionów</td>
        </tr>
      </tfoot>
    </table>
  </body>
</html>
```
<div style="border:1px solid grey;padding:10px">
  <table>
    <thead>
      <tr>
        <th>Nazwa książki</th>
        <th>Autor</th>
        <th>Ilość sprzedanych sztuk</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Don Quixote</td>
        <td>Miguel de Cervantes</td>
        <td>500 millionów</td>
      </tr>
      <tr>
        <td>Harry Potter and the Philosopher's Stone</td>
        <td>J. K. Rowling</td>
        <td>107 millionów</td>
      </tr>
      <tr>
        <td>The Hobbit</td>
        <td>J. R. R. Tolkien</td>
        <td>100 millionów</td>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <td></td>
        <td></td>
        <td>707 millionów</td>
      </tr>
    </tfoot>
  </table>
</div><br>
Słowa kluczowe `rowspan=""` oraz `colspan=""` służą do łączenia komórek w jedną większą patrząc przez pryzmat wiersza - rowspan, oraz kolumny - colspan.
