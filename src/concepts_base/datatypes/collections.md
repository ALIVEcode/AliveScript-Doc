# Les collections

Une collection est un rassemblement de données. Il existe deux types de collections dans AliveScript:

* les listes (type `liste`)
* les dictionnaires (type `dict`)

## Le type `liste`

Une liste est une collection (un rassemblement) de valeurs ordonnées par leur ordre d'insertion.  
Les listes permettent de **regrouper plusieurs données en une seule**.

### Terminologie

* Un membre d'une liste est appelé un `élément` de la liste.
* La position d'un élément dans une liste est appelée son `index`.

### Syntaxe

* Une liste commence par un _crochet ouvrant_ `[` et se termine par un _crochet fermant_ `]`.
* Chaque élément d'une liste est séparé par une _virgule_ `,`.

### Particularités

* On compte les index à partir de `0`.
* Les éléments d'une liste peuvent être de n'importe quel type.
    * Par conséquent, une liste *peut contenir d'autres listes*.

### Exemple de listes:

```
var maListeVide = []

var mesFruits = ["pommes", "bananes", "oranges"]

var listeMelange = [vrai, 21, "salut", 1.2]

var listeAvecListe = [1, 2, 3, [4, 5, "six"], 7]
```

## Le type `dict`

Les dictionnaires servent à organiser des données selon des [paires](./type_particulier.md#le-type-paire)
de `clef:valeur`, à la manière des dictionnaires de langues qui associent des mots avec des définitions.

Comme nous allons voir, ce type de collection offre de nouvelles possibilités d'organisations des données.

### Terminologie

* Chaque élément d'un dictionnaire est appelé un `item` et est de type [paire](./type_particulier.md#le-type-paire)
* Lorsqu'on parle des `clefs d'un dictionnaire`, on parle de l'ensemble des clefs des paires de ce dictionnaire.
* Lorsqu'on parle des `valeurs d'un dictionnaire`, on parle de l'ensemble des valeurs des paires de ce dictionnaire.

### Syntaxe

* Un dictionnaire commence par une accolade ouvrante `{` et se termine par une accolade fermante `}`.
* Chaque item d'un dictionnaire est séparé par une _virgule_ `,`.

### Particularités

* En plus de pouvoir accéder aux items d'un dictionnaire par leur index (similairement aux listes), on peut accéder à
  une valeur contenue dans le dictionnaire en utilisant la clef qui lui est associée (voir les opérations sur les
  dictionnaires au [_chapitre 2.5.3_](../operateurs/iterables.md))

* Les valeurs d'un dictionnaire peuvent contenir d'*autres dictionnaires*.

* Chaque clef d'un dictionnaire doit être _unique_, mais plusieurs clefs peuvent avoir la même valeur.
    ```
    {"nom": "Jean", "age": 24} ✅
    {"nom": "Jean", "nom", "Marie"} ❌
    ```

### Exemple de dictionnaires:

```
var monDictVide = {}

var notes = {
    "Josianne": 78,
    "Amélie": 100,
    "Pierre": 91,
    "Joseph": 57,
}

var personne = {
    "infos": {"nom": "Bob", "age": 20}, 
    "addresse": "123 rue Imaginaire",
    "liste d'épicerie": ["pommes", "oranges"],
}
```
