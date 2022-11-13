# Les types de données

Un type, c'est une manière de catégoriser des données selon certaines propriétés.

Chaque donnée présente dans AliveScript est associée directement à un type de donnée. Ces types ont une double utilité:

1. Permettre de facilement classifier les valeurs en catégories.
2. Permettre à AliveScript de s’assurer que certaines opérations sont valides avant même qu’elles ne soient exécutées.

> Astuce 🔎  
> Pour voir tous les types de données de manière synthétisée, voir le tableau des types de données dans
> l'[Annexe B](../../annexe/tableau_datatypes.md)

### Liste des types primitifs

[Cliquez ici](types_primitifs.md) pour en savoir plus sur les types primitifs.

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

### Liste des types de collections

[Cliquez ici](collections.md) pour en savoir plus sur les types de collections.

On appelle **type de collection** les types suivants:

* Le type [`liste`](./collections.md#le-type-liste)
* Le type [`dict`](./collections.md#le-type-dict)

## Liste des types particuliers

On appelle **type particulier** les types suivants:

* Le type [`iterable`](./type_particulier.md#le-type-iterable)
* Le type [`tout`](./type_particulier.md#le-type-tout)
* Le type [`rien`](./type_particulier.md#le-type-rien)
* Le type [`paire`](./type_particulier.md#le-type-paire)
  <br>

---

## Rappel pour ceux qui s'y connaissent

Afin de savoir de quel type est une certaine valeur, il suffit d'utiliser la fonction builtin `typeDe`.
Ex:

```
afficher typeDe(12)  # entier
afficher typeDe(-420.69)  # decimal
afficher typeDe(afficher)  # fonctionType
```
