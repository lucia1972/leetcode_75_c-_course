# Introducere in algoritmi - definitii, importanta
## Definitia algoritmului, proprietățile algoritmului, schema logica, pseudocod**

Bun venit în primul modul al cursului nostru despre algoritmi! 
Acest modul vă va introduce în lumea algoritmilor, elemente esențiale în domeniul informaticii și programării.

Definiția Algoritmului
Un **algoritm** este un set finit si binedefinit de instrucțiuni clare și neambigue, destinat să rezolve o problemă specifică. Imaginați-vă un algoritm ca pe o rețetă de gătit, care vă spune exact ce ingrediente aveți nevoie și pașii pe care trebuie să îi urmați pentru a pregăti un anumit fel de mâncare.
Algoritmii sunt coloana vertebrală a oricărui program sau sistem informatic. Fie că este vorba despre un simplu algoritm de sortare sau cautare sau despre algoritmi complexi folosiți în criptografie sau în sistemele de recomandare, capacitatea de a concepe, de a înțelege și de a implementa algoritmi este crucială pentru orice programator sau dezvoltator software.

Algoritmii sunt fundamentali și prezenți în toate aspectele tehnologiei moderne. Aceștia joacă un rol crucial în funcționarea și eficiența sistemelor informatice, de la procesarea simplă de date până la aplicațiile complexe de inteligență artificială și învățare automată. Fiecare operație efectuată pe un dispozitiv digital, fie că este vorba de o căutare pe Google, navigarea pe rețele sociale, sau utilizarea aplicațiilor de navigație, este posibilă datorită algoritmilor bine proiectați. Aceștia nu doar că optimizează performanța și viteza proceselor, dar și gestionează eficient resursele, asigurând o experiență de utilizare net superioară.

Nu orice algoritm scrii este un algoritm corect și eficient. Scrierea algoritmilor necesită o înțelegere profundă a problemei de rezolvat, precum și a resurselor disponibile și a cerințelor de performanță. Un algoritm trebuie să fie nu doar corect, adică să producă rezultatele așteptate pentru toate cazurile valide de intrare, dar și eficient din punct de vedere al consumului de timp și spațiu de memorie. Algoritmi ineficienți pot duce la întârzieri semnificative în procesare și la consum excesiv de resurse, ceea ce afectează negativ performanța generală a sistemelor informatice. Prin urmare, proiectarea algoritmilor necesită o analiză atentă, testare riguroasă și adeseori iterații multiple pentru optimizare.

Pentru a fi corect, algoritmul trebuie sa aiba:

 - `finitudine` - trebuie să se termine după un număr finit de pași.
 - `definitie` -fiecare pas al algoritmului trebuie să fie clar și precis definit.
 - `generalitate` - pentru un set de date de intrare, algoritmul sa rezolve o clasa de probleme de acelasi fel.
 - `eficienta` - raspunsul la problema dat de algoritm trebuie sa se faca intr-un timp cat mai mic si sa ocupe cat mai putina memorie.


Algoritmii pot fi descrisi prin
- schema logică - metoda grafica de descriere a algoritmilor ("desenam algoritmii");
- pseudocod - metoda descriptiva folosind o formă simplificată și structurată a unui limbaj natural amestecat cu elemente de limbaj de programare ("povestim algoritmii").

**Schema logică** cunoscută și sub numele de diagramă de flux (`flowchart`), este o reprezentare vizuală a pașilor unui algoritm.
Ea utilizează diverse simboluri standardizate pentru a indica operațiile (cum ar fi calculele matematice sau deciziile de logică), fluxul de control (direcția execuției), și procesarea datelor.
Folosirea lor faciliteaza înțelegerea interacțiunilor și dependențelor dintre diferitele operații mai ales în fazele inițiale ale proiectării unui sistem, în educație și în documentația tehnică, unde claritatea este esențială.

**Pseudocodul** este o metodă de a descrie un algoritm folosind o formă de limbaj natural amestecat cu structuri de control din limbajele de programare. Scopul este de a exprima logica algoritmului într-un format care poate fi ușor înțeles de oricine, fără a necesita cunoștințe de sintaxa specifică unui limbaj de programare.
Pseudocodul nu este destinat să fie executat pe un computer, ci să servească ca o descriere intermediară între problema formulată în limbaj natural și codul sursă complet. El folosește structuri de control cunoscute (cum ar fi if, else, while, for) pentru a exprima logica si este înțeles de programatori indiferent de limbajul de programare specific pe care îl folosesc. Pseudocodul ajută la planificarea algoritmului și la gândirea clară a soluției înainte de a începe scrierea codului efectiv, reducând astfel riscul de erori și neînțelegeri.

Exemplu de algoritm realizat in pseudocod: Interclasarea a doi vectori

```pseudo
ALGORITM INTERCLASARE VECTORI (r,lr,q,lq)
    //adaugam elemente de garda la finalul vectorilor
    r[lr+1] = q[lq] + 1;
    q[lq+1] = r[lr] + 1;

//initializare contoare
    i = 1; j=1; k=1;

// parcurgerea vectorilor până când toate elementele din ambele vectori sunt adăugate în vectorul result
    PENTRU k de la 1 la (lr + lq) EXECUTĂ
        // Compară elementele curente din fiecare vector și alege cel mai mic
        DACA r[i] < q[j] ATUNCI
            result[k] = r[i]
            i = i + 1
        ALTFEL
            result[k] = q[j]
            j = j + 1
        SFÂRȘIT DACA
    SFÂRȘIT PENTRU
```
(explicatii la bucla for din algoritm)
Daca elementul curent din primul vector parcurs cu contorul `i` este mai mic decat elementul curent din vectorul secund parcurs cu `j`, (`r[i] < q[j]>`) atunci se ia elementul din vectorul `r` si se aseaza in `result` si se incrementeaza `i`. Altfel se ia elementul din vectorul `q` si se incrementeaza `j`. Deci se ia intotdeaua cel mai mic dintre elemente si se incrementeaza contorul corespunzator vectorului care a donat element in `result`.

În concluzie această lecție a explorat ce sunt algoritmii, de ce sunt importanți, proprietățile pe care trebuie să le aibă, și am văzut cum putem folosi schema logică și pseudocodul pentru a planifica și a descrie algoritmi. În următoarea lecție, vom discuta despre cum să rezolvăm probleme folosind structuri de date și subprograme.

Vă mulțumesc pentru atenție și ne vedem în continuare!