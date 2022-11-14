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
  continuation
  > est satisfaite_, sinon on sort de la boucle et on continue l'exécution du programme.

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
repeter <valeur numérique>
    # code à l'intérieur de la boucle
fin repeter
```

### Utilité

La boucle `repeter` est utile lorsque le **nombre d'itérations de la boucle est connu** et que le contenu de la boucle
**ne dépend pas de l'itération**, c'est-à-dire qu'il n'y a pas de différence entre la première et la troisième
itérations.

Ex:

```

```

## La boucle `tant que`

## La boucle `faire tant que`

## La boucle `pour`

