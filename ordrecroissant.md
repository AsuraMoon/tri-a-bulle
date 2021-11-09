Faire un tri croissant de valeur

Procédure recupValeursEtTaille(tableau[], valeur , taille)
    taille ← 0 ;
    Répéter tant que valeur != X ;
        Pour tableau[valeur] ← 0 par pas de 1 ;
            taille = taille + 1 ;
            Display "Entrer vos valeurs ou mettez X quand vous avez fini" ;
            lire tableau[valeur] ;
        FinPour ;
    Fin Répéter tant que ;
Fin Fonction ;

Procédure croissant (valeur[] , position , taille , vérif )
    Répéter Tant que vérif != faux
        vérif ← faux
        Pour valeur[position] ← 1 jusqu'a valeur[position] < taille par pas de 1 ;
            Si valeur[position] < valeur[position+1] ; 
            alors
                vérif ← vrai
                temp ← valeur[position] ;
                valeur[position] ← valeur[position+1] ;
                valeur[position+1] ← temp ;
            Fin Si
        Fin Pour
    Fin Répéter Tant que

var ordreCroissant[]; entier
    chiffre , tailleTableau 

Début
    Procédure recupValeursEtTaille (ordreCroissant , chiffre , tailleTableau)
    Procédure  croissant (ordreCroissant , chiffre , tailleTableau)
    Renvoi tableau
Fin

4! = 4x3x2


Fonction Cherche(valeurVrai , valeurOrdi)
Valeur←100
    Si valeurVrai != valeurOrdi
        alors 
        Si valeurVrai < valeurOrdi
            valeurOrdi ← valeurOrdi-(valeurOrdi/2)
            retourne Cherche(valeurVrai , ValeurOrdi)
        Sinon
            valeurOrdi ← valeurOrdi+(valeurOrdi/2)
            retourne Cherche(valeurVrai , ValeurOrdi)
        FSi
    Fsi



/////////////////////


Tri Rapide

tableau a n valeur (0 a n-1)
max = n-1

faut comparer n-1 avec les valeurs précedantes et les décalées si elle sont sup
    par pas de 1 
    si (n-1)<((n-1)-n)


5       9   1   4   2       7   5
-6+0 -6+1 -6+2 -6+3 -6+4 -6+5 -6+6
6-6  6-5  2-6  3-6  4-6  5-6  6-6

Const valeurPivot[n]
Pour valeur[n-(n-i)] ← 0 jusqu'a valeur[n] < n par pas de 1 ;
    Si valeurPivot[n] < valeur[n-(n-i)] ;
    alors
        temp ← valeur[n-(n-i)] ;
        valeur[n-(n-i)] ← valeur[n] ;
        jusqu'à valeur[n-1] ← valeurPivot[n] ;
        n <- n-1
    Fin Si
Fin Pour


/////////////////////////////////////////::


8   2   9   1  |4|
1   2   9  |4|  8
2   1  |4|  9   8

1   2  |4|  9   8
1   2  |4|  8   9

////////////////


4   3   5   9   1   2   7   8  |6|
4   3   5   8   1   2   7  |6|  9
4   3   5   7   1   2  |6|  8   8
4   3   5   2   1* |6|  7   8   9

2   3   5   1*  4          |6|            7   8   9
5   3   1*  2   4          |6|            7   8   9
3   1*  5   2   4          |6|            7   8   9
1*  3   5   2   4          |6|            7   8   9

1   3   5   2   4*         |6|            7   8   9
1   3   2   4*  5          |6|            7   8   9

1   3   2*  4   5          |6|            7   8   9
1   2   3   4   5          |6|            7   8   9