---
title: "Les prédictions ? Ça promet !"
date: 2020-05-05T07:14:42+02:00
publishdate: 2020-05-06
draft: false 
tags: ["rero-ils", "release"]
---

Alors que le
[sprint
29](https://tree.taiga.io/project/rero21-reroils/wiki/sprint-info-page-29)
est terminé et que le [sprint
30](https://tree.taiga.io/project/rero21-reroils/wiki/sprint-info-page-30) a
déjà bien commencé, la [version
`v0.8.0`](https://github.com/rero/rero-ils/releases/tag/v0.8.0) de {{<
smallcaps "rero ils" >}} est publiée ([notes de version
complètes](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v080)).
Ci-dessous, un bref résumé des nouveautés.

<!--more-->

Les prédictions pour les périodiques deviennent possibles, avec une souplesse
qui permet d'encoder les cas les plus courants. Concrètement, les *holdings*
correspondant à des publications en série peuvent être éditées et une section
du formulaire est dédiée à la prédiction. Celle-ci se fait en deux temps, le
premier pour paramétrer la séquence elle-même, et le deuxième pour configurer
son affichage, au moyen d'un mécanisme de *template*. Dix des prédictions les
plus fréquemment utilisées dans les bibliothèques du réseau RERO ont été
importées avec succès.

## Historique des transactions 

Le compte du lecteur ou de la lectrice vu par le ou la bibliothécaire
s'enrichit d'un onglet affichant l'historique des transactions. Pour l'instant,
et conformément aux règles en vigueur, cet historique contient les transactions
des six derniers mois. À l'avenir, le lecteur ou la lectrice pourra décider si
cet historique sera accessible ou non. Toutefois, un historique des
transactions d'un exemplaire, relativement limité dans le temps, restera
nécessaire pour le bon fonctionnement des bibliothèques.

## Abonnements annuels

La gestion des frais permet désormais celle des abonnements annuels, ce qui
correspond à une pratique existante dans certains cantons ou municipalités en
Suisse.

## Édition manuelle de la liste des demandes

Le ou la bibliothécaire pouvait déjà placer une demande sur un exemplaire pour
un lecteur ou une lectrice, il ou elle peut maintenant éditer la liste des
demandes existantes pour un exemplaire, afin d'ajouter une demande
supplémentaire, en supprimer une, ou modifier le lieu de retrait d'une des
demandes.

## Résultats de recherche filtrés par organisation

La recherche dans l'interface professionnelle filtre désormais les résultats
sur la base de l'organisation de la personne connectée, cette dernière
travaillant le plus souvent sur les exemplaires appartenant à son réseau. Une
nouvelle facette hiérarchique, avec l'organisation concernée sélectionnée par
défaut, permet de restreindre les résultats à une bibliothèque particulière, ou
au contraire d'étendre la recherche à l'ensemble du catalogue des organisations
de {{< smallcaps "rero ils" >}}, afin par exemple de se raccrocher à une notice
bibliographique existant dans une autre organisation.\
Ce filtre par défaut s'applique également aux suggestions de recherche
proposées lorsque l'on tape une requête.

{{< video src="ils-pro-result-filter" legend="Filtrage par défaut des résultats de recherche" >}}

## Intégration des autorités IdRef dans MEF

Enfin, on peut noter que les autorités personnes du fichier d'autorité IdRef
ont été ajoutées au serveur d'autorités multilingues
[{{< smallcaps "mef" >}}](https://mef.test.rero.ch) et sont visibles dans
{{< smallcaps "rero ils" >}}, en vue du jour où les autorités
{{< smallcaps "rero" >}} seront versées dans ce fichier.
