---
title: "Projet RERO 21"
language: "fr"
date: 2020-07-09
---

[RERO](https://www.rero.ch/) est le Réseau des bibliothèques de Suisse occidentale, dont la centrale est basée à Martigny, en Valais. Dans le contexte actuel de mutation du paysage des bibliothèques en Suisse, RERO se transforme d'ici 2021, en un centre de compétences et de services destinés aux bibliothèques. Il deviendra dès lors une fondation à but non lucratif. Ce projet d'envergure s'intitule RERO 21 et a été approuvé par l'autorité de tutelle de RERO, la [CIIP](https://www.rero.ch/pdfview.php?section=communique&filename=ciip_communique.pdf "Communiqué de la CIIP au format PDF") en septembre 2018.

Ce blog a pour objectif de publier des billets concernant RERO 21, regroupés sous [l'étiquette RERO 21](/tags/rero21 "Regroupement des billets concernant RERO 21"), ainsi que sur les différents sous projets qui le constituent : {{< smallcaps "rero ils" >}}, MEF et SONAR.

### RERO ILS

*Plus d'infos sur la [page de RERO ILS](/reroils)*

RERO ILS est un système de gestion de bibliothèque Open Source développé par RERO en collaboration avec l'[Université catholique de Louvain (UCLouvain)](https://uclouvain.be/). Il sera mis en production en remplacement du système actuel dans le cadre du projet RERO 21.

### MEF : *Multilingual Entity File*

RERO 21 proposera ses services sur l'ensemble du territoire helvétique, aussi {{< smallcaps "rero ils" >}} doit impérativement être multilingue. Avec MEF, RERO a developpé une solution décentralisée qui se base sur la fiabilité des autorités et sur le Linked Data.

MEF contiendra des notices de personnes, de collectivités, d'oeuvres, d'expressions, de lieux, de périodes et de noms communs, pouvant être intégrés et utilisés de manière multilingue par des systèmes de gestion de bibliothèque, dont {{< smallcaps "rero ils" >}}. MEF récupère les autorités des différentes sources (GND, IdRef, etc.) et les agrège automatiquement grâce à [VIAF](https://viaf.org "Site web du Virtual International Authority File"), déduisant ainsi des labels d'affichage en allemand et en français (à l'heure actuelle) lorsqu'ils sont disponibles. Les autorités elles-mêmes sont maintenues et éditées directement à la source, en accord avec leur institution émettrice.

RERO pense que le MEF peut être utile et a décidé de développer ce service de manière ouverte et de le mettre à disposition, pour l'instant en version test, à l'adresse [mef.test.rero.ch](https://mef.test.rero.ch "Le service MEF, accessible librement").

### SONAR : *Swiss Open Access Repository*

*Plus d'infos sur le site www.sonar.ch*

Le projet SONAR fait partie du programme [P-5](https://www.swissuniversities.ch/en/organisation/projects-and-programmes/p-5/) de [*swissuniversities*](https://www.swissuniversities.ch/ "Site web de *swissuniversities*"). Il s'agit du développement d'une archive institutionnelle nationale, dont le but est de collecter, de promouvoir et d'assurer la préservation des publications scientifiques *open access* des auteurs affiliés aux institutions de recherche publiques en Suisse. SONAR a également pour but d'offrir un service d'archive institutionnelle (*IR as a Service*).