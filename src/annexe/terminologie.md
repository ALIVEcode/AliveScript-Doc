# Terminologie

Ici, on retrouve les définitions des termes et concepts utilisés tout au long de l'ouvrage.

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
