---
title: "Quelles nouveautés à la fin mars 2019 ?"
date: 2019-05-06
tags: ["rero-ils", "release"]
---

Fin mars, une nouvelle version de <span style="font-variant: small-caps;">rero ils</span> (v0.1.a21) a été publiée :

- La [note de publication](https://github.com/rero/rero-ils/releases/tag/v0.1.0a21) donne la liste des modifications et des ajouts.
- Le site de démonstration public : [ils.test.rero.ch](https://ils.test.rero.ch).
- La page d'aide : [github.com/rero/rero-ils/wiki/Public-demo-help](https://github.com/rero/rero-ils/wiki/Public-demo-help).

Vous trouverez ci-dessous une brève description des principales évolutions.

<!--more-->

Celles-ci concernent les aspects suivants :

1. le prêt,
1. l'interface utilisateur,
1. les autorités personnes.

### Le prêt.

Au cours de l'été 2018, l'équipe de développement de <span style="font-variant: small-caps;">rero ils</span> a collaboré avec l'équipe de [<span style="font-variant: small-caps">cds</span>](http://cds.cern.ch) du [<span style="font-variant: small-caps">cern</span>](https://home.cern) afin de réécrire le module [`invenio-circulation`](https://github.com/inveniosoftware/invenio-circulation) en s'appuyant sur une [modélisation du prêt](https://github.com/rero/rero-ils/blob/master/doc/circulation_statechart/circulation_item_statechart.pdf) suffisamment générique pour pouvoir être adaptée à la grande majorité des bibliothèques.   
Ce module est désormais pleinement intégré et utilisé pour chaque transaction de circulation au sein de <span style="font-variant: small-caps;">rero ils</span>.

Cette version complète par ailleurs une composante importante de la circulation, à savoir le paramétrage des politiques de prêt et leur prise en compte lors des transactions. Une politique de circulation établit, pour un couple *type de lecteur* / *type d'exemplaire* donné si le prêt et les prolongations sont possibles, et leur durée. À noter que le minimum requis pour le paramétrage du module de prêt est de créer une seule politique de prêt et de préciser que c'est la politique par défaut. En effet, lors d'une transaction, en fonction du type du lecteur et du type d'exemplaire, le système cherche si il y a une politique de prêt qui s'applique, d'abord au niveau de la bibliothèque, puis au niveau de l'organisation. S'il n'en trouve pas, alors il va utiliser la politique de prêt par défaut.

{{< figure src="/img/0a21-circ-pol.png" caption="Exemple de politique de prêt" alt="Capture d'écran de l'éditeur de politique de prêt" >}}

### L'interface utilisateur.

L'interface utilisateur a été entièrement revisitée dans le but de la simplifier et d'harmoniser quelque peu la structure des pages selon leur type (recherche, vue de notices… ). Une redistribution a également été réalisée entre les pages disponibles publiquement, mais avec des fonctionnalités professionnelles selon l'utilisateur ou l'utilisatrice connectée, et les pages qui ne sont jamais accessibles aux non professionnels.

Au cours de la  saisie, le champ de recherche propose des suggestions. Il s'agit d'une liste de titres de documents ou d'autorités personnes correspondant à la requête en cours de saisie. Lorsque l'on sélectionne une proposition de document, une recherche est lancée avec les mots du titre, alors que si l'on sélectionne une autorité personne, la notice de celle-ci est affichée.

{{< figure src="/img/0a21-suggestion-recherche.png" caption="Suggestion de recherche" alt="Capture d'écran des suggestions de recherche sous le champ de recherche, lors de la saisie" >}}

### Les autorités personnes.

L'usage par <span style="font-variant: small-caps;">rero ils</span> du [<span style="font-variant: small-caps;">mef</span>](https://mef.test.rero.ch) s'est considérablement développé. Un travail important a eu lieu sur le <span style="font-variant: small-caps;">mef</span> lui-même qui est passé des 96 notices de personnes physiques, lors des tests, au lot complet de 6,8 millions de notices.

Dans <span style="font-variant: small-caps;">rero ils</span>, les liens existants entre les notices bibliographiques et ces autorités personnes ont été importés, concrétisés par des hyperliens permettant d'afficher la notice de telle ou telle personne physique. D'un point de vue technique, la notice d'autorité personne n'est pas importée dans <span style="font-variant: small-caps;">rero ils</span>, mais interrogée à distance en temps réel.

Lors du catalogage, l'éditeur permet de rechercher, toujours en temps réel via le service <span style="font-variant: small-caps;">mef</span>, une autorité personne parmi les 6,8 millions d'autorités existantes et d'enregistrer un lien si l'autorité désirée existe. Sinon, les données de l'auteur sont stockées sous forme textuelle dans la notice bibliographiques. Le mécanisme des autorités temporaires doit encore être modélisé et développé.

{{< figure src="/img/0a21-edit-authority.png" width="300px" caption="Recherche d'une autorité personne lors de la création d'une notice bibliographique" alt="Capture d'écran de la recherche d'autorité personne dans l'éditeur lors du catalogage" >}}
