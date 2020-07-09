---
title: "RERO ILS: système de gestion de bibliothèque open source"
language: "fr"
date: 2020-07-13
---

RERO ILS est un système de gestion de bibliothèque (SGB) *open source* développé par RERO en collaboration avec l'[Université catholique de Louvain (UCLouvain)](https://uclouvain.be/). ILS est une abréviation anglaise signifiant *Integrated Library System*. Il s'agit d'une catégorie de logiciels permettant de gérer les activités courantes d'une bibliothèque (acquisitions de documents, prêt, catalogage, recherche) et offrant une interface publique pour les utilisateurs.

D'un point de vue technique, RERO ILS se fonde sur le *framework* [Invenio](https://invenio-software.org) développé par le [CERN](https://home.cern/).

Un site web de démonstration est publiquement accessible à l'adresse suivante : [ils.test.rero.ch](https://ils.test.rero.ch "Site de démonstration de RERO ILS").

### Le contexte RERO

RERO ILS représente la pierre angulaire du projet de mutation [RERO 21](/about).

Se basant sur plus de 30 ans d'expérience dans la gestion d'un important réseau de bibliothèques, la centrale RERO a débuté le développement de RERO ILS en 2017, dans le but de remplacer à l'horizon 2021 le logiciel propriétaire actuellement implémenté dans le réseau. Grâce à un système *open source*, la centrale peut exploiter le plein potentiel de ses compétences pour satisfaire au mieux les besoins actuels et futurs de ses bibliothèques membres.

Le service RERO ILS proposé par RERO vise essentiellement les bibliothèques et réseaux de bibliothèques publics, scolaires et patrimoniaux en Suisse. Il est disponible en français, allemand, italien et anglais.

### Que fait RERO ILS?

Une première version stable est agendée pour la fin de l'année 2020, pour être déployée en production dans le courant de l'année 2021, avec les fonctionnalités suivantes :

* Une interface publique
	* Fonctions pour les utilisatrices et utilisateurs de bibliothèque : recherche, compte personnel, demandes de prêt, gestion des emprunt, etc.
	* Système d'authentification unique (Single Sign-On)
	* Une interface pour chaque réseau ou organisation
	* Une interface collective regroupant toutes les organisations
* Une interface professionnelle
	* Administration : paramétrage des bibliothèques et localisation, des règles de prêt
	* Gestion des utilisateurs
	* Gestion des frais : retard, abonnements
	* Gestion du catalogue : recherche, description (standard RDA), import et export de métadonnées, gestion des exemplaires
	* Gestion multilingue des autorités au moyen de MEF
	* Gestion de la circulation : prêts, retours, prolongations, demandes, transits de documents entre bibliothèques
	* Gestion des publications en série : prédictions, bulletinage, états de collection
	* Gestion des acquisitions : budgets, comptes, fournisseurs, commandes, factures
* Fonctionnement consortial
	* Trois niveaux : organisations, bibliothèques, localisations
	* Les organisations sont indépendantes au sein du système, mais partagent les données bibliographiques

A l'heure actuelle, certaines de ces fonctionnalités sont encore en plein développement.

### Bibliothèques "early adopters"

Une quarantaine de bibliothèques actuellement membres de RERO ont communiqué leur intention de bénéficier de la solution RERO ILS, avec un passage en production prévu pour l'été 2021. Parmi celles-ci, six bibliothèques pilotes collaborent au processus de développement participatif :

* [Bibliothèque cantonale jurassienne](https://www.jura.ch/occ/bicj)
* [Bibliothèque de Bulle](https://musee-gruerien.ch/)
* [Bibliothèque de la Ville de la Chaux-de-Fonds](http://cdf-bibliotheques.ne.ch/)
* [Bibliothèque municipale de Delémont](http://www.delemont.ch/fr/Tourisme-culture-et-loisirs/Vie-culturelles/Bibliotheque/Bibliotheque.html)
* [Bibliothèque publique et universitaire de Neuchâtel](http://bpun.unine.ch/)
* [Médiathèque Valais](https://www.mediatheque.ch/)

Complété par l'expertise des bibliothèques d'UCLouvain, ce pôle utilisateurs constitue la base de référence pour les orientations de RERO ILS. L'équipe de développement est très heureuse de pouvoir compter sur cette participation !

### Contribuer à RERO ILS

Vous pouvez tester la dernière version sur [ils.test.rero.ch](https://ils.test.rero.ch/). En cas de question, adressez-vous à l'équipe RERO via notre [chat Gitter](https://gitter.im/rero/reroils).

Sur le [dépôt Github](https://github.com/rero/rero-ils/) de RERO ILS, vous trouverez toutes les informations sur l'installation du système et la contribution au développement.