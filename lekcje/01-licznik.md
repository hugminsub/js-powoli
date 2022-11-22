# Lekcja pierwsza

> Rób -> nauczysz się.

## Licznik - polecenie

Jako użytkownik, który ma otwarty plik `index.html` w przeglądarce, chcę modyfikować licznik poprzez klikanie w przycisk `+` oraz `-`.

**Gdy** kliknę w przycisk `+`  
**Wtedy** w inpucie wartość licznika zwiększa się o 1

**Gdy** kliknę w przycisk `-`  
**Wtedy** w inpucie wartość licznika zmniejsza się o 1


## Zadania

1. Utwórz repozytorium w githubie o nazwie "js-licznik"
1. Sklonuj repozytorium na Twój komputer
1. Utwórz plik index.html (treści poniżej)
1. Utwórz plik licznik.js
1. W pliku licznik.js oprogramuj zadanie


## Czego sie nauczysz

### zmienna

Zmienna w javascript pozwala na przechowywanie wartości w _nazwie_.

Zmienną powinno się definiować poprzez napisanie słowa `let` a następnie jej nazwy.

```
let suma = 5
```

Teraz możesz coś zrobić z tą `suma`. Na przykład:

```
let suma = 5;
console.log(suma)

suma = suma + 10; // w sumie jest 15
console.log(suma)

suma -= 1; // w sumie jest 14
console.log(suma)

suma += 6; // w sumie jest 20
console.log(suma)
```

> zobaczysz także zapis: `var suma = 5` oraz samo `suma = 5`, ale nie rób tak!  
> **korzystaj z `let`**
>
> też istnieje `const`, ale to nie dziś. Po prostu wiedz, że jest.


## funkcja

Funkcja (najprościej) to jeden kontener, zbiornik, pudełko, w którym zapisujesz instrukcje.

### definiowanie funkcji

```javascript
function nazwa(){
}
```

1. słowo `function`
1. nazwa funkcji
1. nawiasy `()`
1. klamra `{`
1. zawartość funkcji (np. ten długi kod z powyższego "zmienna")
1. klamra `}`


```javascript
function przeliczSumy() {
  let suma = 5;
  console.log(suma)

  suma = suma + 10; // w sumie jest 15
  console.log(suma)

  suma -= 1; // w sumie jest 14
  console.log(suma)

  suma += 6; // w sumie jest 20
  console.log(suma)
}
```


### wywoływanie/uruchamianie funkcji

```
przeliczSumy()
```

## Klikanie w przycisk

Przeglądarka non stop Ciebie śledzi.

Wszystko co robisz - ona o tym wie.

Oraz wysyła Eventy o tym co robisz!

A to oznacza, że możemy powiedzieć przeglądarce _"Ej, ty, słuchaj no. Jak ktoś kliknie w ten przycisk, to mi o tym powiedz"_. A robi się to tak:

```javascript
document.getElementById("plus").addEventListener("click", function(){
  console.log('kliknąłeś w przycisk')
})
```

W pliku HTML są przyciski `<button` i mają one przypisany identyfikator `id`.

`document.getElementByid("plus")` znajduje element o identyfikatorze "plus".

Następnie `addEventListener("click", function..` mówi, uruchom funkcję, gdy ktoś kliknie w przycisk.

## Ustawianie wartości inputa

`<input value` możesz modyfikować atrybuty w htmlu. Dziś będziesz modyfikować atrybut `value`.

podobnie do "klikanie w przycisk", najpierw musisz znaleźć element o identyfikatorze "wynik", następnie przypisać jemu wartość.

```javascript
let suma = 87
document.getElementById("wynik").value = 777
document.getElementById("wynik").value = suma
```


---

## plik HTML

Na dziś, po prostu skopiuj i wklej. Nauszysz sie wszystkiego z czasem

```html
<head>
   <meta charset="utf-8">
   <title>Licznik</title>
</head>
<body>
   <button id="plus">+</button>
   <button id="minus">-</button>
   <input id="wynik" value="5">
   <script src="licznik.js"></script>
</body>
</html>
```

1. Materiał do nauki
   - html
     - <button>
     - <input>
     - attr "id"
   - addEventListener
   - document.getElementById
