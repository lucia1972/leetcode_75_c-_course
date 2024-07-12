Pentru a intelege mai bine si a explica punctual conceptele prezentate in filmele anterioare, voi lua cateva exemple si le voi rezolva complet.

Unul dintre cei mai cunoscuti algoritmi extrem de simpli si importanti este `algoritmul de numar par`.
Trebuie deci sa determin daca un numar dar este `par` sau `impar`.

Conform definitiei un numar dat este `par` daca restul impartirii lui la 2 este 0. Daca restul impartirii numarului la 2 este 1, numarul este `impar`.

Pentru a implementa acest algoritm am nevoie de o operatie matematica de baza: operatia de impartire si apoi retinerea restului din aceasta operatie.
Voi folosi operatorul `%` pentru a determina acest lucru.
De exemplu: `5 % 2 = 1` sau `6 % 2 = 0`.

Algoritmul va citi de la tastatura un numar intreg in variabila n si va afisa pe ecran unul dintre mesajele ` este par` sau ` este impar` precedat de valoarea numerica citita.
In mod clasic, voi folosi instructiunea de decizie `if(conditie){set_operatii1;}else{set_operatii2;}` care executa `set_operatii1` daca `conditie` este `true` sau executa `set_operatii2`, daca `conditie` este `false`.



```cpp

#include <iostream>
using namespace std;

int main(){
    int n;
    cin>>n;

    if(n % 2 ==0){
        cout<<n<<" este par";
    }else{
        cout<<n<<" este impar";
    }

    return 0;
}

```
Testez programul meu pentru `n = 6` si apoi pentru `n = 11`.

Daca doresc sa scriu codul mai concis, pot folosi pperatorul ternar `? :`. Acesta va decide ce mesaj să fie afișat:

- `n % 2 == 0` verifică dacă `n` este divizibil cu `2`.
- Dacă `n % 2 == 0` este `true`, afișează `este par`.
- Dacă n % 2 == 0 este `false`, afișează `este impar`.

```cpp

#include <iostream>
using namespace std;

int main(){
    int n;
    cin>>n;
    cout<< n << (n % 2 ==0 ? " este par" : " este impar");

    return 0;
}

```

