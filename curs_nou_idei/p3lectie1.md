Algoritmii de baza care pot fi scrisi in algoritmica sunt foarte des combinati intre ei pentru a rezolva o problema mai complexa.
Sa vedem impreuna cati divizori are oglinditul unui numar dat.

```cpp
#include <iostream>
#include <cmath>
using namespace std;

long n;

long ogl(long number){
    long o = 0;
    while (number){
        o = o*10+number%10;
        number/=10;
    }
    return o;
}

long nrDiv(long number) {
    long contorDiv =1, d=2,f;
    while (number>1) {
        while (d*d<=number && number%d) d++;
        if (d*d>number) d = number;
        f = 1;
        while (number%d == 0) {f++; number/=d;}
        contorDiv*=f;
    }
    return contorDiv;
}

int main() {
    cin>>n;
    cout<<nrDiv(ogl(n));

    return 0;
}

```

Codul C++ poate separa algoritmul in 2 subalgoritmi: 
--- unul care sa calculeze oglinditul unui numar adica numarul obtinut prin inversarea cifrelor numărului și 
--- al doilea care sa calculeze numărul de divizori ai numărului inversat.

Pentru a rezolva această problemă pas cu pas, trebuie mai întâi să inversăm cifrele numărului dat `n`. 
Scriem functia de tip long `ogl` care va primi un numar de tip long si va returna oglinditul sau.
Calculul oglinditului il putem realiza extragând în mod repetat ultima cifră a lui `n` și adăugând-o la un nou număr `o` (de la oglindit), care începe de la 0. Apoi eliminăm ultima cifră din `n` efectuând o împărțire a întregului cu 10. Acest proces continuă până când `n` devine 0. Numărul rezultat o va fi versiunea inversată a lui `n`.

De exemplu, pentru `number = 123` pornim cu `o = 0`
La prima iteratie `o = o*10 + number%10 = 0 * 10 + 3 = 3` iar `number = 12`
La a doua iteratie `o = o*10 + number%10 = 3 * 10 + 2 = 32` iar `number = 1`
La a treia iteratie `o = o*10 + number%10 = 32 * 10 + 1 = 321` iar `number = 0`
Bucla se opreste si functia returneaza valoarea 321.

În continuare, trebuie să calculăm numărul de divizori ai numărului inversat `o`. Pentru a face acest lucru, folosim o abordare de factorizare in functia de tip long `nrDiv` care primeste ca parametru de intrare local in functie `long number` cu valoarea returnata de apelul functiei `ogl(n)`.
Începem prin a inițializa două variabile: 
--- `contorDiv`, care va stoca numărul total de divizori si este initial 1; 
--- `d` este inițializat la 2 și va fi folosit ca divizor în procesul de factorizare;
--- `f` este inițializat la 1 și va fi folosit pentru a număra factorii primi ai lui `number`.

Intrăm apoi într-o buclă de tip `while` care continuă atâta timp cât `number` este mai mare decât `1`. 
În interiorul buclei, folosim o altă buclă pentru a găsi cel mai mic divizor `d` al lui `number` verificând fiecare număr întreg începând de la 2. 
Dacă `d` pătrat este mai mic decât `number` și `number` este nedivizibil cu `d`, creștem `d`.
Această condiție asigură că divizorul curent `d` nu depășește rădăcina pătrată a lui `number`. Este suficient să verificăm divizorii doar până la rădăcina pătrată a unui număr pentru a găsi toți divizorii săi. Dacă nu găsim niciun divizor până la rădăcina pătrată, înseamnă că numărul este prim.

Odată ce găsim un divizor, setăm `f` la `1` și intrăm în altă buclă pentru a număra de câte ori `d` împarte `number`. De fiecare dată când `d` împarte `number`, creștem `f` și împărțim `number` cu `d`. Deci daca am gasit un divizor al lui `number` impartim cu el atat de mult cat putem si numaram fiecare pas facut.
După numărarea de câte ori `d` împarte `number`, înmulțim `contorDiv` cu `f`. Acest proces asigură că numărăm toți divizorii lui `number`.

De exemplu, daca `number = 24`. Din matematica stim ca 24 = 2^3 * 3.
Deci daca am determinat ca 24 se divide la 2, impartim de 3 ori cu 2 pentru ca atat se poate. Factorul `f` ajunge deci la 4. `contorDiv` ajunge tot 4.
Apoi determinam ca urmatorul divizor este 3. Repunem factorul `f` pe 1. 
Impartim cu 3 o singura data si de fapt ajungem la sfarsit. Factorul `f` ajunge deci la 2. In final `contorDiv = 8`.
Procesul se incheie si se returneaza valoarea gasita 8.

Functia principala a programului, `int main(){}` contine doar citirea unei valori de tip long `n` si tiparirea raspunsului dat de apelul functiei `nrDiv(ogl(n))`. 
Instrucțiunea `cout << nrDiv(ogl(n));` inversează cifrele numărului `n`și apoi calculează și afișează numărul de divizori ai numărului inversat. Acest proces combinat demonstrează cum putem utiliza funcții pentru a realiza operațiuni complexe într-un mod modular și eficient în C++.

Pentru a rezuma, această soluție implică inversarea cifrelor numărului dat n și apoi calcularea numărului de divizori ai numărului inversat. Pașii cheie includ inversarea numărului prin extragerea și adăugarea cifrelor și găsirea numărului de divizori folosind o abordare de factorizare. Prin implementarea sistematică a acestor pași, ne asigurăm că soluția este atât eficientă, cât și exactă. Rezultatul final este numărul total de divizori ai numărului inversat, oferind rezultatul dorit pentru problemă. Această metodă nu numai că garantează corectitudinea, dar respectă și constrângerile problemei, ceea ce o face o alegere robustă pentru aplicații practice.

Acest algoritm exemplifică o abordare eficientă și elegantă pentru rezolvarea unei probleme complexe prin utilizarea funcțiilor specializate. Inversarea cifrelor unui număr și calcularea numărului de divizori sunt realizate prin subalgoritmi bine definiți, ceea ce face codul ușor de înțeles și de gestionat. Această metodă modulară este esențială pentru scrierea de programe robuste și flexibile în orice limbaj de programare.
