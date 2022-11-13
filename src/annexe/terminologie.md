# Lexique

Ici, on retrouve les définitions des termes et concepts utilisés tout au long de l'ouvrage.

## Concept de base

### Langage de programmation

Un langage de programmation, c'est le meilleur compromis que nous ayons trouvé afin de permettre aux humains de dire à
l'ordinateur quoi faire sans que cela soit trop compliqué à comprendre pour les autres humains. En d'autres mots,
c'est un langage, tout comme le français ou l'anglais, qui possède un **ensemble de règles et de contraintes** à
respecter. Cependant, contrairement à la plupart des langages parlés, les règles d'un langage de programmation sont
strictes afin d'éviter, le plus possible, l'ambiguïté.

### Programme

Un programme, c'est le nom qu'on donne à un ensemble de lignes de code qui font une ou plusieurs actions
lorsque exécutées. Par exemple, un programme peut afficher `Bonjour, Monde!` dans la console ou encore envoyer une fusée
sur la Lune! Le terme _programme_ est très large. Ici, il fera référence aux morceaux de code que vous serez invités à
lire tout au long de ce livre.

### Les énoncés

Un énoncé (appelé _statement_ en anglais) est le nom donné à l'action principal réalisé par une _ligne de code_ (un
énoncé peut s'étendre sur plusieurs
lignes, mais cela est rarement le cas). Il ne peut y avoir qu'**un seul énoncé par ligne de code**, mais un énoncé peut
inclure. Contrairement à une expression, un énoncé ne produit aucune valeur après avoir été exécuté.

Ex:

* `lire var monNom` -> ici, l'énoncé est _`lire`_ ayant comme action la déclaration puis la lecture d'une valeur dans
  `nomNom`.
* `var a = 12 + 3` -> ici, l'énoncé est _`déclarer`_ ayant comme action la déclaration de la variable `a` avec la valeur
  donnée par le résultat de l'expression `12 + 3`.

### Les expressions

Une expression est une sous-action qui, une fois évaluée (ou réduite), produit une valeur. Le nombre
maximum d'expressions dépend de l'énoncé dans lequel se retrouve l'expression.

Ex:

* `var a = 12 + 3` -> ici, l'expression est _`additionner`_ ayant comme sous-action `12 + 3` et comme valeur
  résultante, après avoir été évaluée, `15`

### Les blocs de code

Un **bloc de code** est un morceau de code encadré par un énoncé d'ouverture et un énoncé de fermeture.

> Si nous ne sommes pas à l'intérieur d'un bloc de code, on dit qu'on est dans le
> [_bloc de code principal_](#bloc-de-code-principal).

La majorité des blocs de code suivent la syntaxe suivante:

```
<nom_du_bloc> ...
    
    # code à l'intérieur du bloc
    
fin <nom_du_bloc>
```

Ex:

```
afficher "Nous sommes dans le bloc principal"

si vrai  # énoncé d'ouverture du bloc 'si'
    
    afficher "Nous somme dans un bloc 'si'"
    
fin si  # énoncé de fermeture du bloc 'si'

afficher "Nous sommes revenu dans le bloc principal"
```

### Bloc de code *principal*

Nom donné au bloc de code qui englobe tout le programme.

### Une entrée

Entrée: Une _entrée_ (ou _input_ en anglais) est une valeur qui répond aux critères suivants:

1. Elle n'est pas connue du programme avant l'exécution.
2. Elle provient d'une interaction entre une source extérieure et le programme.

### Une sortie