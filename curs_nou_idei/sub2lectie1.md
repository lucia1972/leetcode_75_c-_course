# Introducere in algoritmi - definitii, importanta
## Care sunt pasii pentru implementarea unei solutii algoritmice, structuri de date, subprograme

### Pașii pentru implementarea unei soluții algoritmice
Atunci când ne propunem să construim programe pentru calculator, imaginația și creativitatea noastră joacă un rol foarte important. Totuși, putem să ne gândim la rețete care să ne permită să fim organizați în drumul spre succes. O astfel de rețetă vă propun în cele ce urmează, pentru a găsi în mod organizat soluțiile pe care le căutăm.

Cum abordăm o problemă:

**Ce se dă? Ce se cere?**
Mai întâi, pornind de la enunțul problemei, identificăm care sunt datele de intrare și ieșire. În cazul problemelor cu enunț clar, acest pas este simplu. În situații reale, enunțul poate fi ambiguu, iar inginerii software trebuie să identifice datele de intrare și rezultatele dorite de client.

**Cum am putea rezolva problema?**
După ce avem datele, trebuie să identificăm metoda de rezolvare. Indiferent de complexitate, trebuie să rezolvăm problema înainte de a instrui computerul să urmeze pașii de rezolvare.

**Cum descriem soluția identificată?****
Algoritmii pot fi descriși folosind scheme logice (reprezentări vizuale) sau pseudocod (reprezentări textuale). Calculatoarele execută rapid o succesiune de instrucțiuni, dar nu pot realiza inferențe sau lua decizii bazate pe intuiție ca oamenii.

**Translatarea în limbaj de programare**
Acesta este primul pas care implică computerul. Vom scrie instrucțiuni pe care computerul le poate executa.

**Verificarea corectitudinii**
După ce avem codul executabil, verificăm dacă rezultatele sunt cele așteptate. În cazul unei erori, revenim la pașii anteriori pentru a corecta greșelile.

### Structuri de date
Programarea structurată utilizează mai multe tipuri de structuri pentru a organiza și scrie codul, fiind cunoscută și ca `descompunere procedurală`. Aceasta include următoarele structuri esențiale:

**Structuri liniare**: Acestea reprezintă instrucțiuni executate secvențial, una după alta, asigurând un flux simplu și direct al programului.

**Structuri de decizie sau alternative**: Aceste structuri condiționale permit programului să aleagă între diferite căi de execuție, bazate pe evaluarea unor condiții (de exemplu, `if-else`).

**Structuri repetitive**: Aceste bucle sau iterații permit repetarea unui set de instrucțiuni până când o anumită condiție este îndeplinită (de exemplu, `for`, `while`).

**Funcții**: Acestea sunt apeluri de subrutine structurate care permit reutilizarea codului. Funcțiile ajută la împărțirea programului în module mai mici, fiecare având o sarcină specifică. Acestea îmbunătățesc modularitatea, lizibilitatea și întreținerea programului, facilitând și testarea individuală a componentelor.
Utilizarea acestor structuri ajută la crearea de programe mai clare, eficiente și ușor de întreținut, reducând complexitatea și promovând o abordare organizată a dezvoltării software.

**Teorema Bohm-Jacopini** (1966) este importantă pentru programarea structurată, stabilind setul minim de instrucțiuni necesare pentru implementarea corectă a structurilor de bază ale algoritmilor:

**Atribuire**
**Decizie completă (structura alternativă cu două ramuri)**
**Structura repetitivă cu test inițial (CÂT_TIMP/WHILE)**

Importanța teoretică a acestei teoreme este aceea de a oferi niște linii directoare generale pentru proiectarea unor noi limbaje sau strategii de programare deoarece limbajele de programare tind să se echipeze cu mai multe instrucțiuni decât au nevoie pentru a-și atinge scopurile algoritmului.

### Subprograme
Subprogramele, cunoscute și ca `funcții` sau `proceduri`, sunt componente esențiale în programarea structurată. Ele permit divizarea programului în unități mai mici și reutilizabile, facilitând gestionarea complexității și îmbunătățirea lizibilității codului.

Avantajele folosirii subprogramelor:

**Reutilizabilitate**: Codul poate fi folosit în diferite părți ale programului fără a fi rescris.

**Modularitate**: Programele sunt împărțite în module mai mici, ușurând înțelegerea și întreținerea lor.

**Îmbunătățirea structurii**: Subprogramele ajută la organizarea codului într-un mod logic și structurat.

**Izolarea erorilor**: Erorile pot fi localizate și corectate mai ușor într-un subprogram decât într-un program mare și complex.

Pentru a crea subprograme eficiente, mai întâi identific exact sarcinile care pot fi izolate. Apoi stabilesc parametrii de intrare și ieșire și scriu corpul subprogramului. În pasul următor, integrez subprogramul în codul principal unde este necesar. După aceea, verific corectitudinea subprogramului atât separat, cât și în contextul programului principal. Respectând principiile programării structurate și utilizând subprograme, pot construi programe clare, eficiente și ușor de întreținut.


