# TP Développement Web (CHAMPEAU Loïc et SORROCHE Erwan)

## Réponses aux questions

1. `package-lock.json` se réfère au fichier `package.json` et fixe les versions des dépendances (car il est possible de définir des plages de versions pour les dépendances dans le package) et liste les dépendances transitives (dépendances de dépendances) nécessaires à l'application.
   
2. Le format de 3 chiffres utilisé pour le nommage des versions sur NPM est appelé **Semantic Versioning** (Semver).

3. Une **DevDependency** est une dépendance ajoutée au projet qui, contrairement aux **dependencies** classiques, ne seront pas incluses lors du packaging de l'application.

4. (à faire)

5. `import *` permet d'importer tout les éléments exportés d'un fichier, alors que `import {method}` permet d'importer uniquement les éléments indiqués entre les accolades (s'ils ont bien été exportés dans le fichier cible). Il se peut donc que, par exemple, en utilisant `import *` que l'on se retrouve à importer des éléments dans un fichier qui lui seraient inutiles.

6. Par rapport aux classes ES6, les classes Java peuvent avoir de **"l'overloading"**, c'est a dire avoir plusieurs fois la même méthode mais avec des paramètres différents et des définitions différentes. Les classes ES6 n'ont pas de système d'encapsulation à proprement parler, c'est a dire qu'elles n'ont pas de définition "private" pour les méthodes et les attributs.

7. (à faire)

8. `.bind(this)` permet sur des déclarations de fonctions de call-back de lier la fonction en question à un autre contexte, ici pour donner à la fonction le contexte de l'objet dans laquelle elle est définie (*GameComponent*) et lui donner accès aux attributs de cet objet. Si on supprime `.bind(this)`, le **"this"** fera référence au scope au-dessus, qui est le scope dit **"window"**, le scope global. Il n'est pas utile si l'on utilise une **"arrow function"** car elles récupèrent déjà le contexte du scope dans lequel elles ont été définies.

9. (à faire)

10. Les **promises** permettent de pouvoir effectuer des tâches de manières asynchrone sans avoir besoin de faire appel à des call-backs, qui quand ils deviennent trop nombreux, posent des problèmes de lisibilité du code. Grâce au fait que la méthode `.then()` permette d'effectuer une opération après la fin de la **"promise"** et qu'une promise retourne un autre promise et qu'elles ont donc la possibilité d'être mise à la chaine, elles peuvent parfaitement remplacer les chaines de call-backs.

11. Les mots-clés `async` et `await` sont apparus sous **ES8 (ECMAScript 8)**.

12. La programmation **"Component oriented"** est plus facile à entretenir car elle compartimente l'application par composants, permettant de mieux isoler les changements effectués dans l'application et également les problèmes (si un problème intervient avec une carte, il sera évident d'aller chercher la source dans le composant `card`). Également, les évolutions sont simplifié car les composants sont fait de manière à être réutilisable.

13. (à faire)

14. La fonction `map()` permet de récupéré chaque valeur d'une liste et de la remplacer par une autre suivant une condition donnée.
    Exemple :
```
    map(value => value +2)
```
récupère chaque valeur et lui ajoute 2

15. La fonction `filter()` récupère chaque valeur d'une liste et retire ou non cette valeur de la liste suivant une condition donnée.
    Exemple :
```
    filter(value => value <= 5)
```
récupère chaque valeur et retire celles inférieures à 5

16. la fonction `reduce()` prend 2 paramètres : le premier est une variable qui va contenir le résultat de chaque itération, le second est la variable qui va être itérée. La seconde partie contient l'opération effectuée à chaque itération.
    Exemple :
```
    reduce((sum, value) => sum + value)
```
à chaque itération, un élément de la liste sera ajouté à "sum" et le résultat de cette opération sera stockée dans "sum", "value" est donc ajouté au total de l'opération précédente.

17. Par rapport a `.then()` qui laisse le programme fonctionner durant l'attente d'une réponse, `await` dans une fonction `async` bloque l'execution de la fonction `async` jusqu'à l'obtention d'une réponse.

18. (à faire)
