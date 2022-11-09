# Les collections

Une collection est un rassemblement de données. Il existe deux types de collections dans AliveScript:

* les `liste`
* les `dict`

## Le type `liste`

Une liste est une collection (un rassemblement) de valeurs ordonnées par leur ordre d'insertion. (la première valeur est
en premier, la 2e est en deuxième, etc.)

On nomme un membre d'une liste un `élément` et sa position dans la liste est nommée `index`.

Une liste commence par un crochet ouvrant `[` et se termine par un crochet fermant `]`.

Une liste *peut contenir d'autres listes*

Ex:

```
[]  # liste vide, elle ne possède pas d'éléments
[vrai, 1, 21, "salut"]
["hey", ["toi", 2, 2, 3], 3]
```

## Le type `dict`

Les dictionnaires servent à organiser des données selon des clefs et des valeurs, à la manière des dictionnaires de
langues qui associent des mots avec des définitions. Ce type de collection offre ainsi plus de flexibilités et de
possibilités d'organisation qu'avec les listes, car on peut trouver une valeur en cherchant sa clef, sans avoir besoin
de connaître son index.

Un dictionnaire (type `dict`) est une collection de valeurs de type [paires](./types_primitifs.md#le-type-paire)
ordonnées par leur ordre d'insertion.

* Chaque paire d'un dictionnaire est appelé un `item`
* Lorsqu'on parle des `clefs d'un dictionnaire`, on parle de l'ensemble des clefs des paires de ce dictionnaire.
* Lorsqu'on parle des `valeurs d'un dictionnaire`, on parle de l'ensemble des valeurs des paires de ce dictionnaire.

En plus de pouvoir accéder aux éléments d'un dictionnaire par leur index (comme les listes), on peut accéder à une
valeur contenue dans le dictionnaire en utilisant l'une de ses clefs (voir les opérations sur les dictionnaires au
[_chapitre 2.5.3_](../operateurs/iterables.md))

Un dictionnaire commence par une accolade ouvrante `{` et se termine par une accolade fermante `}`.

Un dictionnaire *peut contenir d'autres dictionnaires*.

Chaque clef d'un dictionnaire doit être _unique_, mais plusieurs clefs peuvent avoir la même valeur.

```
{"abc": "def", "ghi": "def"} ✅
{"abc": "def", "abc", "ghi"} ❌
```

Ex:

```
{}
{"abc": 12, "def": vrai, "ghi": [1, 2, 3]}
{"personne": {"nom": "Mathis", "age": 20}, "addresse": "123 rue Imaginaire"}
```
