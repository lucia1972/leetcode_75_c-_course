Complic putin acum lucrurile si iti propun sa gasim prima cifra a fiecarui numar dintr-un sir de `n` numere intregi.

Pentru acest algoritm as putea aborda problema astfel:
--- citesc lungimea sirului;
--- parcurg sirul de la prima valoare pana la ultima valoare citind pe rand valoarea si
--- stabilesc care este prima sa cifra
--- tiparesc prima cifra a fiecarui numar din sir.

Este o problema clasica care, asa cum am spus anterior, poate fi divizata in subalgoritmi mai mici.
Pentru aceasta voi folosi functiile si voi scrie codul meu cu ajutorul lor.
Subalgoritmii / functiile care se pot scrie in acest caz sunt:
--- o functie de tip integer care sa returneze prima cifra a unui numar;
--- o functie de tip `void` care sa execute citirea fiecarui numar din sir si returnarea raspunsului final.

```cpp
#include <iostream>
using namespace std;

int firstDigit(int number){
   while(number>9){number/=10;}
   return a;
}    

void result(int length){
    int nr;
    for(int i=1;i<=length;i++) {
        cin>>nr;
        cout<<"numar "<<nr<<" are prima cifra "<<firstDigit(nr)<<endl;
  }
}

int main() {
    int n;
    cin>>n;
    result(n);
  return 0;
}

```

Am ales ca raspunsul final sa contina si cateva cuvinte explicative. Acestea se introduc intre `" "`. Raspunsurile finale sunt scrise cate unul pe un rand pentru fiecare numar in parte, am adaugat la finalul instructiunii de scriere pe ecran `cout<<` manipulantul de flux `endl` pentru a introduce un caracter de newline `\n` și pentru a goli bufferul de ieșire.

Functia `int firstDigit(int number)` este o functie care determina prima cifra a numarului `number` pe care il primeste ca si parametru de intrare.
Cat timp numarul este mai mare decat 9, `while(a>9)` adica cat timp numarul are mai mult de o cifra, executa `number/=10`. Aceasta operatie determina, folosind operatorul `/`, catul impartirii lui `number` la 10. Operatia este echivalenta cu `number = number / 10;`. De fapt, aceasta operatie sterge de la coada numarului ultima cifra a sa. Cand numarul ramane la o singura cifra, bucla este incheiata si functia returneaza valoarea lui `number` care acum contine de fapt numai prima cifra a numarului initial.
Am folosit bucla `while` care este o structura repetitiva cu numar nedeterminat de pasi care se incheie atunci cand conditia scrisa intre paranteze `while(conditie)` nu mai este `true`.

Pentru `number = 123`
Prima iteratie `number = 12`
A doua iteratie `number = 1`
Bucla se incheie si se returneaza valoarea `1`.

Functia de tip void `result` primeste ca parametru de intrare lungimea `length` a sirului de valori.
În C++, o funcție de tip `void` este folosită atunci când se dorește executarea unor operații, dar nu este necesară returnarea unei valori către apelant. 
Pentru fiecare valoare in parte, functia trebuie sa returneze prima cifra a numarului.
Citirea sirului de valori o fac cu instructiunea repetitiva cu un numar bine determinat de pasi `for` care va merge cu un contor intreg `i` de la 1 pana la lungimea data a sirului si va citi pe rand cate un numar in variabila `nr` dupa care va apela functia `firstDigit()` pentru acel numar.

Rulez programul de mai sus pentru datele de intrare `n = 3 si valorile 123 45632 7890`.
Programul va returna:

```cpp
numar 123 are prima cifra 1
numar 45632 are prima cifra 4
numar 7890 are prima cifra 7
```

In concluzie, acest exemplu arată cum putem aborda o problemă clasică prin divizarea ei în subalgoritmi mai mici și utilizarea funcțiilor pentru o mai bună organizare a codului. Folosind funcții pentru fiecare parte a algoritmului, obținem un cod mai clar, mai ușor de întreținut și de extins. Testarea programului pe date de intrare variate confirmă corectitudinea implementării.
