#  ![python_technologie](images/Python_technologie.png) **Les tests**


---

## ![python_titre_bleu](images/Python_titre_bleu.png) **Définition**


Les **tests** sont un élément essentiel à tout langage informatique si on veut lui donner un peu de complexité car ils permettent
à l’ordinateur de prendre des décisions. Pour cela, Python utilise l’instruction **if** ainsi qu’une **comparaison**.

Un programme doit pouvoir s'adapter à des différentes situations grâce à des **tests**.

Par exemple : si la température extérieure est inférieure à 16 degrés alors il faut démarrer le chauffage.

En informatique, un test s'appelle aussi une **structure conditionnelle**.

```python
>>> nombre = 5
```

```python
>>> if nombre == 5 :
...     print("Test vrai")
...
```
## ![python_titre_bleu](images/Python_titre_bleu.png) **Test Si … alors …**

Voici un exemple de script utilisant un test :

```python
a = 3
b = 5
if a < b:
    print("a est le plus petit")

```    
Le test commence par un **if**, suivi d’une condition, puis d’un **:** puis, à la ligne suivante, commence une ou des instructions.


> Ici : si (if en anglais) la condition (ici a < b) est vraie, alors exécuter le bloc d’instructions qui suit (ici une seule instruction), à savoir afficher le texte "a est le plus petit".

La syntaxe générale est :


```
début du programme

if condition:
    bloc d’instructions à exécuter si le test est réussi
suite du programme

```
<center>

![diagramme](images/diagramme1.png) 

<img src="images/diagramme1.png" alt="drawing" width="250"/>

</center>


![apprendre](images/apprendre.png) **Remarquez :**


* le `:` indispensable à la fin de la ligne du `if` ;
* que le bloc d’instructions à exécuter est défini par l'indentation (c'est-à-dire décalées vers la droite d'un même nombre d'espaces); 
* que le bloc d’instructions soit exécuté ou pas, le déroulement du programme continue après le test (suite du programme) ;
* le mot _alors_ n’existe pas en Python (dans certains langages, il se traduit par **then**) ;
* la condition est en fait un _booléen_ (Vrai ou Faux, 0 ou 1).

![apprendre](images/apprendre.png) **A tester :**

Exécutez ce script :

```python
a = 3
b = 5
if a < b:
    print("a est le plus petit")
    print("autrement dit b est le plus grand")

```

Modifiez le script ainsi :

```python
a = 5
b = 3
if a < b:
    print("a est le plus petit")
print("autrement dit b est le plus grand")

```
et observez la différence.

## ![python_titre_bleu](images/Python_titre_bleu.png) **Les conditions**

#### **Conditions d’égalité**

`a == b` est vrai quand la valeur de a est égale à celle de b ;

`a != b` est vrai quand la valeur de a est différente de celle de b.


|Syntaxe Python|Signification
|:--:|:--:|
|**==**|égal à|
|**!=**|différent de|



![apprendre](images/apprendre.png) **Attention !**

> Il faut bien faire attention à distinguer l'affectation a = b et le test d'égalité a == b.



#### **Conditions de comparaison**
Les comparaisons se font à l'aide d'un des quatre opérateurs : `>` ou `<` ou `>=` ou `<=`
(_par exemple_  `if moyenne > 10:`  ).


|Syntaxe Python|Signification
|:--:|:--:|
|**>**|supérieur à|
|**>=**|supérieur ou égal à|
|**<**|inférieur à|
|**<=**|inférieur ou égal à|

![apprendre](images/apprendre.png) **A tester :**


> Comparez des chaînes de caractères à l'aide de < par exemple.
> Comment sont classées les chaînes de caractères ?

#### **Conditions d’appartenance**


Il est possible de tester si une valeur est dans un ensemble ou si une lettre est dans une chaîne de caractères avec l'opérateur `in` (dans) :

```python
print(5 in {3, 5, 7, 9})
print(4 in {3, 5, 7, 9})

print("a" in "abc")
print("'d' est dans 'abc' :", "d" in "abc")

```

Il existe aussi l'opérateur `not in` (pas dans).

On peut même tester si un mot est dans un autre :

```python
print("SI" in "NSI")

```

## ![python_titre_bleu](images/Python_titre_bleu.png) **Test Si … alors … sinon…**

En voici un exemple :

```python
lettre = "u"
if lettre in "aeiouy":
    print("C’est une voyelle")
else:
    print("Ce n’est pas une voyelle")  


```    
* si la condition est vraie (si `lettre` fait partie de "aeiouy") alors le premier bloc d’instruction est exécutée ;
* sinon (ELSE en anglais), c’est-à-dire si la condition est fausse (si `lettre` ne fait pas partie de "aeiouy") alors c’est l’autre bloc d’instructions qui est exécuté et le premier bloc est ignoré.
  
Le couple `if` et `else` agit finalement comme un aiguillage.


```flow
st=>start: Début
cond=>condition: Si condition?
op=>operation: Bloc instructions 1
op2=>operation: Bloc instructions 2

e=>end: Suite

st->cond->op->e
st->cond->op2->e
cond(yes)->op
cond(no)->op2

```

![apprendre](images/apprendre.png) **A tester :**


Sans utiliser l'éditeur, indiquez la valeur de la variable s à la fin de ce script (aidez vous d'un brouillon):

```python
e = 4
f = 2
if f != e:
    f = f - e + 1
    s = e + f + 5
else:
    s = 2 + e + f

```


## ![python_titre_bleu](images/Python_titre_bleu.png) **Exercices**




#### **Exercice 1 : Le code PIN de Marc.**

Le code pin du téléphone de Marc est 4567 mais il l'a oublié !
Corrigez le programme suivant pour qu'il affiche :
"Code correct" lorsqu'il entre le bon code
"Code incorrect, désolé !" dans le cas contraire

```python
reponse = input("Votre mot de passe ?")

if reponse :
    print("Code correct")

print("Code incorrect, désolé !")

```


#### **Exercice 2 : Pair ou Impair.**

Complétez le programme pour qu'il affiche la réponse qui convient.
Vous pouvez utiliser l'opérateur % (modulo) qui donne le reste dans une division euclidienne.

Ainsi `26 % 10 == 6` puisque 26 divisé par 10 fait 2 et il reste 6.


```python

n = input("Entrez un nombre")

if           :
    print(n, "est un nombre pair")
else:
    print(n, "est un nombre impair")

```

## ![python_titre_bleu](images/Python_titre_bleu.png) **Test Si … alors … sinonsi …**

Parfois, pour déterminer dans quel cas on se trouve, il faut effectuer plusieurs tests.

![apprendre](images/apprendre.png) **A tester :**

Prenez le temps de lire le script ci-dessous qui doit nous dire quel sera notre mention au bac. Exécutez-le plusieurs fois en changeant la valeur de ma_note et observez.

```python
ma_note = 13
if ma_note >= 16:
    print("Mention TB")
if ma_note >= 14:
    print("Mention B")
if ma_note >= 12:
    print("Mention AB")
else:
    print("Pas de mention")
```

> _Ce script ne fonctionne pas comme prévu. Normalement, il ne devrait y avoir qu'un message d'affiché. C'est parce que les tests sont tous indépendants. Même si le premier test est réussi, les autres tests sont également effectués et potentiellement validés (si ma note est supérieure à 16 alors elle est aussi supérieure à 14 et à 12), alors qu'ils ne devraient l'être que si les précédents ont échoués. Il faut donc imbriquer les tests._



![apprendre](images/apprendre.png) **A tester :**

Modifiez maintenant le programme ainsi  puis testez son bon fonctionnement :

```python
if ma_note >= 16:
    print("Mention TB")
else:
    if ma_note >= 14:
        print("Mention B")
    else:
        if ma_note >= 12:
            print("Mention AB")
        else:
            print("Pas de mention")

```

> _Si la note est supérieure ou égale à 16 alors le programme affiche "Mention TB", sinon il envisage le cas où la note est inférieure à 16, ce qui se sépare en plusieurs cas…
> Ce script fonctionne bien mais "à cause" du système d'indentation, sa lecture n'est pas si simple.
C'est pourquoi il existe une syntaxe permettant de simplifier la rédaction des études de cas, en utilisant le mot clé elif (contraction de else if)._


```flow
st=>start: Début
cond=>condition: Si condition 1 ?
cond2=>condition: Si condition 1 ?
op=>operation: Bloc instructions 1
op2=>operation: Bloc instructions 2
op3=>operation: Bloc instructions 3
e=>end: Suite

st->cond->op->e
st->cond->cond2
op2->e
op3->e
cond(yes)->op
cond(no)->cond2
cond2(yes)->op2
cond2(no)->op3

```





Ce script

```
if condition1:
    bloc d’instructions 1
else:
    if condition2:
        bloc d’instructions 2
    else:
        bloc d’instructions 3
suite du programme

```

peut aussi s’écrire ainsi :
```
if condition1:
    bloc d’instructions 1
elif: condition2:
    bloc d’instructions 2
else:
    bloc d’instructions 3
suite du programme
```


![apprendre](images/apprendre.png) **A tester :**


Modifiez le programme ainsi puis testez son bon fonctionnement :
> 
> if ma_note >= 16:
>     print("Mention TB")
> elif ma_note >= 14:
>     print("Mention B")
> elif ma_note >= 12:
>     print("Mention AB")
> else:
>     print("Pas de mention")

Rajoutez une condition si la note est inférieur à 10 pour indiquer au candidat qu'il est récalé.

## ![python_titre_bleu](images/Python_titre_bleu.png) **Exercices**

#### **Exercice 3 : Quel âge as tu?**

Ecrire un programme dans lequel la machine demande à un utilisateur son âge et dit si l’utilisateur est un enfant (moins de 12 ans) ou un adolescent (entre 12 et 18 ans) ou un adulte (à partir de 18 ans).

#### **Exercice 4 : Professeur Zarbi.**

Le professeur Zarbi met des notes sur 72 points puis les transforme en appréciations suivant ce tableau :

```
Note N	Appréciation
N >= 80 %	A
80 % > N >= 60 %	B
60 % > N >= 50 %	C
50 % > N >= 40 %	D
N < 40 %	E

```
Ecrire un programme qui s'occupe de la conversion en appréciation d'une note N entrée par l’utilisateur sous forme de points (_par exemple si j'entre 39, le programme renvoie C_).
