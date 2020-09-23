#  ![python_technologie](images/Python_technologie.png) **Les boucles _Pour_ (avec `FOR`)**


---

## ![python_titre_bleu](images/Python_titre_bleu.png) **Introduction**


En programmation, on est souvent amené à répéter plusieurs fois une instruction. 
Incontournables à tout langage de programmation, les boucles vont nous aider à réaliser cette tâche de manière compacte et efficace. 

Imaginez par exemple que vous souhaitiez afficher les caractères de la chaîne de caractères NSI 3 fois. 
Dans l'état actuel de vos connaissances, il faut taper quelque chose du style:

```python
nom = 'NSI'
print(nom[0])
print(nom[1])
print(nom[2])
print(nom[0])
print(nom[1])
print(nom[2])
print(nom[0])
print(nom[1])
print(nom[2])

```

```
N
S
I
N
S
I
N
S
I

```

Si votre chaîne ne contient que 4 caractères, ceci est encore faisable mais imaginez qu'elle en contienne 100 voire 1000! Pour remédier à cela, il faut utiliser les boucles. 

Regardez l'exemple suivant:


```python
nom = 'NSI'
nombre = 3
for i in range(nombre):
    for lettre in nom :
        print(lettre)

```
```
N
S
I
N
S
I
N
S
I

```

## ![python_titre_bleu](images/Python_titre_bleu.png) **Exemples commentés**

#### **Exemple 1**

![apprendre](images/apprendre.png) **A Tester :**

```python
for fruit in ["pomme", "poire", "cerise"]:
    print("Je mange une", fruit)
print("J'ai plus faim maintenant !")

```

Cet exemple se lit ainsi : 
`pour fruit` prenant chacune des valeurs `dans` la liste `["pomme", "poire", "cerise"]` (dans l'ordre), `afficher` le texte "Je mange une" suivi de la valeur de `fruit`.

L'instruction `print("Je mange une", fruit)` est ici exécutée trois fois, nous dirons qu'il y a eu trois **itérations**.


Bien sûr, comme d'habitude, le nom de la variable `fruit` peut être changé (nous pouvons même mettre _ à la place !) mais autant choisir un nom facile à comprendre.

Ouvrez [_Python Tutor_](http://www.pythontutor.com/visualize.html#mode=edit) (navigateur web). 
Copiez/collez le code de l'exemple 1 puis cliquez sur "Visualize Execution" pour observer l'exécution de votre code pas à pas (regardez en particulier le mouvement de la flèche verte et les valeurs de la variable `fruit`).

#### **Exemple 2**

```python
for lettre in "Anticonstitutionnellement est un mot long":
    print(lettre)

```
Cet exemple montre qu'une chaîne de caractères est (un peu comme son nom l'indique…) une succession de caractères.


![apprendre](images/apprendre.png) **A Retenir :**


 La syntaxe générale est :
 
 ```
 début du programme
 for variable in collection_objets:
     bloc d’instructions à exécuter un certain nombre (la taille de la collection) de fois
 suite du programme
 ```

> Remarquez le point commun avec `if` :
> 
> * le `:` indispensable à la fin de la ligne du `for` ;
> * le bloc d’instructions à repéter est indenté.
>   
> Enfin, remarquez qu'il y a trois étapes, un peu cachées :
> 
> * **Initialisation :** la variable est initialisée à la première valeur de la collection d'objets.
> * **Condition :** tant que toutes les valeurs de la collection d'objets n'ont pas toutes été lues.
> * **Incrémentation :** la valeur de variable prendra à chaque itération la valeur suivante dans la collection d'objets.
 


## ![python_titre_bleu](images/Python_titre_bleu.png) **Accumulateurs**

#### **Exemple 3**  

Lisez le script ci-dessous puis, sur papier, trouvez ce qu'il va afficher. Exécutez-le ensuite pour vérifier.

```python
texte = "J'aime "
for fruit in ["pomme", "poire", "cerise"]:
    texte = texte + "les " + fruit + ","
print(texte)

```

> Ici, la boucle a permis de construire progressivement la valeur de la variable texte.
> 
> Une variable dont la valeur est constituée grâce à une boucle est parfois appelée un accumulateur.


![attention](images/attention.png) **Attention !**

> Quand vous en utilisez un, n'oubliez pas d'initialiser le ou les accumulateur(s) (essayez d'enlever texte = "J'aime " pour voir) avant l'entrée dans la boucle.


## ![python_titre_bleu](images/Python_titre_bleu.png) **Exercices**

#### **Exercice 1**  


Complétez le programme pour obtenir dans resultat la chaîne de caractères mot écrite dans l'ordre inverse.

_Ainsi "abc" doit donner "cba" et "lacer" doit donner "recal"._

```python

mot = "informatique"     #? exemple

resultat = 
for lettre in 
    resultat = 

print(resultat)

```

#### **Exercice 2** 

Complétez le script suivant pour qu'il double les lettres d'un texte (par exemple : avec `initial = "abc"` j'obtiens `final = "aabbcc"`) :

```python
initial = "mettez ce que vous voulez ici"

for lettre in initial:

print(final)
```

## ![python_titre_bleu](images/Python_titre_bleu.png) **Boucle et condition**

Observez puis exécutez le script ci-dessous.

```python
texte = "A vaincre sans péril, on triomphe sans gloire."
texte_reduit = ""
for lettre in texte:
    if lettre not in "aeiouyAEIOUYéèêà": # on peut en trouver d'autres...
        texte_reduit = texte_reduit + lettre # ou : texte_reduit += lettre
print(texte_reduit)

```
Seules les lettres du texte "A vaincre sans péril, on triomphe sans gloire." qui ne sont pas des voyelles sont ajoutées au texte réduit.
Ce script supprime donc les voyelles d'un texte.

Remarquez la double indentation de l'instruction texte_reduit = texte_reduit + lettre (qui est dans le if, lui-même dans le for).



![apprendre](images/apprendre.png) **A Faire :**

Modifiez le script pour qu'il compte les voyelles dans le texte. 


## ![python_titre_bleu](images/Python_titre_bleu.png) **La fonction range**


Bart a encore eu une punition, il doit recopier 100 fois le texte "Je ne me laisserai pas aller à la facilité". 

Comme il a du mal a écrire à la main (c'est fatiguant, vous comprenez), il décide d'utiliser un ordinateur :

```python
print("Je ne me laisserai pas aller à la facilité")
print("Je ne me laisserai pas aller à la facilité")
print("Je ne me laisserai pas aller à la facilité")
print("Je ne me laisserai pas aller à la facilité")

```
mais même en utilisant le copier-coller, c'est laborieux.

Sa soeur, qui le prend en pitié, lui dit que les boucles sont utiles pour cela. Il tente alors :

```python
for n in [1, 2, 3, 4, 5, ...]:
    print("Je ne me laisserai pas aller à la facilité")

```
mais il faut taper tous les entiers jusqu'à 100…

Heureusement, la fonction `range `de Python va l'aider.

Tapez dans l'éditeur l'instruction print(range(10)).
Que remarquez-vous ?

> * la fonction range génère une liste (qui n'est pas une liste Python…) d'entiers consécutifs ;
> * l'instruction range(10) génère une liste de 10 nombres ;
> * le dernier nombre n'est pas 10 mais 9.

![apprendre](images/apprendre.png) **A Faire :**

Ecrivez une commande qui fera gagner du temps (mais pas forcément de la bonne conscience) à Bart.


![apprendre](images/apprendre.png) **A Retenir :**

> * Il y a trois syntaxes pour la fonction range :
>   
>   * range(n) donne une liste de n nombres entiers, de 0 à n-1 ;
>   * range(deb, fin) donne une liste des entiers entre deb inclus jusqu'à fin exclus ;
>   * range(deb, fin, pas) donne une liste des entiers entre deb inclus jusqu'à fin exclus, avec un écart de pas entre chaque.
> 
> * Elle est très utilisé avec for pour répéter des instructions un certain nombre de fois.



![apprendre](images/apprendre.png) **A Faire :**

Générez avec la fonction range les listes suivantes :

* 0, 1, 2, …, 42

* 42, 43, 44, …, 75

* 13, 16, 19, 22, 25, …, 97

