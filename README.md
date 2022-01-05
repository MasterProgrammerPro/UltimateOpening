# Implémentation de l'opérateur Ultimate Opening avec Maxtree

Projet de mise en œuvre d'un opérateur d'ouverture finale à l'aide de Maxtree.

Une description détaillée de la mise en œuvre de la méthode est disponible sur ce lien : 
https://people.cmm.minesparis.psl.eu/users/marcoteg/cv/publi_pdf/jonathan/fabrizio_marcotegui_ismm09_published.pdf

## Max-tree

L'article décrit une façon d'implémenter l'algorithme Max-tree, qui est plus rapide que la version originale. Dans notre cas, nous avons utilisé l'implémentation de cet algorithme dans la bibliothèque scikit-image, car l'idée principale concernait plutôt l'implémentation de l'ouverture ultime. De cette façon, nous avons accéléré le processus de travail sur le projet.

Lien vers l'implémentation max-tree utilisée: https://scikit-image.org/docs/dev/auto_examples/developers/plot_max_tree.html

## Ultimate Opening

Ultimate Opening est un opérateur qui accentue les zones les plus contrastées d'une image sans avoir besoin de paramètres.

Dans ce cas, nous avons implémenté une version de cet opérateur en utilisant maxtree. La fonction principale qui effectue le calcul est compute_uo. Pour les détails de la fonction, voir les commentaires du code.

## Tests 

La méthode a été testée sur 2 images :

* Photo d'une rue avec différents éléments
* Une photographie en noir et blanc avec différents petits détails présentant un grand contraste entre eux (drapeau, lettres, etc.)
* Image créée, avec des éléments de base

Les données d'image ont été extraites de l'article pour une comparaison approximative des résultats. D'autres images peuvent également être utilisées pour les tests

<img width="964" alt="jarray reverse exampl" src="https://github.com/OOps717/Path-tracing-Monte-Carlo/blob/master/Images/Screenshot%20from%202022-01-03%2011-20-08.png">

## Utilisation

Pour tester la méthode, changez le chemin vers l'image dans la ligne de code ``` img = io.imread('./opening_test.png', as_gray = True) * 255 ```
