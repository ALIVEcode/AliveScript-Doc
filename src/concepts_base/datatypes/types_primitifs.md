# Les types primitifs

Les types primitifs sont les blocs légos

## Les types numériques

AliveScript supporte 2 types numériques (`entier` et `decimal`) ainsi qu'un type englobant les deux (`nombre`).

### Le type `entier`

On écrit le nombre simplement le nombre entier.
*On peut mettre un `-` devant pour le rendre négatif*.

Ex:

```
42069
1290
-1232
-123456
```

### Le type `decimal`

Il existe 3 façons d'écrire un nombre décimal:

1. On écrit un `.` entre deux nombres entiers.
2. On écrit un `.` devant un nombre entier (signifie `0.`).
3. On écrit un nombre entier suivi d'un `.` (signifie `.0`).

*On peut mettre un `-` devant pour le rendre négatif*.

Ex:

```
0.123
.1425
9192.
-0.1234
```

### Le type `nombre`

Le type `nombre` englobe les types `entier` et `decimal`, c'est-à-dire qu'une valeur de type `nombre` est soit
un `entier`
, soit un `decimal`.

Autrement dit, le type `nombre` est synonyme de `entier | decimal` (voir les opérations sur les types [_chapitre
2.2.3_](./operations.md))

## Le type `texte`

On met des doubles guillemets (`"`) ou des simples guillemets (`'`) de part et d'autre du texte.

_Le symbole choisit doit être le même au début et à la fin du texte._

Ex:

```
"abc" ✅ 
'def' ✅  
"je vous dit bonjour si je le veux!" ✅ 
"ce n'est pas valide' ❌ 
```

## Le type `booleen`

Type représentant le concept de vérité. Les booléens sont définis par les mots clefs `vrai` et `faux`.

## Le type `nulType`

Ce type est défini par le mot clef `nul` et représente l'absence de valeur. De ce fait, tous les autres types acceptent
la valeur `nul`, mais le contraire n'est pas vrai (ex: le type `entier` accepte la valeur `nul`, mais le type `nulType`
n'accepte que la valeur `nul`).

## Le type `fonctionType`

Ce type englobe toutes les fonctions (comme `afficher`, `typeDe`, `tailleDe`, etc.). Pour en savoir plus sur les
fonctions, voir le [_chapitre 4_](../../fonctions/fonctions.md)

## Le type `structureType`

Ce type englobe toutes les structures. Pour en savoir plus sur les structures, voir le
[_chapitre 5_](../../structures/structures.md)

**Attention, le type d'une structure n'est pas le même type que l'instance d'une structure!!**
