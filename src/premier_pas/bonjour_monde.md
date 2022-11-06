# Bonjour, Monde!

## Écrire son premier programme en AliveScript

Le programme le plus simple à faire en AliveScript permet d'afficher `Bonjour, Monde!`
dans la console.

Pour ce faire, on écrit:

```
afficher "Bonjour, Monde!"
```

Puis on exécute le programme en appuyant sur le

<svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="play-circle" class="svg-inline--fa fa-play-circle fa-w-16 fa-fw fa-2x button-fa-icon" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="currentColor" d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm115.7 272l-176 101c-15.8 8.8-35.7-2.5-35.7-21V152c0-18.4 19.8-29.8 35.7-21l176 107c16.4 9.2 16.4 32.9 0 42z"></path></svg>
<path fill="currentColor" d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm115.7 272l-176 101c-15.8 8.8-35.7-2.5-35.7-21V152c0-18.4 19.8-29.8 35.7-21l176 107c16.4 9.2 16.4 32.9 0 42z"></path>
</svg>

La console devrait alors afficher

```
Bonjour, Monde!
[exécution terminée]
```

Si c'est le cas, félicitation, vous pouvez maintenant ajouter programmeur d'AliveScript à votre C.V.!

## Décortiquer le programme

Malgré l'apparente simplicité de ce qu'on vient de faire, un tel programme ne pourrait pas être
possible sans l'interaction de multiples systèmes.

La première partie (`afficher`) est une **fonction** que nous appelons en lui passant un **argument**
(`"Bonjour, Monde!"`). La fonction `afficher` imprime **l'argument** sur la console. Si les termes
**fonction**, **appeler** et **argument** ne vous sont pas familiers, pas de panique, nous
y reviendrons dans le _chapitre 4_.

La deuxième partie (`"Bonjour, Monde!"`) est une donnée de type **texte** qui représente la phrase
**Bonjour, Monde!**. Afin que cette phrase soit considérée de type **texte** par AliveScript, nous
l'avons mise entre doubles guillemets `"`. Nous verrons le type **texte** plus en détails ainsi que les
différents types de données dans le _chapitre 2.2_.

## C'est quoi _appeler une fonction_?

Non, nous n'avons pas besoin de son numéro de téléphone pour l'appeler, ce terme a une signification
particulière en programmation.

Appeler une fonction, c'est de lui demander d'exécuter une série d'opérations prédéfinies par la fonction en
utilisant les différentes valeurs que nous lui fournissons (ces valeurs sont appelées **arguments**). Dans le cas de la
fonction `afficher`, elle imprime dans la console l'argument qui lui est passé lorsque nous l'appelons.

Nous reviendrons sur la subtilité de l'appel de fonction, ainsi que sur les autres aspects des fonctions,
plus en détails dans le _chapitre 4_.
