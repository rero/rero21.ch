---
title: "Catalogage et indexation dans RERO ILS"
date: 2021-09-23T16:54:32+02:00
publishdate: 2021-09-30
draft: false
tags: ["catalogage", "RDA", "RDA-DACH", "IdRef", "GND", "RERO RAMEAU", "LRM"]
slug: catalogage-et-indexation-dans-rero-ils
---

Avec RERO ILS,  le catalogage devient plus « user friendly » et innovant :
abandon du MARC pour des champs avec des libellés en langage naturel, adoption
de RDA et d'un fichier d'autorité multilingue développé par RERO+ et qui
s'appuie sur VIAF.

<!--more-->

## Principes

RERO ILS fonctionne avec un catalogue collectif mutualisé et alimenté par
l'ensemble des bibliothèques du réseau RERO+. De ce fait, pour garantir la
cohérence et l'homogénéité du catalogue, mais aussi pour faciliter
l'interopérabilité avec nos partenaires suisses comme SLSP ou Renouvaud, un
socle de règles communes a été mis en place :

- Adoption de la norme de catalogage RDA avec profil d'application germanophone
  DACH ;
- Adoption des autorités IdRef pour les noms propres (chaque autorité sert
  comme ATC/matière) ;
- Utilisation du fichier d'autorité virtuel multilingue MEF, développé par
  RERO+ et intégrant les autorités IdRef (francophones), GND (germanophones) et
  le référentiel RERO RAMEAU pour les sujets noms communs.

## Groupes de travail en catalogage et indexation

Le groupe *RERO ILS metadata* gère le passage à RERO ILS et l'évolution des
règles.

Le groupe *Indexation romande commun RERO+/SLSP* gère l'indexation romande post
coordonnée basée sur les référentiels RERO RAMEAU et IdRef.

## Documentation de référence

La ressource de référence pour les règles de description bibliographique est le
[RDAtoolkit][1]. Son accès est restreint. La documentation des [champs RERO
ILS][2] pour le catalogage s'en inspire et fournit les informations
essentielles.

La documentation pour l'indexation romande est disponible sur
<https://www2000.rero.ch>.

## Format et modèle des données

Le format natif de RERO ILS est le [JSON][3]. C'est une différence majeure
avec le passé, puisque la structuration MARC en vigueur dans Virtua, a été
abandonnée. RERO ILS peut importer et exporter des données MARC.

Le modèle choisi est basé sur une entité *Document* intégrant les
entités *Manifestation*, *Expression* et *Œuvre* du modèle FRBR/LRM, enrichie
de liens vers des autorités MEF (personnes, collectivités, titres, lieux,
concepts RERO RAMEAU, etc) ou vers d'autres notices bibliographiques. À terme,
RERO+ vise à appliquer le modèle [LRM][4] complet à RERO ILS.

## Formulaire de catalogage

{{< figure src="/img/editor.png"
    caption="Formulaire de catalogage de RERO ILS"
    alt="Formulaire HTML en 3 colonne, pour sélectionner les champs à afficher, pour éditer et pour naviguer." >}}

Le formulaire contient principalement des champs et sous-champs dont les
intitulés sont des éléments issus ou inspirés de RDA. Il est ainsi
beaucoup plus proche de RDA que ne l'est MARC qui a dû être adapté tant
bien que mal à ces nouvelles règles. Ce formulaire va encore être
amélioré dans les mois qui viennent.

[1]: https://www.rdatoolkit.org/
[2]: https://bib.rero.ch/help/catalogage/liste-champs/
[3]: https://fr.wikipedia.org/wiki/JavaScript_Object_Notation
[4]: https://fr.wikipedia.org/wiki/Modèle_de_référence_IFLA_pour_les_bibliothèques

