---
title: "Deux versions conséquentes"
date: 2020-04-20T06:20:38+02:00
publishdate: 2020-04-23
draft: false 
tags: ["rero-ils", "release"]
---

On assiste à une accélération de l'espace temps à RERO,
tout particulièrement dans le projet RERO ILS, et dans
cette précipitation, nous avons « oublié » de vous prévenir que deux nouvelles
versions ont été publiées !

Ci-dessous, une synthèse des apports de ces versions est proposée, mais les
notes détaillées sont accessibles par les liens suivants :

- [`v0.6.0`](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v060)
- [`v0.7.0`](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v070)

<!--more-->

## La version `v0.6.0`

La version `v0.6.0` (et sa petite sœur `v0.6.1`, qui n'est qu'un correctif
comme [son numéro de version l'indique](https://semver.org "Explications du
semantic versioning")) sépare l'interface publique de l'interface
professionnelle. La première, accessible à tout le monde avec ou sans
authentification, comprend le catalogue collectif et les catalogues des
organisations, à quoi s'ajoute le compte des lecteurs et des lectrices et les
actions qui leur sont proposées, par exemple demander un exemplaire. La seconde
donne accès à l'ensemble des actions effectuées par les professionnel·les, que
ce soit la recherche dans le catalogue, le catalogage ou le paramétrage.

Cette séparation logique est en partie la conséquence de l'introduction dans la
version `v0.3.0`[^1] des vues par organisation. Il devenait difficile de
définir et de présenter clairement les actions possibles par tel·le
professionnel·le sur telle vue particulière, ou les informations à destination
d'un visiteur quelconque ou d'une lectrice connectée. Par ailleurs,
l'interface professionnelle gagne à être dynamique, afin d'éviter de recharger
la page après chaque action, alors que l'interface publique est plus aisément
indexée par les moteurs de recherche si les pages sont statiques, ce qui est
pertinent pour les notices bibliographiques. Enfin, ce choix
permet de partager une partie de l'interface professionnelle entre les projets
RERO ILS et [SONAR](https://sonar.ch)
et, ainsi, de mutualiser l'effort de développement[^2].

Le développement de la `v0.6.0` a été en bonne partie guidé par la réalisation
des [ateliers](/tags/ateliers) et de la mise en place d'une instance spécifique
pour les [tests des bibliothèques pilotes](/rero-ils-s-expose-aux-tests). De ce
point de vue, il est désormais possible de personnaliser les vues des
différentes organisations par une couleur spécifique de l'entête et un logo.
Mais surtout, les processus de migration ont été définis et développés, afin de
de récupérer les données réelles de Virtua pour un site RERO.

L'interface du module de prêt a été revisitée et présente désormais plus
d'information sur les événements de circulation lors des retours d'exemplaires
demandés, en retard ou en transit. Le ou la bibliothécaire a maintenant une vue
unifiée du compte du lecteur ou de la lectrice, en différents onglets :
exemplaires empruntés, demandes, frais, informations personnelles. Du côté de
l'interface publique, le compte gagne également en fonctionnalités avec le
renouvellement des emprunts, l'accès à l'historique et l'annulation des
demandes.

Le travail continue du côté du modèle de données avec les zones de publication
et d'édition, ainsi qu'un éditeur supportant l'imbrication de champs sur quatre
niveaux ou plus. Enfin, le module d'acquisition a été commencé avec l'ajout des
années fiscales, des comptes, commandes, lignes de commandes et fournisseurs.

## La version `v0.7.0`

Désormais, la ou le bibliothécaire est en  mesure de placer une demande sur un
exemplaire pour un lecteur ou un lectrice, comme le montre l'animation
ci-dessous. Les professionnel·les disposent d'un onglet des frais des lecteurs
et lectrices plus étoffé avec la possibilité de payer partiellement ou
complètement des frais, de les annuler, de les indiquer comme litigieux ou,
à l'inverse de résoudre un litige. Un historique détaillé est proposé pour les
frais, avec le détail de tous les événements. Ces frais sont générés
automatiquement lorsqu'un prêt a dépassé l'échéance de retour. Ils pourront
également être liés à d'autres services de la bibliothèque, comme les
photocopies, le prêt entre bibliothèque, des abonnements ou dans le cas
d'exemplaires endommagés ou perdus.

{{< video src="request_as_a_librarian" legend="Placer une demande pour un lecteur ou une lectrice" >}}

Du côté du modèle de données, un travail complexe a été réalisé pour le titre et
les transformations nécessaires pour passer du MARC au JSON, ainsi que sur les
adresses URL. Enfin, un wiki a été ajouté afin de rédiger en ligne l'aide
professionnelle.

[^1]: Voir la [note de
  version](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v030).
[^2]: Pour celles et ceux que les dessous du capot intéressent, ce changement
 s'est traduit par la création de deux autres dépôts sur GitHub :
 [ng-core](https://github.com/rero/ng-core), un projet angular qui rassemble
 ce qui est commun à RERO ILS et SONAR, et [rero-ils-ui]
 (https://github.com/rero/rero-ils-ui), également un
 projet angular qui implémente la version RERO ILS de
 l'interface professionnelle.
