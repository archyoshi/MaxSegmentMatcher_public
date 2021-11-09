### Description

Certaines langues, comme le chinois, le japonais et le thaï, n'ont pas d'espaces entre les mots. Cependant, la plupart
des tâches de traitement des langues naturelles, comme le marquage des parties du langage, nécessitent des textes dont
les mots sont segmentés. Un algorithme simple et raisonnablement efficace pour segmenter une phrase en ses mots
composants est appelé "MaxMatch".

### MaxMatch

MaxMatch commence au premier caractère d'une phrase et essaie de trouver le mot valide le plus long à partir de ce
caractère. Si aucun mot n'est trouvé, le premier caractère est considéré comme le plus long "mot", quelle que soit sa
validité. Afin de trouver le reste des mots, MaxMatch est ensuite invoqué récursivement sur tous les caractères restants
jusqu'à ce qu'il n'en reste plus. Une liste de tous les mots qui ont été trouvés est retournée.

Ainsi, pour la chaîne "plastiquevert", "plastique" est trouvé car "plastiquevert" n'est pas un mot valide, pas plus
que "plastiquever" ou "plastiquev". Ensuite, MaxMatch est appelé sur "vert", et "vert" est trouvé. Le résultat est la
liste ["plastique", "vert"] dans cet ordre.

### Objectif

Écrivez MaxMatch, qui prend en entrée une chaîne alphanumérique, sans espace et en minuscules et renvoie une liste de
chaînes de caractères qui sont tous les mots trouvés, dans l'ordre où ils ont été trouvés.

_Quelques exemples:_

- "plastiquevert" &#8594; ["plastique", "vert"]
- "ghjtyu" &#8594; ["g", "h", "j", "t", "y", "u"]
- "uevert" &#8594; ["u", "e", "vert"]

La liste des mots a été récupérée sur une page wikipedia et se trouve dans le fichier [repo.txt](./source/repo.txt)

Good luck :)
