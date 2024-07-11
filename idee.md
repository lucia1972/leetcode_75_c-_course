Data Structures & Algorithms in C++

1. Introducere în C++ și Algoritmi
1.1. Fundamentele C++: Variabile, tipuri de date, pointeri, referințe
    1.1.1. Input și Output: Utilizarea bibliotecii standard de I/O în C++ (iostream) și cum se realizează citirea de la tastatură și scrierea pe ecran.

    
    1.1.2. Variabile și Tipuri de Date: 
            Introducere în tipurile de date fundamentale (int, float, double, char), variabile și cum se declară și se utilizează acestea în C++. 
            Discuție despre specificitatea C++ cum ar fi tipurile de date extendate (long, long long)

            Exerciții de pe LeetCode
                1. Two Sum (LeetCode Problem 1)

                Descriere: Se dă un array de numere întregi și un număr țintă, returnează indicii celor două numere astfel încât acestea să adune la țintă.
                Relevanță: Acest exercițiu te ajută să înțelegi utilizarea array-urilor și manipularea tipurilor de date întregi.
                Link: Two Sum - LeetCode
                
                2. Reverse Integer (LeetCode Problem 7)

                Descriere: Se dă un număr întreg, inversează cifrele acestui număr.
                Relevanță: Îți permite să practici cu operații pe tipuri de date întregi și să te gândești la manipularea overflow-ului și underflow-ului.
                Link: Reverse Integer - LeetCode
                
                3. Valid Palindrome (LeetCode Problem 125)

                Descriere: Se dă un șir de caractere, determină dacă acesta este un palindrom, considerând doar caracterele alfanumerice și ignorând cazurile.
                Relevanță: Exercițiul te învață să manipulezi stringuri și să te ocupi de conversii de tip de date și condiții.
                Link: Valid Palindrome - LeetCode
            
            Exerciții de pe Pbinfo
                1. Suma cifrelor (Pbinfo Problem 1)

                Descriere: Se dă un număr natural n. Să se determine suma cifrelor acestui număr.
                Relevanță: Îți dezvoltă abilitățile de a lucra cu bucle și operații pe cifrele unui număr, folosind tipuri de date întregi.
                Link: Suma cifrelor - Pbinfo
                
                2. Cifra de control (Pbinfo Problem 246)

                Descriere: Se dă un număr n. Să se determine cifra de control a acestuia.
                Relevanță: Ajută la înțelegerea procesării numerelor și utilizarea buclelor pentru a reduce un număr la o singură cifră.
                Link: Cifra de control - Pbinfo
                
                3. Număr palindrom (Pbinfo Problem 497)

                Descriere: Verificați dacă un număr natural n dat este palindrom (se citește la fel de la stânga la dreapta și de la dreapta la stânga).
                Relevanță: Folosește conversii între tipuri de date și operații pe cifre pentru a determina dacă un număr este palindrom.
                Link: Număr palindrom - Pbinfo


    1.1.3. Pointeri și Referințe: 
            Explicarea conceptului de pointeri și referințe, două dintre cele mai puternice unelte în C++ care permit manipularea memoriei și a adreselor de memorie. 
            Exemplificarea utilizării pointerilor pentru a accesa și modifica valori stocate în memorie, și diferența dintre pointeri și referințe.

            Exerciții de pe LeetCode
                1. Reverse Linked List (LeetCode Problem 206)

                Descriere: Se dă capul unei liste înlănțuite, inversează lista și returnează noul cap.
                Relevanță: Acest exercițiu este ideal pentru a practica manipularea pointerilor pentru a modifica legăturile dintre nodurile unei liste.
                Link: Reverse Linked List - LeetCode
                
                2. Remove Nth Node From End of List (LeetCode Problem 19)

                Descriere: Se dă capul unei liste înlănțuite și un număr n. Elimină al n-lea nod de la sfârșitul listei și returnează capul listei modificate.
                Relevanță: Utilizează pointeri pentru a parcurge lista și a modifica legăturile într-o singură trecere.
                Link: Remove Nth Node From End of List - LeetCode
                
                3. Swap Nodes in Pairs (LeetCode Problem 24)

                Descriere: Se dă capul unei liste înlănțuite, schimbă între ele nodurile în perechi.
                Relevanță: Această problemă îți testează capacitatea de a folosi pointerii pentru a reorganiza legăturile între noduri într-un mod mai complex.
                Link: Swap Nodes in Pairs - LeetCode
            
            Exerciții de pe Pbinfo
                1. Adunare numere mari (Pbinfo Problem 2544)

                Descriere: Realizați un program care să adune două numere mari, memorate în liste înlănțuite.
                Relevanță: Exercițiul necesită manipularea listelor înlănțuite folosind pointeri pentru a aduna cifrele numerelor stocate.
                Link: Adunare numere mari - Pbinfo
                
                2.Ștergerea unui element din listă (Pbinfo Problem 149)

                Descriere: Se dă o listă înlănțuită și un număr. Ștergeți toate aparițiile acestui număr din listă.
                Relevanță: Aceasta problemă îți va dezvolta abilitățile de a folosi pointerii pentru a elimina elemente dintr-o structură de date înlănțuită.
                Link: Ștergerea unui element din listă - Pbinfo
                
                3. Copiere liste (Pbinfo Problem 512)

                Descriere: Se dă o listă înlănțuită. Realizați o copie exactă a acesteia.
                Relevanță: Îți permite să practici utilizarea pointerilor pentru a crea o copie exactă a unei liste înlănțuite, gestionând corect alocațiile de memorie.
                Link: Copiere liste - Pbinfo

    1.1.4. Structuri de Control: 
            Prezentarea instrucțiunilor de control de flux (if, switch, for, while, do-while) și cum acestea sunt utilizate în C++ pentru a dirija executia codului.

            Exerciții de pe LeetCode
                1. Fizz Buzz (LeetCode Problem 412)

                Descriere: Scrie un program care afișează numerele de la 1 la n. Pentru multiplii de trei afișează „Fizz” în loc de număr și pentru multiplii de cinci afișează „Buzz”. Pentru numere care sunt multipli de amândoi trei și cinci afișează „FizzBuzz”.
                Relevanță: Acest exercițiu utilizează structurile if și for pentru a implementa o logică condițională simplă și repetitivă.
                Link: Fizz Buzz - LeetCode
                
               2. Valid Parentheses (LeetCode Problem 20)

                Descriere: Dat fiind un șir care conține doar caracterele '(', ')', '{', '}', '[' și ']', determină dacă șirul de intrare este valid.
                Relevanță: Folosește structuri de control precum for și if pentru a verifica și gestiona condiții complexe.
                Link: Valid Parentheses - LeetCode
                
                3. Climbing Stairs (LeetCode Problem 70)

                Descriere: Trebuie să urci o scară care are n trepte. Poți face fie un pas de o treaptă, fie de două trepte. Câte moduri unice există de a ajunge în vârf?
                Relevanță: Deși problema este clasică pentru recursivitate și programare dinamică, implementarea ei necesită înțelegerea și utilizarea buclelor for sau while.
                Link: Climbing Stairs - LeetCode
                
            Exerciții de pe Pbinfo
                1. Număr Pătrat Perfect (Pbinfo Problem 100)

                Descriere: Se dă un număr n. Să se determine dacă n este pătrat perfect.
                Relevanță: Utilizează bucla for sau while pentru a verifica dacă un număr este pătrat perfect.
                Link: Număr Pătrat Perfect - Pbinfo
                
                2. Divizori (Pbinfo Problem 4)

                Descriere: Se dă un număr natural n. Să se afișeze toți divizorii acestuia.
                Relevanță: Perfect pentru practicarea buclelor for în combinatie cu instrucțiunile condiționale if pentru a identifica divizorii unui număr.
                Link: Divizori - Pbinfo
                
                3. Suma Divizorilor (Pbinfo Problem 330)

                Descriere: Se dă un număr n. Să se calculeze suma divizorilor lui n.
                Relevanță: O altă ocazie excelentă de a folosi for și if pentru a acumula suma sub anumite condiții.
                Link: Suma Divizorilor - Pbinfo


    





Introducere în algoritmi: Definiții, importanță, aplicații
    Definiții și Importanță: 
        Ce sunt algoritmii, de ce sunt importanți în programare și în rezolvarea problemelor. 
        Discuții despre cum algoritmii eficienți pot îmbunătăți performanța aplicațiilor.
    

    Aplicații ale Algoritmilor: 
        Exemple de aplicatii reale ale algoritmilor în software engineering, știința datelor, inteligență artificială, etc.


Analiza complexității: Big O, Big Theta, Big Omega
    Ce Este Analiza Complexității: 
        Introducere în conceptul de analiză a complexității algoritmilor și de ce este crucială în alegerea soluției optime.


    Notații Big O, Big Theta, Big Omega: 
        Explicarea acestor notații și cum sunt folosite pentru a descrie eficiența algoritmilor în funcție de timp și spațiu. 
        Exemplificare cu algoritmi simpli pentru o înțelegere mai bună.


    Analiza Complexității Spațiale și Temporale: Cum să evaluăm complexitatea spațială și temporală a diferitelor algoritmi, cu exemple practice.


2. Structuri de Date Primitive
Array-uri și Vectori: operații de bază, diferențe între array static și vector
String-uri: manipulări și reprezentare în C++

3. Structuri de Date Liniare
Liste Liniare:
    Liste simplu și dublu înlănțuite
    Implementarea și operațiile de bază: inserție, ștergere, căutare
Stive (Stacks):
    Implementare folosind vectori și liste înlănțuite
    Aplicații ale stivelor: evaluarea expresiilor, parcursul în adâncime (DFS)
Cozi (Queues):
    Cozi simple, cozi cu priorități, implementare folosind liste înlănțuite
    Utilizări ale cozilor: simulări, scheduling

4. Tabele de Dispersie (Hash Tables)
Hashing: funcții hash, gestionarea coliziunilor prin înlănțuire și adresare deschisă
Map și Unordered_Map: diferențe și utilizări

5. Structuri de Date Arborescente
Arbori binari:
    Arbori binari de căutare (BST), AVL, Arbori Roșu-Negru
    Parcurgeri: inordine, preordine, postordine
Heap-uri:
    Min-heap și Max-heap: implementare și aplicații
    Cozi cu priorități în C++

6. Algoritmi de Sortare
Sortare prin inserție, bule, selecție
Sortări avansate: Merge sort, Quick sort, Heap sort

7. Algoritmi pe Grafuri
Reprezentări: liste de adiacență, matrice de adiacență
Parcurgeri: în adâncime (DFS) și în lățime (BFS)
Algoritmi de drum minim: Dijkstra, Bellman-Ford
Arbori de acoperire minimă: Prim, Kruskal

8. Tehnici de Programare
Programare Dinamică: tehnici de bază, probleme clasice (ex: rucsacul, cel mai lung subsir comun)
Backtracking și Greedy Algorithms: aplicabilitate și exemple

9. Studii de Caz și Aplicații
Rezolvarea problemelor practice folosind structuri de date și algoritmi în C++
Optimizări și refactoring de cod