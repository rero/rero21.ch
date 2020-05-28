---
title: "Une version plutôt riche"
publishdate: 2020-06-04
draft: false 
tags: ["rero-ils", "release", "recherche", "circulation", "métadonnées", "affichage"]
slug: une-version-plutot-riche
---

Une nouvelle version de {{< smallcaps "rero ils" >}} a été publiée, plutôt
riche en nouvelles fonctionnalités, ce qui nous fait bien entendu plaisir.
Ci-dessous, un rapide résumé des nouveautés principales. Les notes de version
complètes, mais techniques, en anglais, sont disponibles sur le projet GitHub :
[`v0.9.0`][1].

<!--more-->

## Amélioration de la recherche

Voilà longtemps que l'équipe des bibliothécaires insistait sur ce point et
les [tests des bibliothèques pilotes][2] l'ont confirmé : pour la recherche dans
un catalogue de bibliothèques, on s'attend à l'application par défaut de
l'opérateur booléen `ET`, afin de réduire le bruit, quitte à n'avoir aucun
résultat. C'est désormais chose faite. Par la même occasion, l'ensemble de
l'indexation des données et du fonctionnement de la recherche a été revisité
et les améliorations sont sensibles.

## Des silos fermés

[UCLouvain][3], qui collabore activement au développement de 
{{< smallcaps "rero ils" >}}, avait proposé l'implémentation des *silos 
fermés*, à savoir la possibilité de bloquer les demandes ou de restreindre les
lieux de retrait pour une localisation donnée. Après l'avoir proposé,
[UCLouvain][3] l'a réalisé.

{{< figure src="/img/rero-ils-paging.png" caption="Édition d'une localisation, avec des restrictions sur les lieux de retrait" >}}

## Le blocage manuel des lecteurs et lectrices

Il est désormais possible de bloquer un lecteur ou une lectrice, manuellement.
Une note en texte libre peut être ajoutée pour expliquer la raison du blocage.
La personne bloquée ne peut plus emprunter d'ouvrages ni faire
de demandes. Dans son compte, elle est avertie du blocage et de sa raison.
Le ou la bibliothécaire est également notifié·e lors des transactions de prêt qui
ne sont plus possibles (prêter ou faire une demande pour le lecteur ou la
lectrice).

## Métadonnées et affichage des notices

Le travail d'implémentation du modèle de données continue avec les champs de
description physique des documents : l'importance matérielle, la durée, le
format, les illustrations, les couleurs et les éléments matériels. Ces champs
sont clairement basés sur le standard RDA, avec une granularité plus fine,
alors que {{< smallcaps "marc" >}} regroupait différents types d'informations
au sein d'un même sous-champ. Lors du travail pour afficher ces champs dans la
notice (la vue détaillée des documents), la présentation a été revue et
améliorée : les informations essentielles sont mises en évidence en haut et les
détails bibliographiques complémentaires apparaissent dans un onglet dédié.

{{< video src="new-document-detailed-view" legend="Réorganisation de la notice bibliographique (interface professionnelle)" >}}


[1]: https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v090
[2]: /rero-ils-s-expose-aux-tests/
[3]: https://uclouvain.be/fr/bibliotheques
