---
title: "\"Swiss made\" signifie aussi multilingue"
publishdate: 2021-02-18
draft: false
tags: ["rero-ils", "multilinguisme", "entités"]
slug: swiss-made-signifie-aussi-multilingue
---

Avec l'intégration des collectivités dans son modèle de données, RERO&nbsp;ILS concrétise clairement l'ambitieux objectif de multilinguisme promis par le projet MEF. L'utilisatrice ou l'utilisateur final aura ainsi non seulement accès à une interface en plusieurs langues, mais également à des *données* en plusieurs langues. Suisse oblige! 🇨🇭

<!--more-->

## Fonctionnement du multilinguisme

Le multilinguisme des données se base sur le projet [MEF - Multilingual Entity File](https://www.rero.ch/produits/mef). La page du projet explique en détail le fonctionnement du service. En voici les principes résumés:

1. Lors du catalogage, les documents sont reliés à des agents[^1] décrits dans les fichiers d'entités IdRef[^2] (en français) ou GND[^3] (en allemand).
2. Chaque mois, le système VIAF fusionne les entités IdRef et GND (et autres) représentant les mêmes agents.
3. MEF récupère ces données et RERO&nbsp;ILS peut ensuite afficher, dans l'interface publique
    * la version IdRef si la langue de l'interface est le français.
    * la version GND si la langue de l'interface est l'allemand.

Le multilinguisme a certaines limites:

* Il ne fonctionne pour l'instant que pour l'allemand et le français.
* Il ne fonctionne que pour les documents avec lien à une entité présente à la fois dans IdRef et GND (et qui a été clusturisée par VIAF).
* Il est particulièrement utile pour les noms de collectivités, mais moins pour les noms de personnes qui ne sont pas traduits d'une langue à l'autre.

Enfin, les référentiels IdRef et GND sont également deux éléments essentiels du catalogage au sein du réseau SLSP. RERO assure donc une bonne interopérabilité des données.

## Une réelle plus-value pour l'utilisatrice ou l'utilisateur final

Le multilinguisme se caractérise par trois fonctionnalités dans l'interface.

**1. L'affichage des noms de personnes et de collectivités pour les documents**

Ces noms sont présents dans la liste de résultats, dans la vue détaillée du document et au sein du compte lecteur (emprunts, historique, demandes, etc.). Lorsque la langue de l'interface change, la forme allemande ou française est affichée.

Dans l'image ci-dessous, on voit un document présenté à gauche dans l'interface allemande et à droite dans l'interface française. Ce ne sont pas seulement les éléments d'interface qui s'adaptent à la langue, mais également les noms des auteurs. Les données transcrites, à l'instar de la mention de responsabilité, ne s'adaptent évidemment pas puisqu'elles se doivent de représenter fidèlement le document.

{{< figure src="/img/multilingualism_display.png" caption="Vue détaillé d'un document, en allemand et en français">}}

**2. La facette auteur**

Lorsque la langue de l'interface change, la forme allemande ou française est affichée.

{{< figure src="/img/multilingualism_facet.png" caption="Facette auteur en allemand et en français">}}

**3. La barre de recherche et l'autocomplétion**

Lorsque la langue de l'interface change, les suggestions s'affichent en français ou en allemand. La recherche est bien sûr effectuée dans toutes les langues.

Dans l'image ci-dessous, l'interface est en allemand mais l'utilisateur·trice recherche en français. RERO&nbsp;ILS lui présente donc des suggestions en allemand si possible.

{{< figure src="/img/multilingualism_search.png" caption="Suggestions de recherche s'adaptant à la langue de l'interface">}}

## Catalogage avec ou sans entité

Le multilinguisme ne fonctionne donc que si un lien à une entité existe. Lorsque ce n'est pas le cas, la ou le bibliothécaire peut choisir de créer l'entité (directement dans les outils IdRef ou GND) ou de saisir un point d'accès autorisé sans entité (voir image ci-dessous).

{{< figure src="/img/multilingualism_local_entity.png" caption="Saisie des différentes informations d'un point d'accès pour une collectivité dans RERO&nbsp;ILS">}}

## Entité ou autorité?

Nous utilisons les deux mots de manière indifférente, mais préférons clairement *entité*. Effectivement, l'expression *autorité* date des renvois au sein des catalogues à fiches dans des tiroirs. A l'heure du web sémantique, il est devenu plus courant de parler d'*entités*. Celles-ci ne se limitent plus seulement à une forme retenue et des formes rejetées, mais peuvent aussi intégrer de nombreuses autres données structurées. C'est donc une terminologie que nous estimons plus appropriée.

[^1]: Le mot "agent" vient de la terminologie officielle RDA. Il regroupe les personnes, familles et collectivités.
[^2]: [IdRef](https://www.idref.fr/) est un référentiel d'autorités francophones, maintenu par l'Agence bibliographique française (ABES) et utilisé par différentes plateformes des institutions scientifiques françaises.
[^3]: [GND](https://www.dnb.de/DE/Professionell/Standardisierung/GND/gnd_node.html), pour Gemeinsame Normdatei, est un référentiel d'autorités germanophones géré par la Bibliothèque nationale allemande, mais utilisé par diverses bibliothèques allemandes, autrichiennes et suisses. GND est notamment utilisé par les bibliothèques germanophones du réseau SLSP.