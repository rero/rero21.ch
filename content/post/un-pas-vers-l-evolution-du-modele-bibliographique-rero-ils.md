---
title: "Un pas vers l'évolution du modèle bibliographique RERO ILS: l'interconnection des données"
date: 2019-08-07T08:00:00+02:00
draft: false
tags: ["rero ils", "enrichment", "lrm", "works", "bibliostratus", "data alignment"]
---

Œuvre, expression, manifestation, item, un, deux, trois, quatre... comptine entêtante à laquelle sont désormais familiarisées les personnes travaillant en bibliothèque. Et de fait, ces quatre concepts sont régulièrement scandés dans les conférences du domaine et les cours de bibliothéconomie. Plus largement, ils sont le reflet d'une évolution des modèles bibliographiques (LRM), des règles de catalogage (RDA) et des formats d'échange de données (Bibframe). Nos voisins français ont coutume de nommer cette mouvance la « transition bibliographique ». Et le projet RERO ILS n'y échappe pas, bien au contraire: il s'en imprègne pleinement. L'utilisation de Bibliostratus le montre bien.

<!--more-->

### L'outil Bibliostratus

Bibliostratus est un logiciel libre développé en France dans le cadre de la [transition bibliographique](https://www.transition-bibliographique.fr) (groupe Système et données), projet mené conjointement par l'[Abes](http://www.abes.fr/) et la [BnF](https://www.bnf.fr/). Disponible en téléchargement sur [Github](https://github.com/Transition-bibliographique/bibliostratus), Bibliostratus  permet d'aligner automatiquement des données bibliographiques avec celles du Sudoc et de la BnF[^1].

Pour ce faire, il fonctionne en trois étapes:

1. Conversion des fichiers MARC21 ou UNIMARC en fichiers `.txt` avec une sélection de champs importants
2. Alignement par interrogation de Sudoc et BnF
3. Récupération des notices complètes Sudoc ou BnF

L'étape 2, qui consiste à comparer des champs entre eux afin de déterminer si deux notices correspondent au même objet, est la plus délicate. Pour les livres, dits « monographies textuelles » en jargon, les principaux éléments de comparaison sont l'ISBN, le titre, l'auteur et la date.

Bibliostratus prend en charge l'alignement des manifestations et des autorités (personnes et collectivités). Ces dernières étant déjà interconnectées grâce à VIAF, RERO ne s'intéresse pour l'instant qu'aux manifestations.

##### Quelle utilité pour RERO ILS?

Le modèle bibliographique de RERO ILS va comporter l'entité « œuvre », actuellement absente du catalogue. Toutefois, la génération de ces œuvres de manière automatique sur la base des notices de manifestations est un processus extrêmement complexe qui nécessite des efforts importants si l'on souhaite que les données respectent la définition de l'œuvre selon LRM.

Dans la situation actuelle, RERO n'a pas les ressources pour effectuer de tels développements. Par contre, la BnF et l'Abes se donnent les moyens de réaliser ces enrichissements et alignements. Procédant par étapes et par sous-ensembles de données pour garantir une certaine qualité, la BnF a déjà intégré des milliers de liens œuvre-manifestation dans sa base de production[^2]. De son côté, l'Abes explore les possibilités de son logiciel CBS dans la même optique[^3].

Pour RERO, l'objectif à court terme est de collecter des correspondances avec les notices de manifestations de la BnF et du Sudoc, et de les intégrer dans la base de production Virtua. Ainsi, toutes les bibliothèques en bénéficieront dès 2021.

À moyen et long terme, cela permettra potentiellement de pouvoir relier certaines manifestations RERO à des notices d'œuvres de qualité produites en France.

##### Implémentation

Le catalogue RERO comporte environ 6,1 millons de manifestations, ce qui a fait quelque peu suer Bibliostratus lors de l'étape 1, du point de vue mémoire. Nous avons donc découpé le fichier en paquets de 500'000 notices. Cela nous a ensuite permis de lancer l'étape 2, la plus chronophage, en parallèle pour plusieurs fichiers, sans quoi ce traitement aurait pris plusieurs mois 😱. Le tout a été réalisé sur un PC, en voici un petit aperçu dans l'image ci-dessous:

{{< figure src="/img/bibliostratus_screen.png" caption="Bibliostratus à l'œuvre sur l'un de nos PC" alt="Capture d'écran de Bibliostratus à l'œuvre sur l'un de nos PC" >}}

### Éviter les erreurs par une méthodologie stricte

Avec les données de bibliothèque, la plupart des alignements automatiques basés sur des comparaisons de similarité génèrent des erreurs, que l'on qualifie de faux positifs: l'établissement d'une équivalence erronée.

Pour réduire au maximum ces faux positifs, l'équipe RERO a testé Bibliostratus sur un échantillon de 10'000 notices représentatives du catalogue, puis a sélectionné et évalué les résultats. Le fruit de cette analyse a été communiqué aux personnes développant le logiciel, qui ont ensuite adapté Bibliostratus.

Lors de l'étape de sélection, les données inutiles sont écartées, telles que celles ayant plusieurs équivalences pour une notice ou aucune équivalence du tout. Les données retenues sont ensuite triées par type d'algorithme de génération. Effectivement, Bibliostratus utilise selon les notices bibliographiques plus de 700 algorithmes différents pour établir des correspondances (il y a de la doc sur [Github](https://github.com/Transition-bibliographique/bibliostratus/wiki/2_annexe.-Le-m%C3%A9canisme-d'alignement)). Seuls ceux ayant généré le plus d'alignements sont retenus et évalués. À titre d'exemple, l'algorithme ayant créé le plus d'équivalences avec la BnF compare les ISBN puis les titres entiers (46% des cas).

Les faux positifs les plus courants sont des cas où deux manifestations différentes de la même expression sont mises ensemble. Dans certaines situations, on soupçonne que les deux manifestations soient de fait les mêmes, mais que les données aient été saisies de manière différente. Cela peut s'expliquer par une divergence des règles de catalogage, une divergence d'analyse de la part du catalogueur ou une erreur humaine.

Une fois la qualité d'une méthode validée, les résultats peuvent être intégrés en production, en sachant que le risque d'erreur ne peut être totalement écarté, notamment pour les documents sans ISBN. Toutefois, un faux positif ne sera en général pas totalement faux du fait qu'il regroupe quasi toujours deux manifestations de la même expression.

### Quelques chiffres de l'alignement du catalogue RERO

Les chiffres ci-dessous concernent uniquement les monographies textuelles du catalogue RERO, alignées avec la BnF de préférence, et à défaut avec le Sudoc.

{{< bootstrap-table "table table-striped table-bordered" >}}
| Résultat de l'alignement     | Fréquence | % des monographies RERO | % de tout RERO |
|:-----------------------------|----------:|------------------------:|---------------:|
| Aucune équivalence           | 2'954'451 |          65.2%          |      48.1%     |
| 1 équivalence BnF            | 1'213'557 |          26.8%          |      19.8%     |
| 1 équivalence Sudoc          |  243'569  |           5.4%          |      4.0%      |
| Plusieurs équivalences BnF   |  108'693  |           2.4%          |      1.8%      |
| Plusieurs équivalences Sudoc |   12'896  |           0.3%          |      0.2%      |
{{< /bootstrap-table >}}

Dans un premier temps, les alignements d'une seule équivalence seront intégrés en production, après validation par un contrôle qualité. Cela représente environ 15-20% de l'ensemble des notices RERO.

### Références

[^1]: Bibliostratus. Transition bibliographique des catalogues vers le web de données [en ligne]. 2 juillet 2019. [Consulté le 17 juillet 2019]. Disponible à l’adresse : https://www.transition-bibliographique.fr/systemes-et-donnees/bibliostratus/

[^2]: BNF. Programme national Transition bibliographique. Bibliothèque nationale de France [en ligne]. 2019. [Consulté le 17 juillet 2019]. Disponible à l’adresse : https://www.bnf.fr/fr/programme-national-transition-bibliographique

[^3]: ABES. La FRBRisation des données du Sudoc en questions / réponses [en ligne]. 20 octobre 2017. Abes. [Consulté le 17 juillet 2019]. Disponible à l’adresse : http://documentation.abes.fr/sudoc/autres/FRBRisationDuSudoc.pdf


