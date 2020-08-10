---
title: "MEF: Multilingual Entity File"
language: "fr"
date: 2020-08-18
---

# Ce que fait MEF

MEF est un dispositif qui combine des entités (ou autorités) en plusieurs langues et les met à disposition, ce qui permet notamment :

* À l'utilisateur·trice : de rechercher et afficher les contenus (et pas seulement l'interface) dans sa propre langue
* Aux bibliothèques : de réutiliser autant que possible des référentiels internationaux (GND, IdRef…). Elles peuvent ainsi abandonner la gestion en local d'un fichier d'autorités et embrasser le web des données.

MEF est une API mettant à disposition les données pour d'autres systèmes, notamment pour des ILS. Il est donc utilisable par plusieurs interfaces différentes. Par exemple, RERO ILS utilise MEF. Ce service ne dispose pas d'interface utilisateur propre.

RERO développe ce service de manière ouverte et le met à disposition, pour l'instant en version test, à l'adresse [mef.test.rero.ch](https://mef.test.rero.ch "Le service MEF, accessible librement").

# Types d'entités

MEF contiendra à terme les types de ressources tels que spécifiés dans les standards RDA et [Library Reference Model](https://www.ifla.org/publications/node/11412 "Library Reference Model, sur le site de l'IFLA") :

* personnes
* collectivités
* œuvres
* noms communs
* lieux
* périodes
* expressions

# Fonctionnement

MEF récupère et se synchronise avec les entités de différentes sources (GND, IdRef, etc.). Il les agrège automatiquement grâce à [VIAF](https://viaf.org "Site web du Virtual International Authority File"), déduisant ainsi des labels d'affichage en allemand et en français (à l'heure actuelle) lorsqu'ils sont disponibles.

Les entités elles-mêmes sont maintenues et éditées directement à la source en accord avec leur institution émettrice. Aucune entité n'est créée ni éditée directement dans MEF.

{{< figure src="/img/mef_fonctionnement.svg" caption="Fonctionnement de MEF" alt="Schéma du fonctionnement de MEF" >}}
