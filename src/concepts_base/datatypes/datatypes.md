# Les types de données

Chaque valeur présente dans AliveScript est d’un certain type de donnée. Ces types ont une double utilité. Dans un
premier temps, les types permettent de facilement classifier les valeurs en catégories, rendant la manipulation de
données plus intuitive. Dans un deuxième temps, ils permettent à AliveScript de s’assurer que certaines opérations sont
valides avant même qu’elles ne soient exécutées.

> Pour voir tous les types de données de manière synthétisée, voir le tableau des types de données dans
> l'[Annexe B](../../annexe/tableau_datatypes.md)

### Les types primitifs

On appelle **type primitif** les types suivants:

* Les [types numériques](./types_primitifs.md#les-types-numriques)
    * Le type [`entier`](./types_primitifs.md#le-type-entier)
    * Le type [`decimal`](./types_primitifs.md#le-type-decimal)
    * Le type [`nombre`](./types_primitifs.md#le-type-nombre)
* Le type [`texte`](./types_primitifs.md#le-type-texte)
* Le type [`booleen`](./types_primitifs.md#le-type-booleen)
* Le type [`nulType`](./types_primitifs.md#le-type-nultype)
* Le type [`paire`](./types_primitifs.md#le-type-paire)
* Le type [`fonctionType`](./types_primitifs.md#le-type-fonctiontype)
* Le type [`structureType`](./types_primitifs.md#le-type-structuretype)

### Les types de collections

On appelle **type de collection** les types suivants:

* Le type [`liste`](./collections.md#le-type-liste)
* Le type [`dict`](./collections.md#le-type-dict)

## Les types particuliers

### Le type `iterable`

Le type `iterable` est un type qui englobe les types suivants:

* Le type [`texte`](./types_primitifs.md#le-type-texte)
* Le type [`liste`](./collections.md#le-type-liste)
* Le type [`dict`](./collections.md#le-type-dict)

Si un type est `iterable`, cela signifie qu'il possède certaines opérations particulières (voir les opérations sur
les `iterables` dans le [_chapitre 2.5.3_](../operateurs/iterables.md))

### Le type `tout`

Le type `tout` est un type particulier qui englobe tous les autres types.

### Le type `rien`

Le type `rien` est utile comme type de **retour de fonction** afin de spécifier que la fonction ne retourne aucune
valeur (voir les fonctions au [_chapitre 4_](../../fonctions/fonctions.md)).

En pratique, c'est un synonyme du type `nulType`


---

> Afin de savoir de quel type est une certaine valeur, il suffit d'utiliser la fonction builtin `typeDe`.
> Ex:
> ```
> afficher typeDe(12)  # entier
> afficher typeDe(-420.69)  # decimal
> afficher typeDe(afficher)  # fonctionType
> ```
