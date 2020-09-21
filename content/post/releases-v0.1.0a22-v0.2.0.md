---
title: "Deux nouvelles versions"
date: 2019-06-03T08:33:41+02:00
publishDate: 2019-07-10
draft: false 
tags: ["rero-ils", "release"]
---

Depuis la [Journée RERO](https://www.rero.ch/page.php?section=communique&pageid=reroday2019_fr) de mars 2019, deux versions de RERO ILS ont été publiées. Elles apportent à la fois une consolidation de l'existant, le début du support du modèle consortial, une amélioration du paramétrage du moteur de recherche et la mise en place des notifications en lien avec le prêt.

Les notes de version sont les suivantes :

- https://github.com/rero/rero-ils/releases/tag/v0.1.0a22
- https://github.com/rero/rero-ils/releases/tag/v0.2.0

<!--more-->

## v0.1.0a22, *Consolidation and consortium features*

### Accent sur la qualité du code

Cette version ponctue le sprint 17 qui avait parmi ses objectifs la résolution du plus grand nombre possible de problèmes identifiés (les [*issues* GitHub](https://github.com/rero/rero-ils/issues)), ainsi que l'amélioration de la qualité du code en augmentant sa couverture par des [tests unitaires](https://fr.wikipedia.org/wiki/Test_unitaire) et en s'assurant de mieux le documenter. À la fin du sprint, la couverture du code par les tests est passée de 77 à 89 % (elle dépasse aujourd'hui les 91 %) et il ne restait plus de partie de code non commentée. Enfin, 11 *issues*, dont on trouve la liste à la fin de la [note de version](https://github.com/rero/rero-ils/releases/tag/v0.1.0a22), ont été résolues.

### Organisations multiples : RERO ILS devient *multi-tenant*

En plus d'améliorations apportées à l'interface utilisateur, professionnelle ou non, et au module de prêt, le support du modèle consortial a été implémenté. Par *modèle consortial*, il faut comprendre l'existence de plusieurs **organisations**, comprenant le plus souvent plusieurs **bibliothèques**, elles-mêmes regroupant plusieurs **localisations**. L'existence de plus d'une organisation dans RERO ILS suppose que les données et les actions de chacune d'entre elles soient correctement isolées et traitées.

### Meilleure intégrations d'ebooks

Parallèlement, la collecte des métadonnées des *ebooks* de la plateforme *Cantook*  pour intégration dans le catalogue a été réécrite afin d'interroger directement l'API du fournisseur et d'obtenir des données de meilleure qualité, notamment la langue du document et les sujets.

## v0.2.0, *Search and notifications*

### Amélioration du moteur de recherche

Le sprint 18 s'est concentré sur l'amélioration de la recherche et l'extension des notifications liées au prêt. Concernant le moteur de recherche, un examen plus approfondi a été réalisé sur les champs à indexer et la manière de traiter le texte avant indexation (comme la **suppression des accents et des marques du pluriel**), sur la base des types de recherche désirées selon les cas. En effet, on ne cherche pas de la même façon dans les documents que dans le fichier des lecteurs et des lectrices.

Ensuite, il s'agit d'améliorer l'ordre d'affichage des résultats, avec par défaut un affichage descendant du plus au moins pertinent. Une **pondération des champs** a aussi été ajoutée, par exemple pour donner plus d'importance à un résultat contenant le mot recherché dans le titre plutôt que dans une note.

### Notifications liées au prêt

Du côté des notifications, une nouvelle ressource (un type d'objet à part entière) a été créée dans RERO ILS, afin de les gérer[^1]. Il s'agit d'envoyer une notification (pour l'instant par e-mail et en anglais uniquement, mais [la suite est déjà prévue](https://tree.taiga.io/project/rero21-reroils/us/703)), au lecteur ou à la lectrice, par exemple lorsque le livre demandé l'attend au bureau du prêt, ou que l'échéance de retour des documents empruntés approche.

### Rôles professionnels étoffés

À ces deux points s'ajoute l'implémentation d'un nouveau rôle, **bibliothécaire système**, aux deux rôles déjà existants, **bibliothécaire** et **lecteur**. Les permissions de ces différents rôles ont étés définies ou redéfinies selon les cas pour tenir compte du modèle consortial simple. Le rôle *bibliothécaire* a en général des droits au niveau d'une bibliothèque, alors que celui de *bibliothécaire système* voit ses droits étendus à toute l'organisation, mais pas au-delà. C'est là le début d'une gestion un peu plus réaliste des droits au sein de notre nouveau système.

### Formalisme

Enfin, dès cette publication, le numéro de version suit les recommandations du [*Semantic versioning*](https://semver.org), afin d'être plus explicite sur la valeur d'une *release*. En conséquence, le numéro de version est passé de `v0.1.0a22` à `v0.2.0`. Il s'agit toujours d'une version en cours de développement actif, puisque le premier chiffre est à zéro. C'est donc une nouvelle version mineure (le deuxième chiffre change). À noter que depuis cette publication, un souci dans la génération des données d'exemple a dû être corrigé, ce qui a donné lieu à des publications de correctifs, les `v0.2.1`, `v0.2.2` et `v0.2.3`.

### Pour tester et s'informer

La dernière version publiée est comme toujours disponible publiquement sur [ils.test.rero.ch](https://ils.test.rero.ch), ainsi qu'une page d'aide succincte, en anglais sur le [wiki du projet GitHub](https://github.com/rero/rero-ils/wiki/Public-demo-help), où vous trouverez notamment les identifiants et mots de passe des comptes disponibles pour tester le site de démonstration.   
Si vous constatez des problèmes, ce qui est vraisemblable, n'hésitez pas à nous contacter au moyen des canaux suivants :

- la *room* Gitter [reroils](https://gitter.im/rero/reroils),
- les [*issues* GitHub](https://github.com/rero/rero-ils/issues),
- l'[email](mailto:info@rero.ch),
- le compte Twitter [@rero_centrale](https://twitter.com/rero_centrale).


[^1]: La création de cette ressource a été mise à profit afin d'utiliser une nouvelle version du module `invenio-records` qui permet la création d'un table par ressource. 
