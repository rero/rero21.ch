---
title: "Le catalogage s'étoffe"
date: 2020-07-06T08:23:38+02:00
publishdate: 2020-07-06
draft: false
tags: ["rero-ils", "release", "acquisition", "affichage", "métadonnées", "prédictions"]
slug: le-catalogage-setoffe
---

Un nouveau sprint se termine pour RERO ILS avec une version bien fournie en nouveautés. Grâce à des fondations techniques de plus en plus stables, l'équipe de développement peut se concentrer sur des fonctionnalités orientées vers les utilisateurs et les utilisatrices. Les notes complètes de cette nouvelle version sont consultables comme d'habitude sur la page Github : [`v0.10.0`][1].

<!--more-->

## Améliorations d'interface

Le travail sur les interfaces publique et professionnelle se poursuit. Cette version leur apporte de nombreux ajustements et notamment une refonte de l'éditeur de métadonnées (interface de catalogage) en vue d'améliorer sa lisibilité. L'éditeur occupe maintenant toute la largeur de l'écran et les champs sont mieux séparés visuellement ; les titres des champs principaux sont désormais en gras et certains sous-champs peuvent s'afficher en ligne. 

{{< figure src="/img/rero-ils-editeur.png" caption="Affichage de sous-champs en ligne plutôt que les uns sous les autres et titres des champs en gras">}}

## Importation de notices

Le fait de pouvoir importer des notices de catalogues externes facilite et fluidifie une grande partie du travail de catalogage des bibliothécaires. RERO ILS offre la possibilité de le faire via [le protocole SRU][2]. Il est possible de faire une requête par mots-clés (auteur, titre, date, ISBN, etc.) dans le catalogue choisi (à l'heure actuelle, seulement la BnF) et choisir la notice à importer. Celle-ci peut ensuite être librement éditée dans l'interface de catalogage avant son enregistrement. 

## Arrivée des fonctions de bulletinage

Autre nouveauté de cette version `v0.10.0`, les fonctionnalités de bulletinage des périodiques font leur apparition. Un champ **fréquence** dans l'état de collection, reprenant le [standard RDA][3], permet de prédire automatiquement les dates des prochains numéros réguliers et de les réceptionner rapidement, d'un simple clic. Il est bien sûr aussi possible de recevoir un numéro irrégulier. Le système crée automatiquement un exemplaire pour chaque numéro reçu.

{{< video src="rero-ils-receiveissue" legend="Réception rapide des fascicules réguliers selon leur fréquence" >}}

Dans la vidéo ci-dessus, un exemple de bulletinage rapide :

1. *Obtenir* affiche la liste des exemplaires
1. On affiche les prédictions des prochains numéros
1. Un clic sur le bouton de bulletinage rapide crée l'exemplaire. En cas de besoin, l'autre bouton permet d'éditer l'exemplaire avant de le bulletiner.

## Des bonnes notes pour les exemplaires

Pour terminer, mentionnons qu'un champ `notes` a été ajouté au modèle des exemplaires. Ces notes peuvent être de quatre types :

* **Note publique** : s'affiche dans la vue détaillée de l'interface publique et professionnelle.
* **Note professionnelle** : s'affiche seulement dans la vue détaillée de l'interface professionnelle.
* **Note de retour** : affiche une alerte lors du retour.
* **Note de prêt** : affiche une alerte lors du prêt.

Ces notes répondent à un besoin essentiel exprimé par plusieurs de nos bibliothèques pilotes ainsi que par nos partenaires de l'UC Louvain.

{{< figure src="/img/item-notes.png" caption="Les notes d'exemplaires dans l'interface professionnelle">}}

[1]: https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v0100
[2]: https://www.bnf.fr/fr/protocole-sru-vue-densemble
[3]: http://www.rdaregistry.info/termList/frequency/?language=fr