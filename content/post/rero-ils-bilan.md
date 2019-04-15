---
title: "RERO ILS : un bilan"
date: 2018-11-23T12:17:24+01:00
draft: true 
tags: ["rero-ils"]
---

Le développement d'un système de gestion de bibliothèque est au centre du projet RERO 21. Jusqu'ici, ce développement s'est fait sour le nom RERO ILS, mais il n'est pas impossible que ce nom change à l'avenir. Ce développement ne part pas complètement de zéro puisqu'il se base sur le *framework* [Invenio](https://inveniosoftware.org "Site web d'Invenio"). Une première exploration a été présentée en novembre 2017, lors de la journée RERO.

<!--more-->

Depuis, le logiciel s'est 


------------------------------

Pour autant, la déclinaison <abbr title="Integrated Library Service"><span style="font-variant: small-caps;">ils</span></abbr>

------------------------------


Le développement de RERO-ILS, le futur système de gestion de bibliothèque de RERO prévu pour 2021, suit son cours à un rythme soutenu à la Centrale RERO.

Fin novembre 2018, le prototype comprend :

- une structure consortiale à 3 niveaux (organisation, bibliothèque et localisation)
- 10’000 notices bibliographiques de livres importées du catalogue RERO, ainsi que des exemplaires fictifs générés automatiquement, liés aux notices;
- Plus de 8'000 notices d'e-books du fournisseur Cantook moissonnées par OAI-PMH (en attendant le moissonnage prévu par API en début d'année 2019);
- un moteur de recherche complet, y compris une recherche avancée performante réalisée par des équations de recherche complexe;
- une interface de recherche avec des filtres par facette;
- la possibilité de s’identifier avec un compte professionnel (utilisateur : reroilstest@gmail.com, mot de passe : 123456);
- un éditeur simple pour créer un nouvel enregistrement ou éditer une notice existante;
- une interface de prêt permettant de traiter les prêts, retours et demandes;
- une interface d'administration réservée au professionnel identifié;
- environ 100 notices d'autorités multilingues de type personne (RERO, BNF, GND) moisonnées depuis le serveur MEF dédié à la gestion d'autorités multilingues;
- des vignettes de couverture;
- une fonction d’importation de notices, depuis le service SRU de la BNF, utilisant le numéro EAN pour l’identification d’un document.

La méthode de gestion de projet appliquée par RERO pour le développement de RERO-ILS est la méthode Scrum.

La réflexion autour du développement du module de prêt à engagé une collaboration étoite avec le CERN au cours de l'été pour faire évoluer l'outil Invenio et plus spécifiquement le module Invenio circulation afin de l'adapter aux besoins spécifiques de RERO. Le CERN continue à être un partenaire privilégié de RERO pour le développement de RERO-ILS, les équipes à Martigny et à Genève ayant des contacts réguliers.

Bien qu'un effort important ait jusqu'ici été investi dans l'implémentation des premières fonctionnalités de prêt, d'autres fonctionnalités liées aux métadonnées, à l'interface publique ou encore à l'administration du système sont développées en parallèle. La mise en place des fonctionnalités dans RERO-ILS se fait ainsi en fonction de récits utilisateurs (user stories selon la dénomination Scrum), discutés et prioriés par une partie de l'équipe RERO représentant la vision du client final (Product Owner). Une collaboration étroite s'en suit avec l'équipe de développement chargée de traduire cette vision du client final concrètement dans RERO-ILS. Ainsi, cette approche est privilégiée à celle visant une implémentation module par module. C'est donc tout un travail d'équipe qui mobilise une grande partie des collaborateurs de la Centrale.

L'équipe de développement avance par sprints de 3 semaines consécutives. À un rythme de 3 à 4 semaines, de nouvelles versions de RERO-ILS sont déployées sur l'instance publique de test, accompagnées d’une note de publication de version. Les notes de publication sont accessibles publiquement sur GitHub : https://github.com/rero/reroils-app/releases.

Le dernier sprint de l'année 2018, débuté le 26.11.2018, est dédié à un important travail de refactoring ainsi qu'à la poursuite de la mise en place de fonctionnalités liées au module de prêt, dont la gestion du calendrier des bibliothèques (prise en compte des heures d'ouverture et de fermeture, des jours fériés, etc.) et à l'attribution de règles de prêt aux combinaisions exemplaire/type de lecteur.

Le prototype sera présenté lors de la prochaine Journée RERO, le jeudi 28 mars 2019. Réservez d'ores et déjà cette date!

- [RERO ILS](https://ils.test.rero.ch 'Le site démo de RERO ILS')
- <i class="fab fa-github"></i> [`rero-ils`](https://github.com/rero/rero-ils 'Le projet rero-ils sur GitHub')
- le [wiki](https://github.com/rero/rero-ils/wiki 'Le wiki de RERO ILS')

La liste des fonctionnalités prévues, ainsi que la liste des fonctionnalités sélectionnées pour
chaque sprint, sont consultables sur le site taiga.io : https://tree.taiga.io/project/rero21-
reroils/backlog.
Le code source du projet est disponible sur GitHub.
Il est possible de contacter de manière informelle l’équipe de développement via le salon Gitter
https://gitter.im/rero/reroils, via le compte Twitter de la centrale (@rero_centrale), ou via
l’adresse e-mail info@rero.ch.

Enfin, une page d’aide en anglais est régulièrement mise à jour, dans le but d’expliquer
l’utilisation de l’instance de démonstration: https://github.com/rero/reroils-app/wiki/Publicdemo-help.

{{< figure src="/img/rero-ils-homepage2.PNG"
		   alt="Capture d'écran de la page d'accueil de RERO ILS"
           link="https://ils.test.rero.ch"
		   caption="Page d'accueil de RERO ILS" >}}
