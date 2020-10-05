#  ![python_technologie](images/Python_technologie.png) **Bon départ avec les Fonctions en Python**


---

## ![python_titre_bleu](images/Python_titre_bleu.png) **Situation n°1**

### Introduction

Le droit d'entrée journalier dans un parc d’attraction est de **37€** pour un **adulte** et de **28€** pour un **enfant**.  

Alice et Bob doivent faire payer les entrées, mais leur caisse est malheureusement tombée en panne, et la queue s’allonge très vite… 

On leur fourni en urgence une calculatrice qui dispose de Python pour les aider.

Un groupe de **2 adultes et 2 enfants** se présente à la caisse. 
Il faut donc calculer :  **`2*37 + 2*28`**

Un groupe de **3 adultes et 5 enfants** se présente à la caisse. 
Il faut donc calculer :   **`3*37 + 5*28`**

Un groupe de **1 adulte et 3 enfants** se présente à la caisse. 
Il faut donc calculer :   **`1*37 + 3*28`**

Ces calculs sont très répétitifs, et prennent du temps. La queue continue à s’allonger …

Ils remarquent qu’il suffirait de saisir le **nombre d’adultes** et le **nombre d’enfants** pour automatiser le calcul. 

Ils décident d’écrire une fonction en Python :

```python

def prix(nbre_adultes,nbre_enfants):
    resultat = 37*nbre_adultes + 28*nbre_enfants
    return resultat

```

![apprendre](images/apprendre.png) **A Tester :**

**Ouvrir** l’éditeur Python (par exemple EduPython), **recopier** ce script, puis l’**exécuter**.

_Que se passe-t-il ?_


![apprendre](images/apprendre.png) **A Tester :**

Dans la console, **saisir** : 

`>>> prix(3,2)` 

_Qu’obtenez-vous ?_

Dans la console, **saisir** : 

`>>>prix(2,3)`

_Qu’obtenez-vous ?_



**Remarques :**

> Si on « appelle » **prix(3,2)** : 
> •	3 est automatiquement affecté à la variable `nbre_adultes`
> 
> •	2 est automatiquement affecté à la variable `nbre_enfants`          

Alice et Bob ont créé la **fonction** dont le nom est `prix`, qui a deux **paramètres** `nbre_adultes` et `nbre_enfants`


### Petits changements


La situation d’Alice et Bob s’est nettement améliorée, mais ils veulent aller encore plus vite. 

Ils voudraient juste saisir les nombres d’adultes et d’enfants, par exemple 3 et 2 , et ne pas avoir à écrire `prix(3,2) `.

Pour cela, ils écrivent le script suivant : 

```python
def prix(nbre_adultes,nbre_enfants):
    resultat = 37*nbre_adultes + 28*nbre_enfants
    return resultat

adultes = int(input("Nombres d'adultes ?"))
enfants = int(input("Nombres d'enfants ?"))
a_payer = prix(adultes,enfants)
print("Somme à payer : ",a_payer)

```

![apprendre](images/apprendre.png) **A Tester :**

**Recopier** ce script dans l’éditeur puis l’**exécuter**.

_Que se passe-t-il ?_

> La fonction `prix` a été **appelée**. Le résultat **renvoyé** par la fonction a été **affecté** à la variable `a_payer`. Cette variable a ensuite été **affichée**.

#### Exercice n°1

On vient signaler à Alice et Bob qu’un nouveau tarif entre en vigueur instantanément : 

- le tarif « étudiant » à 30€. 


![apprendre](images/apprendre.png) **A Faire :**

**Modifier** le script précédant pour qu’il tienne compte de ce nouveau tarif.

Le **tester** pour 1 adulte, 2 étudiants, 3 enfants. Le prix à payer doit être 183 €.

#### Exercice n°2


**Nouveauté** : si c’est le jour d’anniversaire d’une personne du groupe, tout le groupe bénéficie d’une réduction de 10 %.

![apprendre](images/apprendre.png) **A Faire :**

Sans modifier la fonction de l'**Exercice n°1**, **compléter** le programme pour qu’il demande si c’est un jour anniversaire, et qu’il affiche le prix à payer suivant les cas.

On rappelle que pour diminuer un prix de 10%, il suffit de le multiplier par 0.9.


## ![python_titre_bleu](images/Python_titre_bleu.png) **Situation n°2**

Le petit frère de Bob doit apprendre ses tables de multiplication.

Pensant l’aider, Bob écrit la fonction suivante :

```python
def table_mult(nbre):

    for i in range(1,11):
        return (i*nbre)

print (table_mult(9))

```

![apprendre](images/apprendre.png) **A Faire :**

**Recopier** puis **exécuter** ce script. 

_Que se passe-t-il?_


## ![python_titre_bleu](images/Python_titre_bleu.png) **Et si l’on veut que notre fonction fasse plusieurs choses ?**




Vous rencontrerez souvent des fonctions comme celle se trouvant dans le script ci-dessous : 

```python
def somme_prod (nbre1,nbre2):
    return nbre1 + nbre2 , nbre1 * nbre2

resultat = somme_prod(2,5)
print(resultat)
print(type(resultat))

```


![apprendre](images/apprendre.png) **A Faire :**

**Recopier**, puis **exécuter** ce script. 

_Que s’affiche-t-il ?_

> Vous observez que des **parenthèses** sont apparues dans l’**affichage** du résultat. 
> 
> En fait il y a **une seule variable retournée**, et non deux, qui est de **type tuple** (ici un “couple” de deux entiers), comme l’affichage de la ligne suivante le confirme. 
> 
> Nous étudierons plus tard les tuples.


## ![python_titre_bleu](images/Python_titre_bleu.png) **Comment créer une fonction qui nous donne une table de multiplication ?**

### ![python_titre_bleu](images/Python_titre.png) **Methode n°1:**



On écrit une fonction qui renvoie une « liste » ou un « tuple».

Une telle fonction renverra par exemple pour la table de 9 

•	Si la fonction renvoie une liste : `[9,18,27,36,45,54,63,72,81,90]`
•	Si la fonction renvoie un tuple : `(9,18,27,36,45,54,63,72,81,90)`

Nous étudierons les listes et les tuples un peu plus tard


### ![python_titre_bleu](images/Python_titre.png) **Methode n°2:**

On peut écrire une fonction qui ne renvoie rien, mais qui fait des actions, comme par exemple des affichages. 

Une **fonction** qui **ne renvoie rien** s’appelle une **procédure**.



![apprendre](images/apprendre.png) **A Faire :**

**Recopier** et **exécuter** le script.

```python
def table_mult(nbre):
    for i in range (1,11) :
        print (i*nbre)
    return None

```

Puis dans la console taper : `table_mult(9)`

_Que s’affiche-t-il?_



![apprendre](images/apprendre.png) **A Faire :**

**Modifier** le script en supprimant la ligne return None. (Vous pouvez juste écrire un # devant la ligne)

_Que s’est-il passé ?_


> Dans une procédure, la ligne `return None` est facultative.


## ![python_titre_bleu](images/Python_titre_bleu.png) **Une fonction sans paramètre ?**



**Tester** le programme suivant :

```python
from random import*

def jouer() :
    return randint (1,6)

for i in range(10) :
    de = jouer()
    print (de)
```


#### A retenir :

> Une fonction commence par le mot **def** , suivi du **nom de la fonction**, de la liste des paramètres entre parenthèses, et de « **:** ».
> 
> Toutes les **instructions** d’une fonction sont **indentées**.
> 
> S’il n’y a **pas de paramètres**, il faut obligatoirement mettre des **parenthèses vides**.
> 
> Une fonction ne peut **renvoyer qu’une seule variable**. Cela se fait avec l’instruction **return** .
> 
> L’exécution de l’instruction **return** provoque obligatoirement la **sortie de la fonction**. Si d’autres instructions se trouvent après return elles ne seront jamais exécutées. 
>  
> La valeur renvoyée est indiquée par l’instruction (optionnelle) return. Si celle-ci n’est pas présente, la valeur par défaut None est renvoyée.


## ![python_titre_bleu](images/Python_titre_bleu.png) **Appeler une fonction dans une fonction**




![apprendre](images/apprendre.png) **A Tester :**

**Recopier** et **exécuter** le script suivant :

La fonction `euro_vers_yuan` appelle deux autres fonctions. Cela ne pose aucun problème.


```python
def euro_vers_dollar (euros) :
    return euros*1.17 # on suppose que 1 euros = 1,17 dollars

def dollar_vers_yuan(dollars) :
    return dollars*6.75 # on suppose que 1 dollar = 6.75 yuan

def euro_vers_yuan(montant) :
    # appel de la fonction euro_vers_dollar
    montant_dollar = euro_vers_dollar(montant)
    # appel de la fonction dollar_vers_yuan
    montant_yuan = dollar_vers_yuan(montant_dollar)
    # valeur renvoyee
    return montant_yuan

print (euro_vers_yuan(2))

```

#### Remarque sur la “portée des variables” :

**`euros`** est une variable locale dans la fonction **`euros_vers_dollars`** ,  **`dollars`** est une variable locale dans la fonction **`dollar_vers_yuan`**, et **`montant`** une variable locale dans la fonction **`euro_vers_yuan`**. Ces variables ne sont “connues” que dans ces fonctions.

### ![python_titre_bleu](images/Python_titre.png) **Conséquence n°1 : Choix du nom des paramètres**

Nous aurions donc pu choisir pour chaque fonction le même nom de paramètre.

![apprendre](images/apprendre.png) **A Faire :**

**Modifier** le script précédant de la façon suivante, l’**exécuter**, et le **tester**.

```python
def euro_vers_dollar (montant) :
    return montant*1.17 # on suppose que 1 euros = 1,17 dollars

def dollar_vers_yuan(montant) :
    return montant*6.75 # on suppose que 1 dollar = 6.75 yuan

def euro_vers_yuan(montant) :
    # appel de la fonction euro_vers_dollar
    montant_dollar = euro_vers_dollar(montant)
    # appel de la fonction dollar_vers_yuan
    montant_yuan = dollar_vers_yuan(montant_dollar)
    # valeur renvoyee
    return montant_yuan

print (euro_vers_yuan(2))

```

Ici nous avons **trois variables locales différentes montant** dans les trois fonctions du script.

### ![python_titre_bleu](images/Python_titre.png) **Conséquence n°2 : Une variable “locale”, n’est pas reconnue à “l’extérieur”**

![apprendre](images/apprendre.png) **A Tester :**

**Recopier** et **exécuter** le script suivant :
 
```python
def euro_vers_dollar (montant) :
    resultat_dollars = montant*1.17 # on suppose que 1 euros = 1,17 dollars
    return resultat_dollars

print (euro_vers_dollar(1))
print(resultat_dollars)

```


_Que se passe-t-il ?_


### ![python_titre_bleu](images/Python_titre.png) **Conséquence n°3 : Méthode souvent utilisée** 

On affecte à une variable la valeur renvoyée par une fonction.

![apprendre](images/apprendre.png) **A Tester :**

**Recopier** et **exécuter** le script suivant :

```python
def euro_vers_dollar (montant) :
    resultat_dollars = montant*1.17 # on suppose que 1 euros = 1,17 dollars
    return resultat_dollars

montant_euros = float(input("Saisir le montant en euros :"))

'''
Nous allons affecter à la variable montant_dollars
la valeur renvoyée par la fonction ero_vers_dollar
'''
montant_dollars = euro_vers_dollar(montant_euros)

#afficahge du résultat :
print(montant_dollars)

```

![apprendre](images/apprendre.png) **Attention :** ne pas utiliser des noms de variables et des noms de fonctions identiques


## ![python_titre_bleu](images/Python_titre_bleu.png) **“Docstring” d’une fonction**

Nous reviendrons plus tard dans l’année sur les “docstring” d’une fonction, et ajouterons d’autres éléments.  

Pour le moment, nous les utiliserons pour  expliquer le rôle d’une fonction.

Cette “docstring” est composée de lignes de texte écrites entre '''et ''' (touche 4) ou bien """ et """ (touche 3).

Ces lignes ne sont pas exécutées par le programme, et simplement destinées à donner des explications à celui qui lit le code (script).

**Par exemple :**

```python
def euro_vers_dollar(euros):
    '''
    Cette fonction renvoie la valeur de euros en dollars
    Par exemple euro_vers_dollar(1) doit renvoyer 1,17
    euro_vers_dollar(2) doit renvoyer 2,34
    '''
    return euros*1.17 # on suppose que 1 euro = 1.17 dollars

```


