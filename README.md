// CIUREA ROBERT-MIHAI 313CB
// PC - TEMA 2
                                                Tema 2. A Game of Scrabble
                        
    Task0:
-acest task a constat in crearea game_board-ului si afisarea acestuia, astfel ca am creat o matrice de 15 x 15, stocand
 in fiecare element cate un '.'

    Task1:
-acest task a constat in scrierea unor cuvinte in game_board, precum si afisarea acestuia. Astfel ca a trebuit sa
 citim dintr-un fisier numarul de cuvinte, coordonatele primei litere a fiecarui cuvant si directia pe care urma
 cuvantul sa fie scris. Odata ce am citit elementele si am facut conversia din string sau char in int acolo
 unde a fost nevoie, am continuat prin a verifica pentru fiecare cuvant cum trebuie sa aiba orientarea pentru a incepe
 scrierea acestora litera cu litera. La final nu a mai ramas decat afisarea board_game-ului

    Task2:
-acest task a constat in calculul punctajului fiecarui jucator in functie de cuvintele atribuite fiecaruia dintre ei. In
 primul rand a trebuit sa avem grija sa nu atribuim unui jucator cuvantul altui jucator, astfel ca am constatat ca daca am
 fi atribuit cate un numar fiecarui cuvant, player1 ar fi avut cuvintele cu numere pare, iar player2 cuvintele cu numere
 impare, asa am facut diferentiera cuvintelor in functie de cui ii erau atribuite. Mai departe, pentru a calcula punctajul
 fiecarui jucator a trebuit sa calculam punctajul fiecarui cuvant, bazandu-ne pe un vector de 26 de elemente care pe fiecare
 pozitie retinea punctajul atribuit fiecarei litere din alfabetul englez. Fiecare punctaj a fost atribuit jucatorului
 corespunzator pentru ca in final sa se afiseze ambele punctaje

    Task3:
-ascest task a fost asemantor task-ului precedent, diferenta facandu-se la faptul ca punctajul jucatorilor era bazat
 si pe bonusurile atribuite cuvintelor in functie de 2 pattern-uri. Pentru primul pattern m-am bazat pe functia strstr
 care imi cauta in fiecare cuvant aparitia pattern-ului corespunzator, iar daca acesta exista veriifcam in bonus_board
 cate aparitii ale numarului 1 existau in zona unde era scris fiecare cuvant pentru a stii de cate ori sa inmultesc
 punctajul initial al cuvantului cu 2. Verificarea celui de-al 2 lea pattern a fost bazat pe analiza ultimelor 2 litere
 ale cuvantului astfel incat sa se constate daca verifica sau nu conditia. Atribuirea celui de-al 2 lea bonus s-a efectuat
 identic primului pattern, tinandu-se cont de faptul ca puntajul trebuia inmultit cu 3 de oricate aparea numarul 2

    Task4:
-acest task a constat in gasirea urmatorului cuvant care ar fi putut fi utilizat de jucatorul 2 si scrierea acestuia
 in board_game. Astfel ca a trebuit initial sa scriem in board_game fiecare cuvant utilizat de cei 2 jucatori, precum si
 retinerea acestora intr-un vector de aparitie pentru a se verifica care cuvinte din vectorul words mai erau disponibile
 pentru utilizare. De fiecare data cand se gasea unu cuvant neutilizat, se verifica eligibilitatea acestuia. Pentru acest
 lucru am parcurs board_game pozitie cu pozitie de la prima poiztie de pe prima linie pana la ultima pozitie de pe ultima
 linie pentru a verifica daca cuvantul neutilizat era si eligibil scrierii. Odata ce gaseam o aparitie a primei litere a
 cuvantului, trebuia verificat daca acesta avea suficient spatiu pentru a fi scris ori pe orizontala ori pe verticala. Daca
 nu se gasea spatiu in board_game, se cauta urmatorul cuvant din words care ar fi fost neutilizat si a se parcurge din nou
 intregul algoritm. Insa daca se gasea spatiu suficient, ori pe orizontala, ori pe verticala, se retineau coordonatele si
 directia cuvantului si se scriau pe board_game pentru ca in final sa se afiseze matricea