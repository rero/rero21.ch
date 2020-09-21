---
title: "Deux sprints, une version"
publishdate: 2020-09-28
draft: false
tags: ["rero-ils", "release", "tests", "bibliothèques-pilotes", "autorités"]
slug: deux-sprints-une-version
---

L'équipe RERO ILS a travaillé successivement ces deux derniers mois sur les sprints [33](https://tree.taiga.io/project/rero21-reroils/taskboard/sprint-33-108) et [34](https://tree.taiga.io/project/rero21-reroils/taskboard/sprint-34-93) du développement. Ce travail donne naissance à une version `v0.12.0` riche en nouveautés et déployée pour la deuxième phase de tests des bibliothèques pilotes, qui a débuté fin septembre. Voici les modifications les plus importantes de cette version dont les notes complètes sont consultables sur Github [`v0.12.0`](https://github.com/rero/rero-ils/blob/dev/RELEASE-NOTES.rst#v0120).

<!--more-->

## Lien aux autorités-personnes en contribution

Un nouveau champ `contribution` vient remplacer le champ `author` dans le catalogage des documents afin d'être adapté aux normes actuelles, en particulier les règles RDA. Les documents sont mis en relation avec des agents contributeurs, dont les autorités proviennent de référentiels vérifiés (IdRef et GND). Le rôle de chaque agent dans la production d'un document est également indiqué avec un code de relation RDA. Si l'autorité n'est pas présente dans les référentiels, on peut aussi l'enregistrer manuellement sous forme de chaîne de caractères dans ce même champ.

{{< figure src="/img/contribution.jpg" caption="Le champ `contribution` nouvellement ajouté au modèle de données du document">}}

## Densité de la circulation sous contrôle

Un grand travail de l'ombre a été effectué sur le backend du module de circulation, afin de résoudre les problèmes constatés lors des premiers tests-pilotes du mois de mars 2020 et implémenter correctement toutes les [actions de circulation](https://github.com/rero/rero-ils/blob/dev/doc/circulation/actions.md) identifiées, d'une part. D'autre part, des tests automatisés ont également été développés afin de pouvoir contrôler le bon fonctionnement de ce module à chaque nouvelle version et repérer d'éventuelles erreurs inattendues lorsque des travaux seront effectués sur d'autres parties du logiciel.

## Besoin d'aide ?

Avec l'évolution constante des fonctionnalités de RERO ILS, il était nécessaire de documenter son fonctionnement pour l'utilisateur·trice final·e. C'est désormais chose faite avec une [plateforme d'aide](https://ils.test.rero.ch/help/home/) accessible depuis les interfaces professionnelle et publique de RERO ILS. Cette application propose sur une même plateforme, l'aide publique et l'aide professionnelle de RERO ILS afin de guider les utilisateurs·trices et d'accompagner leur formation à l'outil.

{{< figure src="/img/public-help.JPG" caption="L\'interface d'aide de RERO ILS développée sous [flask-wiki](https://github.com/rero/flask-wiki)">}}

## Listage des nouvelles acquisitions

Un champ qui devrait s'avérer intéressant pour la mise en avant des collections a été implémenté dans le modèle de données des exemplaires : `new_acquisition`. Ce champ permet d'indiquer si un exemplaire doit faire partie des _nouvelles acquisitions_ selon les critères de chaque bibliothèque. Cela permet d'exclure certains documents de cette liste (documents patrimoniaux, rachats, livres plus anciens, ou autres). Ce champ comprend aussi une date qui pourra être utilisée pour construire des URL permettant d'afficher la liste des nouvelles acquisitions d'une bibliothèque. Cette liste peut être filtrée par date, mais aussi selon d'autres critères (localisation, statut, etc.), ce qui apporte une grande flexibilité.

Un cas d'utilisation courant de cette fonctionnalité est de pouvoir renvoyer vers la liste des nouvelles acquisitions pour un mois donné directement depuis le site web d'une bibliothèque. Les URL créées sont permanentes et pointent directement sur une liste de documents de l'interface publique de RERO ILS. La construction des URL pour ces listes est par ailleurs documentée dans [l'aide professionnelle](https://ils.test.rero.ch/help/recherche/#nouvelles-acquisitions). 

## Importation de notices externes par API

Pour terminer avec les nouveautés de cette `v0.12.0`, mentionnons l'ouverture d'un point d'accès API qui permet à un utilisateur authentifié d'importer des données `marcxml` directement dans RERO ILS en utilisant un script ou une application externe. Dans le contexte de nos bibliothèques pilotes, le logiciel [EZPump](http://www.ngscan.com/ezpump/) est utilisé pour importer des notices MARC de nombreux réservoirs. Il est actuellement en cours de test pour son adaptation à l'environnement RERO ILS via ce point d'accès.

## Deuxième phase des tests pilotes

Cette version est aussi l'occasion de poursuivre notre collaboration avec nos [bibliothèques pilotes](/reroils/early_adopters/). En effet, la deuxième vague de tests a été lancée le 24 septembre. La centrale est heureuse de compter sur la participation d'un nouveau partenaire pour ces tests, la Médiathèque de Monthey.