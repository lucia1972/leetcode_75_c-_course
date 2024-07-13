O alta problema foarte des intalnita in interviurile din industria IT este problema **FizzBuzz**.
Este o problema simpla, dar in cele mai multe cazuri problemele simple ridica mai multe probleme.

FizzBuzz poate fi enuntata astfel:

Se da un `n` numar intreg. Sa se afiseze numerele de la `1 - n` in urmatorul fel:
--- Numerele multiplu de 3 trebuie inlocuite cu textul `Fizz`.
--- Numerele multiplu de 5 trebuie inlocuite cu textul `Buzz`.
--- Numerele multiplu de 3 si 5 trebuie inlocuite cu textul `FizzBuzz`.

Pare un algoritm simplu care ar trebui sa afiseze la rulare un sir de genul:

1, 2, Fizz, 4, Buzz, Fizz, 7, 8, Fizz, Buzz, 11, Fizz, 13, 14, FizzBuzz ...


```cpp

#include <iostream>

using namespace std;

void fizzBuzz(int number) {
    for(int i = 1; i <= number; i++) {
        if(i % 3 == 0 && i % 5 == 0) {
            cout << "FizzBuzz" << " ";
        }
        else if(i % 3 == 0) {
            cout << "Fizz" << " ";
        }
        else if(i % 5 == 0) {
            cout << "Buzz" << " ";
        }
        else {
            cout << i << " ";
        }
    }
}

int main() {
    int n;
    cin>>n;
    fizzBuzz(n);

    return 0;
}
```

Pentru un numar dat `n` pe care l-am citit in programul principal, apelez functia `fizzBuzz(n)` care va realiza de fapt intregul sir de modificari pe care le cere cerinta problemei.
Funcția `fizzBuzz` scrisa primește un parametru întreg local `number` și nu returnează nimic `void`. Intr-o bucla repetitiva `for` iterează de la 1 la `number` și aplică regulile din cerinta:
--- Dacă `i` este divizibil atât cu 3 cât și cu 5 `i % 3 == 0 && i % 5 == 0` afișează `FizzBuzz`.
--- Dacă `i` este divizibil doar cu 3 `i % 3 == 0` afișează `Fizz`.
--- Dacă `i` este divizibil doar cu 5 `i % 5 == 0` afișează `Buzz`.
--- Dacă `i` nu este divizibil nici cu 3, nici cu 5, se va afisa valoarea lui `i`.
Rezultatele sunt afișate pe aceeași linie, separate de un spațiu `" "`.

Algoritmul a fost implementat simplu, fara a folosi structuri de date de tip vector.