# ![projet](images/yoda.png)  **Recherche d'un nombre par dichotomie**


## Variante 1 : Number's Yoda



La recherche par dichotomie est une méthode qui consiste à diviser (en général en parties égales) un problème pour en trouver la solution. 
À titre d’exemple, voici une discussion entre **Vador** et **Yoda** dans laquelle Vador essaie de deviner le nombre (compris entre 1 et 100 inclus) auquel Yoda a pensé.

+ **[Yoda]** « C’est bon, j’ai pensé à un nombre entre 1 et 100. »
+ **[Vador]** « OK, je vais essayer de le deviner. Est-ce que ton nombre est plus petit ou plus grand que 50 ? »
+ **[Yoda]** « Plus grand. »
+ **[Vador]** « Est-ce que ton nombre est plus petit, plus grand ou égal à 75 ? »
+ **[Yoda]** « Plus grand. »
+ **[Vador]** « Est-ce que ton nombre est plus petit, plus grand ou égal à 87 ? »
+ **[Yoda]** « Plus petit. »
+ **[Vador]** « Est-ce que ton nombre est plus petit, plus grand ou égal à 81 ? »
+ **[Yoda]** « Plus petit. »
+ **[Vador]** « Est-ce que ton nombre est plus petit, plus grand ou égal à 78 ? »
+ **[Yoda]** « Plus grand. »
+ **[Vador]** « Est-ce que ton nombre est plus petit, plus grand ou égal à 79 ? »
+ **[Yoda]** « Égal. C’est le nombre auquel j’avais pensé. Bravo ! »

Pour arriver rapidement à deviner le nombre, l’astuce consiste à prendre à chaque fois la moitié de l’intervalle dans lequel se trouve le nombre. 

Voici le détail des différentes étapes :

```
1. le nombre se trouve entre 1 et 100, on propose 50 (100 / 2).
2. le nombre se trouve entre 50 et 100, on propose 75 ( 50 + (100-50)/2 ).
3. le nombre se trouve entre 75 et 100, on propose 87 ( 75 + (100-75)/2 ).
4. le nombre se trouve entre 75 et 87, on propose 81 ( 75 + (87-75)/2 ).
5. le nombre se trouve entre 75 et 81, on propose 78 ( 75 + (81-75)/2 ).
6. le nombre se trouve entre 78 et 81, on propose 79 ( 78 + (81-78)/2 ).

```
Créez un script qui reproduit ce jeu de devinettes. Vous pensez à un nombre entre 1 et 100 et l’ordinateur essaie de le
deviner par dichotomie en vous posant des questions.
Votre programme utilisera la fonction ``input()`` pour interagir avec l’utilisateur.


## Variante 2 : Number's Vador

Créez un script qui reproduit ce jeu de devinettes. Maintenant c'est **Vador** qui va penser à un nombre entre 1 et 100 et **Yoda** (vous)  va essayer de le
deviner. 
Votre programme utilisera la fonction ``input()`` et `print` pour interagir avec l’utilisateur.

**Remarque :** Pour tirer un nombre au hasard on utilise la fonction `randint()` du **module random** qui permet de générer des nombres entiers aléatoires (ici entre 1 et 100 inclus).

```python
from random import *

# donne un nombre nb aléatoire entre 1 et 100
nb = randint(1,100)
print (nb)
```

donne :

```
*** Console de processus distant Réinitialisée *** 
65
>>> 
```

## Variante 3 : Interagir avec l’utilisateur

Niveau 1 :3rd_place_medal:

* Votre programme doit proposer une invitation pour choisir un nombre ou deviner le nombre de l'autre.

* On doit avoir la possiblité de quitter le jeux ou de recommencer.

Niveau 2 :2nd_place_medal:

* On doit  pouvoir avoir un mode combat, avec un nombre de round a choisir ou chaque joueur tentera de deviner le nombre de l'autre.

Niveau 3 🥇 

* Vous devez ajouter un compteur de tentative, un compteur de nombre de partie.

* Si le joueur decide de quitter le jeu, il doit s'afficher un recapitulatif du nombre de partie, du cumul de tentative pour les deux joueurs et désigner un gagnant. (Moins de tentative = Gagnant)


Il faut aussi soigner la convivialité des dialogues
