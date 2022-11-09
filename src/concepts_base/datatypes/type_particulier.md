# Les types particuliers

Les types particuliers sont les types de données qui ne sont ni primitif ni une collection. Ils ont des significations
spéciales, voilà pourquoi ils méritent d'être traité séparément!

## Le type `iterable`

Le type `iterable` est un type qui englobe les types suivants:

* Le type [`texte`](./types_primitifs.md#le-type-texte)
* Le type [`liste`](./collections.md#le-type-liste)
* Le type [`dict`](./collections.md#le-type-dict)

Si un type est `iterable`, cela signifie qu'il possède certaines opérations particulières (voir les opérations sur
les `iterables` dans le [_chapitre 2.5.3_](../operateurs/iterables.md))

## Le type `tout`

Le type `tout` est un type particulier qui englobe tous les autres types.

## Le type `rien`

Le type `rien` est utile comme type de **retour de fonction** afin de spécifier que la fonction ne retourne aucune
valeur (voir les fonctions au [_chapitre 4_](../../fonctions/fonctions.md)).

En pratique, c'est un synonyme du type `nulType`


