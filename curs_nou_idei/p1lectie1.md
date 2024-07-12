Pentru a intelege mai bine si a explica punctual conceptele prezentate in filmele anterioare, voi lua cateva exemple si le voi rezolva complet.

Pentru a practica si tu codul explicat de mine in acest curs poti folosi orice IDE ai la indemana. Iată câteva dintre cele mai populare:

- `Visual Studio Code`: Un IDE dezvoltat de Microsoft, foarte popular pentru dezvoltarea aplicațiilor C++.
- `CLion`: Un IDE dezvoltat de JetBrains, cunoscut pentru suportul său excelent pentru CMake și proiectele C++.
- `Code::Blocks`: Un IDE gratuit și open-source, configurabil și extensibil, potrivit pentru dezvoltarea C++.
- `Eclipse CDT`: O extensie a IDE-ului Eclipse pentru dezvoltarea C/C++.
- `Xcode`: IDE-ul dezvoltat de Apple, utilizat pentru dezvoltarea aplicațiilor pe macOS și iOS, include suport pentru C++.
Eu voi folosi Visual Studio Code in prezentarile codului C++ pentru ca este un IDE universal, free si foarte usor de utilizat.

Unul dintre cei mai cunoscuti algoritmi extrem de simpli si importanti este `algoritmul de numar par`.
Trebuie deci sa determin daca un numar dar este `par` sau `impar`.

Conform definitiei un numar dat este `par` daca restul impartirii lui la 2 este 0. Daca restul impartirii numarului la 2 este 1, numarul este `impar`.

Pentru a implementa acest algoritm am nevoie de o operatie matematica de baza: operatia de impartire si apoi retinerea restului din aceasta operatie.
Voi folosi operatorul `%` pentru a determina acest lucru.
De exemplu: `5 % 2 = 1` sau `6 % 2 = 0`.

Algoritmul va citi de la tastatura un numar intreg in variabila intreaga `n` si va afisa pe ecran unul dintre mesajele ` este par` sau ` este impar` precedat de valoarea numerica citita.
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

Codul meu C++ are cateva componente importante pe care le voi avea in toate programele pe care le voi prezenta de-a lungul cursului.

Apelez la acest mod de a introduce noțiunile pentru că, dacă încerci să implementezi alături de mine codul, pe lângă faptul că reușești să elimini mult mai repede greșelile de scriere, capacitatea ta de înțelegere a codului crește.

Deci, prima linie a programului este: `#include <iostream>`. Deoarece aceasta linie începe cu simbolul `#` ea se numește "directivă de preprocesare". Înainte de a fi compilat programul, are loc preprocesarea adică se citesc liniile care încep cu simbolul `#` și se configurează programul.

După simbolul `#` urmează cuvântul `include` care indică faptul că se va include un fișier header numit `<iostream></iostream>` . 

`Iostream` este un fișier de *tip antet* care permite programului C++ să facă operații de bază: 

- citirea datelor de intrare,
- tipărirea datelor de ieșire,
- funcție de afișare a unui caracter pe o linie nouă,
- funcție de afișare a mesajelor de eroare standard pe fluxul standard de ieșire a datelor
- operații matematice de bază etc.

Acestea sunt doar câteva exemple de funcții de bază incluse în `<iostream>` dar putem găsi multe alte funcții cu care putem manipula fluxurile de intrare și de ieșire a datelor în C++.

Următoarea linie din programul de mai sus este: `using namespace std`. Se introduce astfel un spațiu de nume standard cu numele `std`. Spațiile de nume sunt folosite pentru a crea și organiza entitățile programului care trebuie să aibă un nume în C++. În acest caz, programul nostru va avea acces la nume de entități care fac parte din spațiul `std`.

Un program C++ poate conține mai multe astfel de spații de nume. 

În rândul imediat următor găsim `int main(){}`. Acest lucru indică antetul funcției care poartă numele `main` și care va returna o valoare de tip întreg (specificat de cuvântul `int` de la începutul instrucțiunii) când încheie execuția programului. Este o funcție unică într-un program C++. Există o mulțime de alte funcții pe care le putem adăuga în program, dar nici una nu se va numi `main`.

În C++ fiecare acoladă sau paranteză care se deschide trebuie să aibă o acoladă corespondentă care se închide. 

C++ este un limbaj de programare `case-sensitive` ceea ce înseamnă că el este sensibil la majuscule. Deci cuvântul `Main` sau `main` nu însemnă același lucru. Atenție deci și la acest detaliu!

In interiorul simbolurilor `{}` din `int main(){}` voi introduce corpul programului.

!!! Fiecare linie din interiorul programului se termină cu caracterul `;`. **Acesta este obligatoriu.** El marchează finalul unei propoziții sau a unei declarații.

Incep cu declararea datelor de intrare. Variabila `int n` este o variabila de tip intreg care va retine numarul dat.
Variabila de intrare trebuie citita de la tastatura `cin>>n` - instructiunea de citire a datelor in C++.

Folosind instructiunea de decizie, algoritmul stabileste care este raspunsul pe care il va returna, calculand restul impartirii numarului dat la 2 `n%2` si verificand daca acesta are valoarea `0` sau `1`.
Returnarea raspunsului se face pe ecran, simplu si clasic, cu ajutorul instructiunii de scriere `cout<<n<<"mesaj";`.

Înainte de acolada care marchează închiderea funcției `int main(){}`, apare încă o linie: `return 0;` care trimite o valoare întreagă nulă înapoi la sistemul de operare pentru a  semnaliza faptul că execuția programului s-a încheiat cu succes. 

Daca doresc sa scriu codul mai concis, pot folosi operatorul ternar `? :`. Acesta va decide ce mesaj să fie afișat:

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

În concluzie, această lecție te-a ghidat prin procesul de abordare a unei probleme de programare, folosind structuri de date și subprograme. Am discutat importanța algoritmilor, am prezentat cum să identifici și să descrii soluțiile, și am demonstrat implementarea unui algoritm simplu pentru a verifica dacă un număr este par sau impar. Practicarea acestor concepte folosind diverse IDE-uri, precum `Visual Studio Code`, `CLion`, `Code::Blocks`, `Eclipse CDT` și `Xcode`, îți va îmbunătăți abilitățile de programare și înțelegerea algoritmilor.