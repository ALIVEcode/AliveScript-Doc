# Les entrées et les sorties (IO)

Les opérations d'IO (`Input/Output` en anglais, signifiant `entrées/sorties` en français) permettent de rendre un
programme ✨interactif✨!

## Mais c'est quoi des entrées et des sorties?

### Entrée

Une _entrée_ (ou _input_ en anglais) est une valeur qui répond aux critères suivants:

1. Elle n'est pas connue du programme avant l'exécution.
2. Elle provient d'une source extérieure au programme ou d'une interaction entre une source extérieure et le
   programme.

> Attention!  
> Une valeur générée aléatoirement (comme avec la fonction `aleatoire`) n'est PAS considérée comme une entrée. En
> effet,
> même si elle satisfait le critère `1.` (ne pas produire une valeur connue avant l'exécution), elle ne satisfait pas
> le critère `2.` puisqu'elle ne provient pas d'une source extérieure.

### Sortie

Une _sortie_ (ou _output_ en anglais) est une valeur qui répond aux critères suivants:

1. Elle agit (directement ou indirectement) sur un composant externe au programme.
2. L'interaction avec le composant externe ne change pas la valeur (interaction unidirectionnelle).

## L'énoncé d'entrée `lire`

L'[énoncé](../annexe/terminologie.md#les-énoncés) `lire` (peu importe la variation) affiche un message et demande à
l'utilisateur d'entrer une valeur puis enregistre cette valeur dans une variable (pour en savoir plus sur les variables,
voir [_chapitre 2.4_](./variables.md))

Les différentes variations de l'énoncé `lire` (pour la signification des symboles,
voir [Annexe F](../annexe/legende_syntaxe.md)):

* Lire: `lire [var] <nom_var>[, <message>]`
    * Si `var` est inclus, l'énoncé déclare la variable en plus de lui affecter la valeur entrée par l'utilisateur.
    * Si `, <message>` est inclus, le message demandant d'entrée une valeur est celui spécifié par `<message>` au lieu
      d'être le message par défaut (`Entrez une valeur`).

* Lire dans: `lire <fonction|type> dans [var] <nom_var>[, <message>]`
    * La valeur entrée par l'utilisateur est passée comme argument dans un appel à la fonction et c'est la
      nouvelle valeur retournée par la fonction qui est utilisé dans l'affectation de la variable.
    * Si `var` est inclus, l'énoncé déclare la variable en plus de lui affecter la valeur entrée par l'utilisateur.
    * Si `, <message>` est inclus, le message demandant d'entrée une valeur est celui spécifié par `<message>` au
      lieu d'être le message par défaut (`Entrez une valeur`).

## Les sorties les plus communes

* La fonction `afficher`:
    * Elle prend une valeur et la fait agir sur le terminal (en l'affichant). La valeur passée à la
      fonction `afficher` est donc une valeur de sortie.

* La fonction `notif`:
    * Similairement à la fonction `afficher`, `notif` prend une valeur et la fait agir sur le site web (en
      affichant une notification). La valeur passée à la fonction `notif` est donc une valeur de sortie.



