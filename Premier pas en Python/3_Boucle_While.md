#  ![python_technologie](images/Python_technologie.png) **Les boucles _Tant_que_ (avec `WHILE`)**


---

## ![python_titre_bleu](images/Python_titre_bleu.png) **Partie 1**

Ce type de boucle est adapté quand nous ne savons pas à l'avance combien de fois les instructions doivent être répétées.


### Exercice n°1


Demandons à un utilisateur d'entrer des prénoms et arrêtons-nous quand le prénom est "Bébert". 

Lisez puis testez ceci :

```python
prenom = "Hubert"           # ou n'importe quel texte autre que "Bébert"
while prenom != "Bébert":   # tant que le prenom n'est pas "Bébert"
    prenom = input()        # demander à l'utilisateur un autre prénom
    print("Bonjour", prenom)
print("Ah non, pas Bébert !")

```

La boucle se lit ici : 

tant que la variable `prenom` ne contient pas la valeur `"Bébert"`, demander (`input`) une nouvelle valeur, l'affecter à `prenom` et afficher `"Bonjour"`
suivi de la valeur entrée.

La boucle Tant que (`while`) exécute des instructions tant qu'une condition est vérifiée.

![apprendre](images/apprendre.png) **A Tester :**


Que se passe-t-il :

* si vous supprimez la première ligne ?
* si vous mettez `prenom = "Bébert"` à la place de `prenom = "Hubert"` ?


![apprendre](images/apprendre.png) **`WHILE` est plus fort que `FOR`:**


Il est toujours possible de remplacer une boucle `for` par une boucle `while`.

**Par exemple :**

```python
for n in range(100):
    print("Je ne me laisserai pas aller à la facilité")

```
**peut s'écrire :**

```python
nb_copie = 0
while nb_copie < 100:
    print("Je ne me laisserai pas aller à la facilité")
    nb_copie = nb_copie + 1

```
L'inverse n'est pas vrai, il suffit de réfléchir à l'exemple 1 ci-dessus, non réalisable avec un for (nous ne savons pas combien de prénoms l'utilisateur va entrer…).



## ![python_titre_bleu](images/Python_titre_bleu.png) **Partie 2**



Il est fréquent d'utiliser une variable qui va permettre à la boucle de s'interrompre mais d'autres variables peuvent apparaître comme accumulateurs, comme dans l'exemple suivant :

### Exemple 2

Nous allons faire une division entière avec des soustractions ; par exemple combien y a-t-il de 7 dans 61 ? L'idée est ici de retirer des 7 du nombre 61 tant que c'est possible (tant que le résultat dépasse 7).

```python
nb_sept = 0
nombre = 61
reste = nombre
while reste >= 7:              # je peux encore retirer un 7
    nb_sept = nb_sept + 1       # ou nb_sept += 1
    reste = reste - 7         # je retire un 7 du nombre
print("Il y a", nb_sept, "sept dans", nombre)

```
Prenez le temps de regarder comment ce programme fonctionne à l'aide de [Pythontutor](http://www.pythontutor.com/visualize.html#mode=edit).


![apprendre](images/apprendre.png) **A Retenir :**


La syntaxe générale est :

```
début du programme
while condition:
    bloc d’instructions à exécuter tant que la condition est vérifiée
suite du programme 

```

Remarquez les points communs avec `if` et `for` :

* le `:` à la fin de la ligne du `while` ;
* le bloc d’instructions à repéter est indenté.

Enfin, remarquez qu'il y a trois points essentiels pour créer une boucle `while` :

* **Initialisation(s)** : avant la boucle la (ou les) variable(s) utilisées dans la condition _doivent être initialisée_.

* **Test** : bien le définir. En particulier, il est préférable qu'il devienne faux à un certain moment.
* **Modification(s)** : la (ou les) variable(s) utilisées dans la condition _doivent être modifiées_ (sans quoi, la boucle sera infinie).


## ![python_titre_bleu](images/Python_titre_bleu.png) **Les commandes `Break` et `continue`**



La commande `break` permet de sortir définitivement d'une boucle. En général, il est conseillé de se passer de cette commande mais elle peut servir dans de rares occasions.

**Exemple d'utilisation (non pertinente):**

```python
n = 0
while True:     # boucle infinie
    if n == 10:
        break   # sortir de la boucle quand n vaut 10
    n = n + 1   # instruction non exécutée si n vaut 10
print("n vaut", n)

```
La commande `continue` permet de sortir de l'itération actuelle et de passer à l'itération suivante.

**Testez l'exemple suivant :**

```python
n = 0
while n < 10:
    n = n + 1
    if n == 5:
        continue   # passer à l'itération suivante si n vaut 5
    print("n vaut", n)  # instruction non exécutée si n vaut 5

```
Petite remarque au passage : vous avez vu que la dernière ligne dit que n vaut 10, c'est pourquoi il n'y a plus d'autre itération.


## ![python_titre_bleu](images/Python_titre_bleu.png) **Exercice : Température de l'eau.**

Complétez le programme pour obtenir la réponse au problème suivant :

Lydia vient d'arrêter la chaudière alors que la température de l'eau était affichée à 64°.

Elle sait que cette température va baisser de 2 % à chaque minute qui passe.
Au bout de combien de minutes la température de l'eau sera-t-elle descendue en-dessous de 30° ?


```python
temperature = 64    #? température initiale
duree = 0           # temps écoulé en minute

while   :
    temperature = 
    duree = 

print("Dans", duree, "minutes.")
```
