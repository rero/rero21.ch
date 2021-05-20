---
title: "Sortie de la v1.2.0 : merci pour les traductions !"
date: 2021-05-20
draft: false
tags: ["multilinguisme", "release", "rero-ils"]
---

Après un nouveau sprint intense chez RERO+ et UCLouvain, l'arrivée de la
version `v1.2.0` amène son lot de nouveautés et de corrections pour stabiliser
RERO ILS avant le *go-live* du 12 juillet. Les notes de version complètes sont
consultables sur [GitHub][release-notes]. C'est l'occasion pour nous de mettre
en avant l'aspect communautaire de RERO ILS avec les processus de traduction du
système.

<!--more-->

## La traduction communautaire de RERO ILS

Afin d'être ouvert et accessible, RERO ILS se doit également d'être
multilingue. Dans cette optique, le logiciel est traduit avec l'aide du service
[Weblate](https://hosted.weblate.org/projects/rero_plus/rero-ils/) qui permet à
l'équipe de développement de collaborer sur ce travail, mais aussi à des
personnes externes de participer. En effet, la communauté peut proposer des
traductions pour le projet. Nous souhaitons donc remercier les membres suivants
pour leurs contributions à ce projet :

- [Ambros Gattlen](https://hosted.weblate.org/user/ambgat/)
- [phlostically](https://hosted.weblate.org/user/phlostically/)
- [Adolfo Jayme Barrientos](https://hosted.weblate.org/user/Fito/)
- [Allan Nordhøy](https://hosted.weblate.org/user/kingu/)

Si vous souhaitez vous aussi apporter votre pierre à l'édifice, n'hésitez pas à
visiter [la page du projet sur
Weblate](https://hosted.weblate.org/projects/rero_plus/rero-ils/).

## Plusieurs organisations pour un lecteur ou une lectrice

Parmi les [nombreuses nouveautés][release-notes] de la `v1.2.0` se trouve la
possibilité de s'inscrire dans différentes organisations avec le même compte,
un besoin clair des bibliothèques de RERO+.

Comme nous l'avons déjà [noté](/nouvelle-version-1.1.0/), les données de
circulation des utilisatrices et utilisateurs ne sont pas partagées entre
différentes organisations ; il est néanmoins probable que des personnes soient
inscrites dans des bibliothèques d'organisations différentes, par exemple une
fois dans le réseau de RERO Valais et une deuxième fois dans le réseau RBNJ
(Neuchâtel-Jura). Elles peuvent désormais consulter leurs données
(emprunts, historique, amendes, etc.) des différentes bibliothèques dont elles
sont membres grâce à un menu déroulant directement depuis leur compte. Ainsi,
il n'est pas nécessaire de changer d'interface ou de se déconnecter pour avoir
accès à ces informations.

{{< video src="patron-profile-several-orgs" legend="Une lectrice consulte ses données de prêt dans différentes organisations de RERO ILS" >}}

[release-notes]: https://github.com/rero/rero-ils/blob/dev/RELEASE-NOTES.rst#v120
