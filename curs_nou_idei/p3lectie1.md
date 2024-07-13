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
Deci daca am determinat ca 24 se divide la 2, impartim de 3 ori cu 2 pentru ca atat se poate.
Apoi determinam ca urmatorul divizor este 3. Impartim si cu el si de fapt ajungem la sfarsit.
Deci am realizat 3 impartiri cu 2 

În cele din urmă, după ieșirea din bucle, r va conține numărul total de divizori ai lui o. Apoi scoatem această valoare.


Pentru a rezuma, această soluție implică inversarea cifrelor numărului dat n și apoi calcularea numărului de divizori ai numărului inversat. Pașii cheie includ inversarea numărului prin extragerea și adăugarea cifrelor și găsirea numărului de divizori folosind o abordare de factorizare. Prin implementarea sistematică a acestor pași, ne asigurăm că soluția este atât eficientă, cât și exactă. Rezultatul final este numărul total de divizori ai numărului inversat, oferind rezultatul dorit pentru problemă. Această metodă nu numai că garantează corectitudinea, dar respectă și constrângerile problemei, ceea ce o face o alegere robustă pentru aplicații practice.

Structura generală a codului
Codul include două biblioteci standard C++:

#include <iostream>: pentru operațiuni de intrare și ieșire.
#include <cmath>: pentru operațiuni matematice (chiar dacă nu este utilizată în mod direct în codul furnizat).
Programul definește următoarele componente:

Variabila globală long n pentru a stoca numărul citit de la utilizator.
Funcția ogl(long n) pentru a inversa cifrele unui număr.
Funcția nrDiv(long n) pentru a calcula numărul de divizori ai unui număr.
Funcția main() pentru a citi un număr, a inversa cifrele acestuia și a calcula numărul de divizori ai numărului inversat.
Funcția ogl(long n)
Funcția ogl are rolul de a inversa cifrele unui număr n. Iată cum funcționează aceasta:

cpp
Copy code
long ogl(long n) {
    long o = 0;
    while (n) {
        o = o * 10 + n % 10;
        n /= 10;
    }
    return o;
}
Inițializare: Se declară o variabilă o inițializată la 0. Aceasta va stoca numărul inversat.
Bucla while: Atâta timp cât n nu este zero:
o = o * 10 + n % 10; Adaugă ultima cifră a lui n la o.
n /= 10; Elimină ultima cifră a lui n.
Returnare: Funcția returnează numărul o, care conține cifrele lui n în ordine inversă.
Funcția nrDiv(long n)
Funcția nrDiv calculează numărul de divizori ai unui număr n. Aceasta este mai complexă și implică factorii primi ai numărului. Iată cum funcționează:

cpp
Copy code
long nrDiv(long n) {
    long r = 1, d = 2, f;
    while (n > 1) {
        while (d * d <= n && n % d) d++;
        if (d * d > n) d = n;
        f = 1;
        while (n % d == 0) { f++; n /= d; }
        r *= f;
    }
    return r;
}
Inițializare: Se declară variabilele r (numărul de divizori) inițializată la 1, d (divizorul curent) inițializată la 2, și f (numărul de factori curenți) fără inițializare.
Bucla exterioară while (n > 1): Continuă cât timp n este mai mare decât 1.
Bucla interioară while (d * d <= n && n % d): Crește d până găsește un divizor al lui n sau până când d pătratul său depășește n.
Verificare și actualizare d: Dacă d nu divide n, atunci d devine n.
Factorizare: Inițializează f la 1. Cât timp d divide n, incrementează f și împarte n la d.
Actualizare r: Multiplică r cu f pentru a actualiza numărul total de divizori.
Returnare: Funcția returnează r, care conține numărul de divizori ai lui n.
Funcția main()
Funcția principală main citește un număr, inversează cifrele acestuia și afișează numărul de divizori ai numărului inversat:

cpp
Copy code
int main() {
    cin >> n;
    cout << nrDiv(ogl(n));
    return 0;
}
Citire: Utilizatorul introduce un număr n.
Inversare și calcul divizori: Funcția ogl(n) inversează cifrele lui n, iar nrDiv calculează numărul de divizori ai numărului inversat.
Afișare: Rezultatul este afișat pe ecran.
Analiza detaliată
Inversarea cifrelor:

Procesul de inversare a cifrelor unui număr este util în multe probleme de programare și algoritmică. În acest caz, este un pas intermediar necesar pentru calcularea numărului de divizori ai numărului inversat.
Calculul numărului de divizori:

Calcularea numărului de divizori implică determinarea factorilor primi ai numărului. Aceasta este o metodă eficientă pentru a găsi toți divizorii unui număr. Este utilă în probleme de teorie a numerelor și criptografie.
Complexitate:

Inversarea cifrelor: Operația de inversare are o complexitate de 
𝑂
(
log
⁡
10
𝑛
)
O(log 
10
​
 n), deoarece numărul de cifre este proporțional cu logaritmul numărului în baza 10.
Calculul divizorilor: Factorizarea unui număr are o complexitate aproximativă de 
𝑂
(
𝑛
)
O( 
n
​
 ), deoarece verificăm divizorii până la rădăcina pătrată a numărului.
Exemple de rulare
Pentru a înțelege mai bine funcționarea programului, să considerăm câteva exemple:

Exemplu 1:

Input: 123
Inversare: 321
Divizori: 1, 3, 107, 321 (4 divizori)
Output: 4
Exemplu 2:

Input: 456
Inversare: 654
Divizori: 1, 2, 3, 6, 109, 218, 327, 654 (8 divizori)
Output: 8
Concluzie
Acest program demonstrează cum se pot combina mai multe tehnici algoritmice pentru a rezolva o problemă complexă. Prin divizarea problemei în subprobleme mai mici și folosirea funcțiilor, codul devine mai clar și mai ușor de întreținut. Funcțiile ogl și nrDiv ilustrează modul în care operațiile de bază pot fi combinate pentru a realiza sarcini mai complexe, iar structura modulară permite reutilizarea și testarea independentă a fiecărei componente. Aceasta este o abordare esențială în dezvoltarea de software eficient și robust.