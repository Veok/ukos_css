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
## Box model
W CSS, termin "box model" jest używany, gdy mówimy o projektowaniu i układzie strony internetowej. Box model jest w zasadzie pudełkiem, które owija się wokół każdego elementu HTML. Składa się on z: marginesów, obramowania, paddingu i właściwej zawartości strony. 

![Box model](https://media.emailonacid.com/wp-content/uploads/2018/08/Screen-Shot-2021-11-12-at-1.03.35-PM.png)

Objaśnienie poszczególnych części:

*Content - Zawartość boxu, w której pojawia się tekst i obrazy
*Padding - Oczyszcza obszar wokół zawartości boxu. Wypełnienie jest przezroczyste.
*Border - Obramowanie, które otacza padding i zawartość.
*Margin - oczyszcza obszar poza granicą. Margines jest przezroczysty.

Box model pozwala nam na dodanie obramowania wokół elementów, oraz na zdefiniowanie przestrzeni pomiędzy elementami.

## Przykładowe deklaracje
### background-color
Właściwość `background-color` ustawia kolor wskazanego elementu html.

Przykład:

```
body {background-color: red;}
```
### border-style
Właściwość `border-style` ustawia styl obramowania elementu. 

Przykład:

```
div {border-style: dotted;}
```

### margin
Właściwość `margin` ustawia marginesy dla elementu.

Przykład:

```
p {
  margin: 35px;
}
```
### padding
Właściwość `padding` ustala przestrzeń pomiędzy jego zawartością a obramowaniem.

Przykład:

```
p {
  padding: 35px;
}
```

### height
Właściwość `height` określa wysokość elementu.

Przykład:

```
p {
  height: auto;
}

h1 {
  height: 50px;
}
```
### width
Właściwość `width` określa szerokość elementu.

Przykład:

```
p {
  width: auto;
}

h1 {
  width: 50px;
}
```
### float
Właściwość `float` określa, czy element powinien być umieszczony na lewo, prawo lub wcale.

Przykład:

```
img  {
  float: right;
}
```

### div
Włsciwość `<div>` jest ogólnym kontenerem na zawortość strony HTML. Pozwala on na zgrupowaniu dowolnej ilości elementów HTMl wewnętrz jego ciała i na nadanie wspólnych właściwości stylu.

Przykład:

```
<!DOCTYPE html>
<html>
<head>
<style>
div {
  background-color: lightgrey;
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}
</style>
</head>
<body>

<h2>Demonstrating the Box Model</h2>

<p>The CSS box model is essentially a box that wraps around every HTML element. It consists of: borders, padding, margins, and the actual content.</p>

<div>This text is the content of the box. We have added a 50px padding, 20px margin and a 15px green border. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>

</body>
</html>

```

## Zadanie
Do wykonania zadania będzie potrzebny plik `index.html`, który powinien zostać wykonany podczas poprzednich laboratoriów. Twoim zadaniem jest:
1. Wystylizować użyty nagłówek za pomocą stylów `inline`
2. Stworzyć plik `styles.css` i zaimportować go do pliku `index.html`
3. Wystylizować pozostałe elementy pliku `index.html` używając co najmniej jednego ID selectora oraz class selectora. Style powinny zostać zdefiniowane w pliku `styles.css`. Podane niżej elementy strony powinny zostać wystylowane według poniższych wytycznych:
* strona powinna być koloru szarego
* krótka notka o sobie powinna zostać opatrzona klauzulą `div`, którego style powinny zostać ustawione według poniższej reguły:
kolor tła - czerwony, tekst powinien być pogrubiony, czcionka powinna być pochylona, margines z lewej strony powinien mieć wartość 0.5, padding od dołu powinien mieć wartość 0.5, element powinien być ustalony z lewej strony 
* każdy wiersz tabeli powinien być innego koloru. Należy również wystylować ramkę tabeli oraz ustawić jej szerokość na 50%
* lista z twoim hobby powinna być wystylowana według stylu [upper-roman](https://www.w3schools.com/css/css_list.asp)
* przycisk formularza do wysyłania maila, powinien mieć koloru `#0066ff` oraz mieć wystylowaną ramkę

Wykonane zadanie zacommituj i wypushuj do swojego repozytorium. Po wykonaniu zadania, poproś prowadzącego o sprawdzenie zadania.

---

Dokument oparty na ogólno dostępnych materiałach dostępnych na platformie [W3Schools](https://www.w3schools.com/).
