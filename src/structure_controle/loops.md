# Les boucles

Les boucles permettent au programmeur d'exécuter un même morceau de code plusieurs fois. Il existe plusieurs types de
boucles différentes afin de s'adapter à un grand nombre de situations.

Dans cette section, nous verrons les différents types de boucles supportés par AliveScript ainsi que les situations dans
lesquelles une certaine boucle est à privilégier par rapport à une autre.

Il existe 4 types de boucles dans AliveScript:

* La boucle [`repeter`](#la-boucle-repeter)
* La boucle [`tant que`](#la-boucle-tant-que)
    * La boucle [`faire tant que`](#la-boucle-faire-tant-que)
* La boucle [`pour`](#la-boucle-pour)

> Vocabulaire utile lorsqu'on parle de boucles:
> * Une `itération`. Chaque fois que le code contenu dans une boucle est exécuté, on appelle cela une `itération`.
> * Le `corps de la boucle`. Le nom donné au code présent entre l'énoncé d'ouverture et l'énoncé de fermeture de la
    boucle.  
    **Le corps de la fonction est indenté à un niveau de plus afin de faciliter la lecture du code.**

## Pour toutes les boucles d'AliveScript:

Chaque boucle d'AliveScript:

* Commence par un _[énoncé](../annexe/lexique.md#les-énoncés) d'ouverture_. Celui-ci marque le début de la boucle. Tout
  le code après cet énoncé (jusqu'à l'énoncé de fermeture) fait partie du _corps de la boucle_.

* Se conclut par un _[énoncé](../annexe/lexique.md#les-énoncés) de fermeture_. Celui-ci marque la fin de la boucle,
  c'est-à-dire qu'au-delà de ce point, on revient dans le bloc d'exécution précédent.

* Possède une _condition de continuation_ (pas toutes présentées de la même manière) qui
  permet au programme de savoir quand la boucle est terminée et qu'il faut sortir de la boucle pour continuer
  l'exécution du programme.

  > Lorsque l'exécution arrive à l'énoncé de fermeture, on remonte à l'énoncé d'ouverture _si la condition de
  continuation est satisfaite_, sinon on sort de la boucle et on continue l'exécution du programme.

Les mots clefs reliés aux boucles:

* Le mot clef `sortir`: arrête immédiatement la boucle et reprend l'exécution après l'énoncé de fermeture de la boucle.

* Le mot clef `continuer`: remonte immédiatement à l'énoncé d'ouverture de la boucle si la condition de continuation est
  satisfaite, sinon agit comme `sortir`.

## La boucle `repeter`

### Description et fonctionnement

La boucle `repeter` est la boucle la plus simple qu'il est possible de faire en AliveScript.

Lors de l'énoncé d'ouverture, on précise le nombre de fois que la boucle sera effectuée. À chaque fin d'itération de la
boucle, on remonte à l'énoncé d'ouverture jusqu'à ce que la boucle ait été exécutée un nombre de fois précisé dans
l'énoncé d'ouverture.

### Syntaxe

L'[énoncé](../annexe/lexique.md#les-énoncés) d'ouverture de cette boucle est le mot clef `repeter` suivi d'une
valeur entière (voir [type entier](../concepts_base/datatypes/types_primitifs.md#le-type-entier)) ou d'une variable
contenant une valeur entière.

L'[énoncé](../annexe/lexique.md#les-énoncés) de fermeture est le mot clef `fin repeter`

```
repeter <valeur entière>
    # code à l'intérieur de la boucle
fin repeter
```

### Utilité

La boucle `repeter` est utile lorsque le **nombre d'itérations de la boucle est connu** et que le contenu de la boucle
**ne dépend pas de l'itération**, c'est-à-dire qu'il n'y a pas de différences entre la première et la troisième
itérations.

Exemple où on fait la somme de 5 lancers de dés:

```
var sommeLancers = 0
repeter 5
    var lancer = aleatoire({1...6})  # nombre aléatoire entre 1 et 6
    afficher "Lancer: " + lancer  # afficher le lancers
    sommeLancers += lancer  # on l'ajoute à notre somme
fin repeter
            
afficher "La somme des lancers est " + sommeLancers
```

## La boucle `tant que`

### Description et fonctionnement

La boucle `tant que` est une boucle permettant de répéter un morceau de code jusqu'à ce qu'une certaine condition ne
soit plus satisfaite (_la condition de continuation_).

Lors de l'énoncé d'ouverture, on précise la condition de continuation. À chaque fin d'itération de la
boucle, on remonte à l'énoncé d'ouverture jusqu'à ce que la condition de continuation ne soit plus respectée.

### Syntaxe

L'[énoncé](../annexe/lexique.md#les-énoncés) d'ouverture de cette boucle est le mot clef `tant que` suivi par la
condition de continuation sous la forme d'une [expression](../annexe/lexique.md#les-expressions) dont le résultat sera
converti en un [booléen](../concepts_base/datatypes/types_primitifs.md#le-type-booleen).

L'[énoncé](../annexe/lexique.md#les-énoncés) de fermeture est le mot clef `fin tant que`

```
tant que <condition>
    # code à l'intérieur de la boucle
fin tant que
```

### Utilité

La boucle `tant que` est utile lorsque le **nombre d'itérations de la boucle n'est PAS connu** et que celui-ci dépend
d'une condition.

Exemple:

On veut trouver combien de nombres consécutifs il faut additionner pour que leur somme soit plus grande ou égale à 100.

```
var total = 0  # somme des nombres
var i = 0  # nombre courant
tant que total <= 100
    i += 1      # on augmente i de 1 pour passer au prochaine nombre 
    total += i  # on augmente la somme de i
fin tant que
            
afficher "Il faut faire la somme des " + i + " premiers nombres pour dépasser 100"
```

### Fait intéressant

L'énoncé `tant que vrai` permet de faire une boucle qui s'exécute indéfiniment jusqu'à ce qu'on utilise le mot
clef `sortir`.

## La boucle `faire tant que`

### Description et fonctionnement

La boucle `faire tant que` est très semblable à la boucle [`tant que`](#la-boucle-tant-que). Les seules différences
étant la syntaxe et le fait que la boucle `faire tant que` est toujours exécutée au moins une fois, contrairement à la
boucle `tant que` qui peut ne pas être exécutée si la condition de continuation est fausse dès le départ.

### Syntaxe

L'[énoncé](../annexe/lexique.md#les-énoncés) d'ouverture est le mot clef `faire`

L'[énoncé](../annexe/lexique.md#les-énoncés) de fermeture de cette boucle est le mot clef `tant que` suivi par la
condition de continuation sous la forme d'une [expression](../annexe/lexique.md#les-expressions) dont le résultat sera
converti en un [booléen](../concepts_base/datatypes/types_primitifs.md#le-type-booleen).

```
faire
    # code à l'intérieur de la boucle
tant que <condition>
```

### Utilité

La boucle `faire tant que` est utile lorsque le **nombre d'itérations de la boucle n'est PAS connu** et que celui-ci
dépend d'une condition ET que la boucle doit toujours s'exécuter au moins une fois.

Exemple:

À faire

```
#...
```

## La boucle `pour`

