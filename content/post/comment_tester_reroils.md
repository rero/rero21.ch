---
title: "Comment tester RERO ILS?"
date: 2019-04-29
draft: false
tags: ["rero ils"]
---

Vous avez déjà entendu parler plusieurs fois de <span style="font-variant: small-caps">rero ils</span>, mais vous aimeriez voir à quoi cela ressemble concrètement? Vous faire votre propre opinion, mettre les mains dans le cambouis? Ça tombe bien: <span style="font-variant: small-caps">rero ils</span> est un logiciel libre et développé de manière totalement transparente.

<!--more-->

Voici comment procéder à 3 niveaux.

### Pas à pas

#### Niveau 1: utilisateur/utilisatrice anonyme

* Rendez-vous sur [ils.test.rero.ch](http://ils.test.rero.ch/)

C'est là que se trouve le site de démonstration public. A ce stade, vous avez accès à toutes les fonctionnalités destinées aux personnes non connectées.

#### Niveau 2: lecteur/lectrice

* Ouvrez la page d'aide de <span style="font-variant: small-caps">rero ils</span> (*Menu* > *Aide*) ou cliquez [directement ici](https://github.com/rero/rero-ils/wiki/Public-demo-help#sign-up-and-log-in)
* Récupérez les données de connexion d'un lecteur, sous *Sign up and Log in*, par exemple de Simonetta (`reroilstest+simonetta@gmail.com` / `123456`)
* Revenez à <span style="font-variant: small-caps">rero ils</span> et connectez-vous (*Mon compte* > *Se connecter*)

A ce niveau, vous pourrez notamment consulter votre compte et faire des commandes.

#### Niveau 3: bibliothécaire

* Suivez la procédure du niveau 2, mais récupérez plutôt les données de connexion d'Astrid par exemple (`reroilstest@gmail.com` / `123456`)

Là, vous testerez <span style="font-variant: small-caps">rero ils</span> en tant que bibliothécaire système, donc avec droits étendus! Vous pourrez entre autres effectuer des prêts, paramétrer leur durée et le nombre de prolongations autorisées, inscrire des lecteurs/lectrices, cataloguer des ouvrages ou encore gérer les heures d'ouverture de votre bibliothèque.

### Une alerte lors de chaque nouvelle version de RERO ILS?

Le compte [Github de RERO](https://github.com/rero) héberge les différents projets logiciels de la centrale. Vous y trouverez donc entre autres le projet [RERO ILS](https://github.com/rero/rero-ils/) et ses [versions/releases](https://github.com/rero/rero-ils/releases) successives.

1. Par **flux RSS**:
	* Rendez-vous dans les [releases RERO ILS](https://github.com/rero/rero-ils/releases)
	* Prenez l'URL et ajoutez-y `.atom`: https://github.com/rero/rero-ils/releases.atom
	* Insérez cette URL dans votre gestionnaire de flux RSS!
2. Par **e-mail** (requiert d'avoir ou de se créer un compte Github)
	* Rendez-vous dans les [releases RERO ILS](https://github.com/rero/rero-ils/releases)
	* En haut à droit, cliquez sur *Watch*, puis *Release only*
	* Indiquez que vous souhaitez recevoir les notifications par e-mails dans vos [paramètres](https://github.com/settings/notifications), section *Watching*

### Aller plus loin... et nous faire part de bugs ou de suggestions

Il manque des fonctionnalités essentielles?

* Notre *backlog*, le journal des prochains développements prévus, est librement consultable sur notre outil de collaboration [Taiga](https://tree.taiga.io/project/rero21-reroils/backlog). En explorant un peu, vous y trouverez les tâches en cours auprès des développeurs et tout l'historique des *user stories*, ou récits utilisateurs implémentés.

Vous êtes tombé/e sur un bug?

* Si vous voulez vraiment bien faire les choses, consultez les [problèmes](https://github.com/rero/rero-ils/issues) (*issues* en jargon Github) déjà signalés. Vous pouvez même ouvrir vous-même une issue si vous avez un compte Github.
* S'il n'y a rien dans les issues (et même si vous n'avez pas vérifié), vos retours sont les bienvenus par [e-mail](info@rero.ch) ou via le [chat public](https://gitter.im/rero/reroils) (authentification nécessaire). Nous nous engageons à vous répondre!

Merci d'avance pour votre participation et vos tests!