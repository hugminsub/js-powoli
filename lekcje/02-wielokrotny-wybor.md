# Lekcja druga - test wielokrotnego wyboru

Poprzednio wyświetlałeś w inpucie wartość, która jest przechowwyana w zmiennej `suma`.

Robiłeś to poprzez `...ById("wynik").value = suma`

atrybut `value` przyjmuje wartość, ale też ją zwraca:

### Spróbuj!

otwórz wczorajszy plik index.html w przeglądarce, a w konsoli wpisz:

`console.log(document.getElementById("wynik").value)`

następnie wpisz coś do inputa i raz jeszcze w konsoli wyświetl wartość.


## Zadanie na dziś: Test wielokrotnego wyboru

Jako uczeń, który ma otwarty plik index.html, chcę móc udzielić odpowiedzi na pytanie wpisująć "A, B, C, albo D" i klikając przycisk "sprawdź odpowiedź" dowiedzieć się, czy prawidłowo wpisałem odpowiedź.

**Gdy** w input wpiszę odpowiedź prawidłową  
**Oraz** przycisnę przycisk "sprawdź odpowiedź"  
**Wtedy** zobaczę alert z informacją "dobrze!"

**Gdy** w input wpiszę odpowiedź **nie**prawidłową  
**Oraz** przycisnę przycisk "sprawdź odpowiedź"  
**Wtedy** zobaczę alert z informacją "spróbuj jeszcze raz."

**Krytiera akceptacji:**

1. W input mogę wpisać literę wielką lub małą,
1. Skrypt musi umieć rozpoznawać zarówno małe jak i wielkie litery (`ABCDabcd`)
1. Rezultatem są 2 pliki: index.html oraz test.js
1. Skrypty są wgrane do repozytorium o nazwie "js-wielokrotny-wybor"
1. Znajdź odpowiedź do pytania i oprogramuj odpowiednio

**Treść i wygląd zadania**

```
Lektura Lalka: Kim jest Wokulski?

a) niepoprawnym romantykiem
b) typowym pozytywistą
c) ma cehy romantyka i pozytywisty
d) realistą

odpowiedź: [_________] <sprawdź odpowiedź>
```

**Przydatne wskazówki**

- `<button`
- `<input`
- `console.log("MAŁE LITERY".toLowerCase())`
- `if ("słowo" == "nie pasuje") { alert("takie same")} else {alert("różnią się")}`
