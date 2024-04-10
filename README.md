# TP Développement Web (CHAMPEAU Loïc et ROUBAUD Mathieu)

## Réponses aux questions

1. `package-lock.json` se réfère au fichier `package.json` et fixe les versions des dépendances (car il est possible de définir des plages de versions pour les dépendances dans le package) et liste les dépendances transitives (dépendances de dépendances) nécessaires à l'application.
   
2. Le format de 3 chiffres utilisé pour le nommage des versions sur NPM est appelé **Semantic Versioning** (Semver).

3. Une **DevDependency** est une dépendance ajoutée au projet qui, contrairement aux **dependencies** classiques, ne seront pas incluses lors du packaging de l'application.

4. Une `closure` est une fonction qui se souvient de l'environnement dans laquelle elle à été créée, c'est-à-dire une fonction qui accès à ses variables internes, à celles de sa fonction parente et également celles du scope global. Une `IIFE` est une fonction qui est immédiatement appelée à sa définition (Immediately Invoked Function Expressions). Les `IIFE` était un moyen de créer des scopes privés avant l'arrivée des `ES Modules`.

5. `import * as toto` permet d'importer tout les éléments exportés d'un fichier sous un nouveau nom (ici "toto"), alors que `import {method}` permet d'importer uniquement les éléments indiqués entre les accolades (s'ils ont bien été exportés dans le fichier cible). Il se peut donc que, par exemple, en utilisant `import * as toto` que l'on se retrouve à importer des éléments dans un fichier qui lui seraient inutiles.

6. Par rapport aux classes ES6, les classes Java peuvent avoir de **"l'overloading"**, c'est a dire avoir plusieurs fois la même méthode mais avec des paramètres différents et des définitions différentes. Les classes ES6 n'ont pas de système d'encapsulation à proprement parler, c'est a dire qu'elles n'ont pas de définition "private" pour les méthodes et les attributs.

7. Une variable `var` possède un scope limité à la fonction dans laquelle elle est définie et dans le scope global si elle n'est pas dans une fonction. Une variable `let` est définie dans la structure dans laquelle elle est définie (par exemple, un `if`,`while` ou `for` et dans le scope du module si elle n'est pas dans une structure.

8. `.bind(this)` permet sur des déclarations de fonctions de call-back de lier la fonction en question à un autre contexte, ici pour donner à la fonction le contexte de l'objet dans laquelle elle est définie (*GameComponent*) et lui donner accès aux attributs de cet objet. Si on supprime `.bind(this)`, le **"this"** fera référence au scope au-dessus, qui est le scope dit **"window"**, le scope global. Il n'est pas utile si l'on utilise une **"arrow function"** car elles récupèrent déjà le contexte du scope dans lequel elles ont été définies.

9. Le symbole `@` dans `@Babel` indique à NPM que les packages recherchés font parties du scope Babel dans la banque de donnée de NPM, permettant d'éviter des conflits de nommage entre différents "package" dans la banque de donnée NPM.

10. Les **promises** permettent de pouvoir effectuer des tâches de manières asynchrone sans avoir besoin de faire appel à des call-backs, qui quand ils deviennent trop nombreux, posent des problèmes de lisibilité du code. Grâce au fait que la méthode `.then()` permette d'effectuer une opération après la fin de la **"promise"** et qu'une promise retourne un autre promise et qu'elles ont donc la possibilité d'être mise à la chaine, elles peuvent parfaitement remplacer les chaines de call-backs.

11. Les mots-clés `async` et `await` sont apparus sous **ES8 (ECMAScript 8)**.

12. La programmation **"Component oriented"** est plus facile à entretenir car elle compartimente l'application par composants, permettant de mieux isoler les changements effectués dans l'application et également les problèmes (si un problème intervient avec une carte, il sera évident d'aller chercher la source dans le composant `card`). Également, les évolutions sont simplifié car les composants sont fait de manière à être réutilisable.

13. Le programmation fonctionnelle est une méthode de programmation dont le but est de construire un programme par l'application et la composition entre elles. Par exemple, la bibliotèque `stream` permet de composer des méthodes sur des listes pour effectuer des opérations sur elle-même.

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

18. le caractère `_` dans un fichier Sass indique que le fichier en question est un fichier dit "partiel", c'est à dire qu'il ne sera pas transformer immédiatement en fichier CSS mais qu'il contient plutôt des éléments qui seront référencés dans d'autres fichiers Sass.
