# UKOS - CSS
## Co to jest CSS
CSS (Cascading Style Sheets) jest językiem, którego używamy do stylizacji stron internetowych. Dzięki CSS możesz kontrolować kolor, czcionkę, rozmiar tekstu, odstępy między elementami, jak elementy są pozycjonowane i układane i wiele więcej.
## Składnia
Reguła CSS składa się z selektora i bloku deklaracji.

![CSS Syntax](https://www.w3schools.com/css/img_selector.gif)

* Selektor wskazuje na element HTML, który ma zostać poddany stylizacji.
* Blok deklaracji zawiera jedną lub więcej deklaracji oddzielonych średnikami.
* Każda deklaracja zawiera nazwę właściwości CSS i wartość, które są oddzielone dwukropkiem.
* Wielokrotne deklaracje CSS są oddzielone średnikami, a bloki deklaracji są otoczone nawiasami klamrowymi.
## Jak użyć w HTML?
Gdy przeglądarka odczyta arkusz stylów, sformatuje dokument HTML zgodnie z informacjami zawartymi w tym arkuszu. Są trzy sposoby użycia arkusza styli w HTML.
### External
Dzięki zewnętrznemu arkuszowi stylów możesz zmienić wygląd całej strony internetowej, zmieniając tylko jeden plik. Każda strona HTML musi zawierać referencje do pliku zewnętrznego arkusza stylów wewnątrz elementu `<link>`, w sekcji head. Zewnętrzny arkusz stylów może być napisany w dowolnym edytorze i musi być zapisany z rozszerzeniem `.css`.
Zewnętrzny plik `.css` nie powinien zawierać żadnych znaczników HTML.

Przykład zewnętrznęgo pliku css:

```
body {
  background-color: red;
}

h4 {
  color: green;
  float: left;
}
```

### Internal
Wewnętrzny arkusz stylów może zostać zastosowany jeśli jedna strona HTML ma mieć unikalny styl.

Styl wewnętrzny jest definiowany wewnątrz elementu `<style>`, wewnątrz sekcji `<head>`.

Przykład:

```
<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color: red;
}

p {
  color: green;
  float: left;
}
</style>
</head>
<body>

<p>A tutaj mamy akapit</p>

</body>
</html>
```
### Inline
Styl inline może być użyty do zastosowania unikalnego stylu dla pojedynczego elementu na stronie. Aby go użyć, należy dodać atrybut `style` do odpowiedniego znacznika. Atrybut style może zawierać dowolną właściwość CSS.

Przykład:

```
<!DOCTYPE html>
<html>
<body>

<h1 style="color:blue;text-align:center;">Stylizacja nagłówka</h1>
<p style="color:red;">Stylizacja akapitu</p>

</body>
</html>
```
## Selektory
Selektory CSS są używane do "znajdowania" (lub wybierania) elementów HTML, które chcemy stylizować.

Selektory CSS możemy podzielić na pięć kategorii:

* Selektory proste (wybierają elementy na podstawie nazwy, id, klasy)
* Selektory kombinatoryczne (wybierają elementy na podstawie określonej relacji między nimi)
* Selektory pseudoklasowe (wybierają elementy na podstawie określonego stanu)
* Selektory pseudoelementów (wybierają i stylizują część elementu)
* Selektory atrybutów (wybierają elementy na podstawie atrybutu lub wartości atrybutu)

Poniżej znajduje się objaśnienie dla najbardziej podstawowych selektorów używanych w arkuszach styli.
### Element selector
Selektor elementów wybiera elementy HTML na podstawie nazwy elementu.

Przykład:
```
p {
  text-align: center;
  color: red;
}
```
### Id selector
Selektor identyfikatora używa atrybutu id elementu HTML do wybrania konkretnego elementu. Identyfikator elementu jest unikalny w obrębie strony, więc selektor id jest używany do wyboru tylko jednego unikalnego elementu. Aby wybrać element o określonym id, należy wpisać znak hash (#), a następnie nazwę identyfikatora elementu.

Przykład:

```
<!DOCTYPE html>
<html>
<head>
<style>
#para1 {
  text-align: center;
  color: red;
}
</style>
</head>
<body>

<p id="para1">Hello World!</p>
<p>This paragraph is not affected by the style.</p>

</body>
</html>
```
### Class selector
Selektor klasy wybiera elementy HTML z określonym atrybutem klasy. Aby wybrać elementy o określonej klasie, należy napisać znak kropki (.), a następnie nazwę klasy.

Przykład:

```
<!DOCTYPE html>
<html>
<head>
<style>
.center {
  text-align: center;
  color: red;
}
</style>
</head>
<body>

<h1 class="center">Red and center-aligned heading</h1>
<p class="center">Red and center-aligned paragraph.</p> 

</body>
</html>
```
### Grouping selector
Selektor grupujący wybiera wszystkie elementy HTML z tymi samymi definicjami stylów.

Przykład:

```
<!DOCTYPE html>
<html>
<head>
<style>
h1, h2, p {
  text-align: center;
  color: red;
}
</style>
</head>
<body>

<h1>Hello World!</h1>
<h2>Smaller heading!</h2>
<p>This is a paragraph.</p>

</body>
</html>
```
## Przykładowe znaczniki
### background-color
### opacity
### background-image
### border-style
### margin
### padding
### height
### width
### float
### box model - div
## Zadanie
Z poprzednich zajęć wystuluj index.html. Dla stylowania nagłówka użyj inline styli. Dla pozostałych stwórz plik styles.css i zaimportuj go do pliku HTML. Użyj co najmniej jednego id selectora oraz class selectora. Wystyluj każdy element:
1. Strona powinna mieć swój własny kolor
2. Krótka notka o sobie powinna być opatrzona divem i wystylowana:
    1. wlasny kolor
    2. bold
    3. italic
    4. margin left na 0.5
    5. padding bottom na 0.8
    6. float na left
3. Tabela:
    1. każdy wiersz powinien mieć inny kolor
    2. użyć border-style
    3. width na 50%
4. Lista hobby:
    1. style: upper-roman https://www.w3schools.com/css/css_list.asp
5. Formularz:
    1. Opis boldem
    2. Wystylować przycisk: kolor oraz border

---

Dokument oparty na ogólno dostępnych materiałach dostępnych na platformie [W3Schools](https://www.w3schools.com/).
