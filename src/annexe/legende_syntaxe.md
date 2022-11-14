# Légende des symboles utilisés dans les énoncés et les expressions

| Symbole                           | Signification                                                                                 | Exemple                                                                     | 
|-----------------------------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [...]                             | Ce qui est entre les deux crochets est optionnel                                              | `abc[, ceci]`:<br/>`abc, ceci` OU `abc`                                     |
| \<...>                            | Ce qui est écrit entre les `< >` sert à indiquer par quoi il faut les remplacer dans le code. | `<nom_var>`:<br/>`nom`, `maVariable`, `foo`, etc.                           |
| <code>&#124;</code>               | Sépare des variations possibles                                                               | <code>[var&#124;const]</code>:<br/>`var` OU `const`                         |
| `*` après un des symboles spécial | On peut le répéter 0 fois et plus.                                                            | `<valeur> [+ <valeur>]*`:<br/>`10`, `12 + 2`, `34 + 6 + 5`, etc.            |
| `+` après un des symboles spécial | On peut le répéter 1 fois et plus.                                                            | `<valeur> [+ <valeur>]+`:<br/> `12 + 2`, `34 + 6 + 5`, etc. (mais pas `10`) |
| ...                               | Valeur littérale                                                                              | `lire dans`:<br/>`lire dans`                                                |

### Exemples complets

Description du bloc `si`. `<condition>` sert à indiquer qu'il faut la remplacer par une expression qui sera convertie en
booléen. Le `alors` est optionnel.

```
si <condition> [alors]
    # code dans le bloc si
[sinon si <condition> [alors]
    # code dans le bloc sinon si
]*
[sinon
    # code dans le bloc sinon
]
fin si
```

```
var age = 20
si age >= 18 alors
    afficher "Tu es majeur."
sinon si age >= 13
    afficher "Tu es un adolescent."
sinon si age >= 3
    afficher "Tu es un enfant."
sinon
    afficher "Tu es un bébé."
fin si
```
