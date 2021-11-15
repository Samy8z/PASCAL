
# Les piles et les files (P&F) sont des protocoles de gestion des fluxs des données (des informations)  

avant tout des protocoles avant d’être de l’informatique

Le convoyage des produits déposés sur le tapis roulant d’une caissière est une file, un escalator est une file. Les tours de hanoï c’est une piles, une pile d’assiette est une pile, une pile alcaline n’est pas une file

Dans les ordinateurs les piles et les files sont aussi présentes. Soit au niveau matériel soit au niveau logiciel. en anglais “Stack & queue”

Ex de pile : Pile d'exécution du CPU, stack overflow
Dans les navigateurs et logiciel de traitement de texte, ctrl + z et ctrl + y sont des piles

Les files : files d’impression (envoie de doc à l’imprimant c’est une file)

Des piles et des files il y a en partout

rmq : les piles et files sont tellement classique au niveau logiciel que dans tous les langages de programmation évolué intègre déjà sous la forme de bibliothèque des piles et des files

Premièrement les piles.

La pile est un protocole LIFO (Last In First Out) c a d la donnée la plus jeune qui est manipulée. La dernière donnée se trouvent sur le sommet de la pile c’est donc la dernière c’est donc la plus jeune dans le temps

On accède au information d’une pile seulement et uniquement par le sommet

Le sommet de la pile est le seul index nous permettant de gerer la pile

La gestion d’une pile est forcément séquentiel

le protocole LIFO est défini par 4 services (procédures/outils) standard + un 5e non standard mais admis en informatique et seulement en info

Les 4 outils standard sont :

    - Empiler (push) permet d’ajouter une donnée dans la pile en ayant incrémenté le sommet , la donnée est donc une entrée
    - dépiler (pop) | permet de retirer de la pile, lecture de la donnée du sommet puis décrémente du sommet. La donnée est une sortie 
    - Pile vide (stack empty) est un service qui renvoi un booléen vrai lorsque la pile est vide. Fonctionne en symbiose avec pop 
    - pile pleine (stack full) qui renvoi un booléen vrai quand la pile est pleine fonctionne en symbiose avec push
    - 5e service non standard | Affichage de la pile ATTENTION on respect le protocole, on va du sommet vers la base 

Exemple : gestion d’une pile 

(cf photo discord/ jules)

___________________________________________________________________________

COUR sur les structures permettant de programmer une pile

Le types structure est un moyen permettant de stocker dans une variable de type structure plusieur élément c'est à dire des informations c'est à dire des variables qui sont de type hétérogène ou pas

rmq : contrairement au tableau qui permet de stocker des éléments de même nature et seulement de même nature. La structure permet au besoin l'hétérogénéité

Exemple :

    Une variable individu de type structure  qui contient une variable age de type entier une variable sex de type char une variable de type tableau d’entier permettant de coder le code postal et une autre variable “adresse” de type string.

Toutes ces variables c'est à dire l'âge,sex,code postal et l’adresse sont manipulables en même temps avec la variable individu autrement dit la variable individu contient les 4 autres variables.

Définition algorithmique de l’individu :

Type t_individu = Structure
    Age : Entier
    Sexe : Char
    CoPos : t_Tab_CoPos
    Adresse : Chaine [500]
finStructure
Variable
    individu : t_individu

P.P.
individu.Age ← 20
individu.Sexe ← ‘F’
Pour cpt de 1 à 5 faire
Affiche(individu.CoPos[cpt])
finPour

Pour cpt de 1 à 5 faire
    lire(val)
    individu.CoPos[CP] ← val

Type t_Pile = structure
    Tab_Pile : tab_Pile
    Sommet : Entier
Variable
    pile : t_pile

Procédure Push (val,stk)
paramètre par valeur
    val : t_data // Entier
paramètre par adresse :
    stk : t_pile

Début
    stk.Sommet← stk/sommet + 1
    stk.Tab_pile[stk.Sommet] ← Val
Fin

Cour sur les files :

Introduction

La file est d’abord un protocole, en anglais FIFO pour First In First Out

rmq : ce protocole permet de gérer les données les plus anciennes
rmq : la pile gère les plus récente (les jeunes)

FILE / QUEUE LIFO
Enfiler → 3 // 2 // 1 → Défiler

Les files sont présentes au niveau logiciel et au niveau matériel dans les chaînes c’est aussi présent dans énormément logiciel algorithme de recherche opérationnel

4 outils standard et 1 non standard

Enfiler Queue IN
Défilé Queue OUT
File vide Queue empty
File pleine  Queue FULL
5e service non standard | Affichage de la file ATTENTION on respect le protocole, on va du dernier vers le 1er Queue Show
Gestion d’une file en statique

On utilise 2 index
1 pour enfiler enQ et 2 pour défiler DeQ
