## Opérations sur les types

Les types (comme `entier`, `liste`, `texte`, etc.) sont eux-mêmes des valeurs qui peuvent être manipulées en utilisant
certaines opérations.

### Opération `|`

Cette opération (appelée `ou`) permet de combiner deux types. Le type résultant est compatible avec les deux types
combinés.

Ex:

- `entier | decimal` est compatible autant avec `12.123` qu'avec `-2`
- `liste | entier | texte` est compatible autant avec `69420` qu'avec `[1, 2, 3, "salut"]` et `"mon nom est Mathis"`

