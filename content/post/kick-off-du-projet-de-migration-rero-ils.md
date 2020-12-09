---
title: "Kick-off du projet de migration RERO ILS"
publishdate: 2020-12-08
draft: false
tags: ["migration", "rero-ils", "go-live"]
slug: kick-off-du-projet-de-migration-rero-ils
---

La séance de lancement du projet de migration vers RERO ILS a eu lieu le 3 décembre en présence (virtuelle, bien sûr) des représentants des 41 bibliothèques qui font partie de l'aventure. Cela a notamment été l'occasion de rappeler le contexte du projet, de détailler les contours de la version 1.0.0, d'expliquer le mode de développement à partir de 2021, et bien sûr de présenter le calendrier de migration.

<!--more-->

## Une version 1.0.0

La nomenclature des versions répond à des [conventions][1] bien établies. Pour la première fois, nous itérerons fin décembre le premier chiffre et passerons au 1..., ce qui annonce une version plus aboutie et stabilisée. Ceci a pour but de garantir le bon fonctionnement du système en production dès juillet 2021.

[1]: https://semver.org/

Entre-temps, cette version fera l'objet de chargements complets des données des bibliothèques, afin de permettre des tests, du paramétrage et l'affinement des spécifications de migration. L'équipe de développement se concentrera sur la résolution de bugs et de petites améliorations. Elle travaillera également sur l'amélioration des performances (par exemple le chargement des pages), sur la configuration d’outils de monitoring (alerte en cas d'erreurs ou de pannes) et sur la mise en place d'un environnement de production.

## Des fonctionnalités prioritaires

La version 1.0.0 ne contient pas toutes les fonctionnalités souhaitées par les bibliothèques. C'est pourquoi l'équipe continuera de développer le système, même si les ressources à disposition seront moindres, en raison de la réduction du personnel de la Centrale, du projet de migration et du travail de stabilisation.

Les fonctionnalités prioritaires ont été déterminées en concertation avec le groupe système, qui assure le suivi de la migration et représente les 41 bibliothèques RERO ILS. Une réévaluation des priorités sera faite régulièrement en fonction des besoins.

Et après le go-live, le développement de RERO ILS se poursuivra. En effet, RERO et son partenaire l'Université catholique de Louvain garantiront la mise à jour des composantes du logiciel et contribueront à l'ajout de nouvelles fonctionnalités.

## Le projet de migration

Deux équipes de projet ont été constituées pour suivre la migration et fournir des spécifications:

* Le groupe système. Compétent pour le paramétrage, le prêt, les acquisitions, le bulletinage et les statistiques, il s'occupe également des tests, de la priorisation et des spécifications de conversion.
* Le groupe métadonnées. Responsable du catalogage et de l'interface publique, il collabore en plus aux tests, à l'affinement de la conversion des données bibliographiques ainsi qu'à la définition des processus et règles de catalogage.

La Centrale est heureuse de pouvoir compter sur l'expertise de personnes du terrain pour l'accompagner dans cette migration!

Le calendrier de migration (voir ci-dessous) comporte 4 jalons importants:

* `fin février`: 1er chargement complet
* `mars/avril`: formations de formateurs
* `fin avril`: 2e chargement complet
* `12 juillet 2021`: go-live

{{< figure src="/img/calendrier_migration.svg" caption="Calendrier de migration" alt="Calendrier de migration" link="/img/calendrier_migration.svg" >}}
