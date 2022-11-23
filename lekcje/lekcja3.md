# Lekcja 3 - Test wielokrotnego wyboru z checkboxami

W poprzedniej lekcji odpowiedź wielokrotnego wyboru można było udzielać wpisując litery do pola `<input`.

Tag (pole) `<input` domyślnie jest polem tekstowym. Ale może też być inputem innego typu.

Aby zmienić jego typ, należy zmienic jego atrybut `type`.

Domyślnie, jeśli jest pusty, to jest tekstowy; `<input>` to to samo co `<input type="text">`.

Do tego zadania przyda się Tobie `<input type="checkbox">`.

## Czego się nauczę?

- `<input type=checkbox checked`
- `<ul>`
- `<li>`
- `<p style="display=none"`
- `element.style.display="block" // "none"`
- CSS, a dokładniej to, że istnieje

## Zadanie na dziś - checkboxy wielokrotnego wyboru

Jako uczeń, który ma otwarty w przeglądarce plik index.html, widzę 2 pytania, na które chcę udzielić odpowiedzi oraz dowiedzieć się, czy udzieliłem prawidłowej odpowiedzi.

**Gdy** zaznaczę dowolną liczbę odpowiedzi  
**Oraz** przycisnę przycisk "sprawdź odpowiedzi"  
**Wtedy** Na spodzie, pod formularzem, pojawi się komunikat informujący o tym, czy prawidłowo uzupełniłem test.

### Treść i wygląd zadania

> Dlaczego Wokulski przerwał naukę w Szkole Głównej?
>
> - [ ] ponieważ zawiódł się na systemie nauczania
> - [ ] ponieważ zakochał się w Łęckiej
> - [ ] ponieważ rozpoczął pracę w sklepie Jana Mincla
> - [ ] ponieważ brał udział w powstaniu styczniowym
>
> Co było powodem wyjazdu Wokulskiego na wojnę rosyjsko-turecką do Bułgarii?
>
> - [ ] chęć odnalezienia przyjaciela - Ignacego Rzeckiego
> - [ ] chęć sprawdzenia umiejętności walki
> - [ ] chęć pomnożenia majątku i zaimponowania Izabeli
> - [ ] powołanie do służby wojskowej
> 
> <sprawdź odpowiedzi>

### Kryteria akceptacji

- Samodzielnie znajdziesz prawidłowe odpowiedzi na zdefiniowane pytania i prawidłowo je zaimplementujesz,
- Rezultatem zadania są 2 pliki: index.html oraz wielowybor.js

#### Zadanie dodatkowe:

Utwórz trzecie pytanie o lekturze Lalka, w którym wszystkie odpowiedzi są prawidłowe a domyślnie zaznaczona jest trzecia odpowiedź.

## Pomocne wskazówki

### Odczytywanie atrybutów w tagach htmlowych javascriptem

Z poprzedniej lekcji wiesz, że możesz odczytać wartość atrybutu "value" w polu "<input".

Robisz to poprzez odniesienie się do atrybutu po kropce `document.getElementById("wynik").value`.

Tak samo możesz sprawdzić dowolny atrybut znajdujący się w dowolnym tagu htmlowym.

popatrz na ten przykład:

```html
<ul>
  <li><input type="text" id="t1" value="Jestem input tekstowy">
  <li><input type="password" id="t2" value="Jestem input z hasłem">
  <li><input type="text" placeholder="Domyślny napis" id="t4">
  <li><input type="checkbox" id="tc1" value="odp1"> pierwszy checkbox
  <li><input type="checkbox" id="tc2" value="odp2"> drugi checkboks
  <li><input type="checkbox" id="tc3" value="odp3" checked> ten jest już zaznaczony
</ul>

<script>
console.log(document.getElementById("t1").value)
console.log(document.getElementById("t2").type)
console.log(document.getElementById("t4").id)
console.log(document.getElementById("tc1").value)
console.log(document.getElementById("tc2").checked)
console.log(document.getElementById("tc3").checked)
</script>
```

### Sprawdzanie wartości zaznaczonego checkboxa

1. Najpierw znajdź element (umiesz już szukać elementów po ich ID)
1. następnie sprawdź, czy jest zaznaczony (`checked`)
1. potem sprawdź `value` tego checkboxa i czy jego wartość pasuje od prawidłowej odpowiedzi

### Chowanie i pokazywanie elementów

Jednym ze sposobów na osiągnięcie tego zadania, jest manipulacja stylami CSS elementu.

[CSS](https://www.tutorialspoint.com/css/index.htm) to, w brutalnym skrócie, sposób na malowanie po stronie internetowej, sposób na zmianę wyglądu domyślnych elementów i umiejscawiania ich na ekranie.

CSSy można definiować na kilka sposobów.

1. Jako osobny plik "nazwa-pliku.css"
1. Jako część HTMLa `<style></style>`
1. Jako część elementów tagów `<input style="background:red">`

Sprawdź te przykłady:

```html
<style>
body{
  background:#000000;
  color:#ee1111;
}
div{
  background:yellow;
}
</style>

<div>jestem żółtym tagiem `div` na czarnej stronie, z czerwonym kolorem tekstu</div>
<div style="background:white; color:black; text-decoration:underline">A ja mam białe tło, czarny tekst i tekst jest podkreślony</div>
<p style="display:none">a mnie nie widać, bo jestem schowany</div>
<p id="hideme">A mnie schował skrypt javascriptowy</div>
<p id="showme">A mnie pokazał skrypt javascriptowy</div>

<script>
document.getElementById("hideme").style.display="none"
document.getElementById("showme").style.display="block"
</script>
```

