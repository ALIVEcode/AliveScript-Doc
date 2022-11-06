# Les commentaires

Les commentaires se présentent sous plusieurs formes, mais ils ont tous un point en commun: ils permettent d'annoter le
code
sans impacter son fonctionnement.

Les commentaires sont en effet **ignorés** lors de l'exécution.
<!-- (sauf dans un cas particulier que nous verrons plus tard) par AliveScript -->

## Les commentaires **simple ligne**:

Syntaxe: `# commentaire`

Utilité: Ce type de commentaire est utile lorsque l'information tient sur _une seule_ ligne. Ils peuvent être situés à
la fin d'une ligne tout comme au début d'une ligne.

Ex:

```
afficher "Bonjour!"  # ce code affiche Bonjour!

# ce code va afficher Bonjour!
afficher "Bonjour!"
```

## Les commentaires **multilignes**:

Syntaxe:

- ouverture: `(:`
- fermeture: `:)`

Utilité: Ce type de commentaire est utile lorsque l'information s'étend sur _plusieurs_ lignes. Même s'ils peuvent être
situés aux mêmes endroits que les commentaires simple ligne, il est recommandé de les séparer des lignes de code.

Ex:

```
(:  
 salut je suis un commentaire  
 sur plusieurs  
 lignes  
 et la prochaine ligne
 va afficher
 Bonjour!
:)
afficher "Bonjour!"
```

## Les commentaires de **documentation**:

Syntaxe:

- ouverture: `(-:`
- fermeture: `:-)`

Utilité: Ce type de commentaire est utilisé au-dessus de **fonctions** (voir _chapitre 4_) et de **structures** (voir
_chapitre_ 5) afin de spécifier à quoi elles servent. Par convention, chaque ligne d'un commentaire de documentation
commence par un espace suivi par un `-` (de manière à les aligner avec la syntaxe d'ouverture et de fermeture).

Ex:

```
(-:
 - Cette fonction additionne deux nombres et retourne le résultat
 - @param num1: le premier nombre
 - @param num2: le deuxième nombre
 - @retourne la somme deux deux nombres
:-)
fonction additionner(num1: nombre, num2: nombre) -> nombre
    retourner num1 + num2
fin fonction
```
