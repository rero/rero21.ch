---
title: "Vers l’intégration des autorités RERO dans le référentiel francophone IdRef"
date: 2020-03-12T12:00:00+02:00
draft: false
tags: ["autorités", "idref", "rero-ils", "slsp"]
---

Le réseau RERO sera scindé en deux groupes de bibliothèques à l’horizon 2020-2021, les unes intégrant la Swiss Library Services Platform (SLSP) et les autres adoptant la solution {{< smallcaps "rero ils" >}}. Afin d’éviter que cette situation entraîne la création de deux copies divergentes de son fichier d’autorités francophones actuel, RERO a souhaité l’arrêt de ce fichier au profit d’une solution plus reconnue et ancrée sur une communauté plus large, et pouvant être adoptée simultanément par SLSP et {{< smallcaps "rero ils" >}}. 

<!--more-->

Un accord de principe a été trouvé avec l’[ABES (Agence bibliographique de l’enseignement supérieur, France)](http://www.abes.fr/) en juillet 2019 pour intégrer les autorités RERO *noms propres* dans le fichier francophone [IdRef](https://www.idref.fr/).

Pour les bibliothèques de Suisse romande, cette solution a beaucoup d’avantages:

* Continuer de produire des autorités francophones après la transition. 
* Utiliser et enrichir un fichier d'autorités important et de grande qualité (3.5 millions d'autorités) qui fusionnera à terme avec celui de la BnF (Bibliothèque nationale de France) dans le cadre du [projet FNE](https://www.transition-bibliographique.fr/fne/fichier-national-entites/) (présenté à la [journée RERO](https://www.rero.ch/pdfview.php?section=communique&filename=JR19_FNE_journee_RERO.pdf) en mars 2019).
* Accroitre la visibilité des autorités RERO. 
* Profiter du [service MEF](https://mef.test.rero.ch/) (Multilingual Entity File) développé par RERO dans l'objectif d'implémenter une gestion multilingue des métadonnées dans des SGB

Une présentation plus complète du scénario a été faite en novembre 2019 à la BnF, voir *[Approche multilingue des autorités RERO avec le projet Multilingual Entity File](https://www.transition-bibliographique.fr/2019-09-26-inscriptions-ouvertes-4e-journee-metadonnees-bibliotheques-15-novembre-2019/)* (présentation + vidéo).

### Principes de la solution

* Saisie par les catalogueurs et indexeurs des nouvelles autorités noms propres directement dans IdRef via l’application web
* Établissement des liens aux autorités IdRef et RERO-RAMEAU par la saisie des identifiants dans les points d’accès des notices bibliographiques
* Gestion séparée du référentiel [RERO-RAMEAU (noms communs)](https://www.rero.ch/pdfview.php?section=ressources&filename=rameau_dans_le_reseau_suisse_rero_20141106.pdf), que nous adaptons depuis 2012 à l’indexation post-coordonnée, avec transferts mensuels vers Alma/SLSP et MEF/{{< smallcaps "rero ils" >}}
* Moissonnage régulier du [serveur OAI PMH d’IdRef](http://www.abes.fr/Autorites-et-referentiels/Services-disponibles/Entrepot-OAI-PMH-IdRef) vers Alma/SLSP et MEF/{{< smallcaps "rero ils" >}} pour les mises à jour
* Transmission des propositions RAMEAU à la BnF par les correspondants RAMEAU des sites romands SLSP et RERO, comme jusqu'à présent

### Étapes préparatoires

1. Arrêt de l’alimentation des fichiers d’autorité RERO *noms propres* avant les go-live de fin 2020,
1. Intégration des autorités RERO dans IdRef par le biais d’alignements, d’enrichissements et d’ajouts pour les entités personnes, collectivités noms géographiques et titres, 
1. Intégration d’IdRef dans {{< smallcaps "rero ils" >}} (via MEF) et dans la Community Zone d’Alma en MARC 21

{{< figure src="/img/migration_idref.png" caption="Transition des autorités RERO vers IdRef" alt="Schema: Transition des autorités RERO vers IdRef" >}}

### États des réalisations en mars 2020

L'ABES, RERO, SLSP et la société Ex Libris collaborent activement afin de concrétiser ce projet dans les temps impartis. Ont notamment été réalisés :

* Tests (très prometteurs) d’alignements sur 10'000 autorités personnes
* Alignements sur 200’000 autorités personnes (en cours)
* Intégration des identifiants PPN IdRef sur environ 200'000 notices bibliographiques en vue du troisième test de chargement de données SLSP
* Mapping UNIMARC autorités -> MARC 21 autorités
* Préparation du serveur OAI PMH IdRef en version MARC21 (en cours)

### Début d’un travail de Bachelor sur ce projet

La centrale est très heureuse d’accompagner Etienne Attinger, étudiant à la HEG Genève et en parallèle bibliothécaire à l’Université de Genève, dans la réalisation d’un travail de Bachelor sur le sujet de l’alignement des autorités. Ce mandat a débuté en février et doit se terminer au mois de juillet 2020. Il a pour titre provisoire *Étude, éléments de réalisation et évaluation de l’intégration des autorités RERO dans le référentiel francophone IdRef*.
