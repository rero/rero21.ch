---
title: "Nouvelle version 1.1.0 : corrections et ajustements"
publishdate: 2021-04-14
draft: false
tags: ["rero-ils", "release", "tests"]
---

Après la stabilisation de la première version majeure 1.0.0 de RERO ILS ([voir les notes de version](https://github.com/rero/rero-ils/blob/dev/RELEASE-NOTES.rst#v100)), une grande partie des ressources de la centrale et des bibliothèques a été investie dans la préparation [du projet de migration](https://rero21.ch/kick-off-du-projet-de-migration-rero-ils/). Cependant, les développements de RERO ILS sont loin de s'arrêter là. Preuve en est une nouvelle version `v1.1.0` dont les notes complètes sont toujours disponibles sur [Github](https://github.com/rero/rero-ils/blob/dev/RELEASE-NOTES.rst#v110).

<!--more-->

## Gestion des utilisateur·trice·s

La gestion des données du profil des lectrices et lecteurs de RERO ILS est une question plus complexe qu'il n'y paraît dans un contexte consortial comme celui de RERO ILS. La version `v1.1.0` implémente la structure finale de ces données et permet aux bibliothécaires de gérer plus finement certains paramètres de prêt, comme les notifications et les frais de retard. Les données de chaque utilisateur·trice sont enregistrées sur deux niveaux dans RERO ILS :

- `User` : Contient les données personnelles (nom, sexe, numéros de téléphone, ...) dans le compte RERO qui est partagé par toutes les organisations.
- `Patron` : Lié à un `user`, il contient les données de gestion spécifiques à chaque organisation telles que les transactions de prêt, le rôle et le type de lecteur, les notes, etc.

Cette structure permet d'une part de respecter les exigences légales de protection des données, et d'autre part de n'avoir qu'un seul compte `user` par utilisateur·trice plutôt que d'en créer un pour chaque organisation. Les lectrices et lecteurs peuvent ainsi utiliser le même compte, et donc les mêmes identifiants, s'ils sont inscrits dans plusieurs organisations. En l'état, ce module offre donc plusieurs avantages : 

- Un serveur de [Single Sign-On](https://fr.wikipedia.org/wiki/Authentification_unique) pour une authentification unique sur plusieurs services et organisations.
- La possibilité d'enregistrer des lectrices ou lecteurs sans adresse e-mail, par exemple pour des enfants en bibliothèque publique ou scolaire.
- Le respect de la confidentialité des données entre les différentes organisations
- L'utilisation comme un service web moderne avec un nom d'utilisateur personnalisable. Le numéro de la carte n'est ainsi plus nécessaire pour se connecter à son compte.

Par ailleurs, des travaux ont aussi été effectués dans le but de permettre une bonne gestion des avis de réservation ou d'échéance ainsi que le blocage des comptes dont la date d'expiration a été atteinte.

## Ajout de métadonnées

En préparation de la migration finale des données pour le lancement de RERO ILS le 12 juillet 2021, le modèle de métadonnées a été complété au niveau des exemplaires. Les champs prix, code PAC (preservation and conservation) et URL (pour les documents électroniques en ligne) ont été ajoutés. 

En outre, le système permet désormais aux bibliothécaires de masquer des documents ou des exemplaires afin qu'ils n'apparaissent pas dans l'interface publique. Cette fonctionnalité est utilisée par exemple pour des exemplaires patrimoniaux ou à usage interne.

{{< figure src="/img/masked.png" caption="Un simple interrupteur permet de masquer ou dé-masquer les ressources.">}}

## Correction de bugs

Grâce à la collaboration avec les bibliothèques pilotes lors des phases de test et de préparation à la migration, de nombreux problèmes ont pu être identifiés dont une partie ont été corrigés dans cette version. Une vingtaine d'`issues` ont pu être fermées et plusieurs autres corrections mineures de fonctionnalités ont été implémentées. Travail de longue haleine, la chasse aux bugs continue mais la stabilité du système ne cesse de s'améliorer de version en version. 