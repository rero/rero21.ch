---
title: "Prédictions: entre haine et passion"
date: 2020-05-28T15:00:00+02:00
publishdate: 2020-05-28
draft: false 
tags: ["rero-ils", "acquisition", "prédictions", "bibliothèques pilotes"]
---

Certain·e·s les adorent, d'autres les détestent. Aujourd'hui, nous nous penchons sur les prédictions et leur périodicité parmi les données des bibliothèques pilotes de RERO ILS. Effectivement, le travail sur l'implémentation de la fonction de bulletinage mène la centrale RERO à analyser cet aspect en se basant sur les données existantes. (Pour les experts, ces prédictions se trouvent dans le champ MARC 853 des holdings.)

Après extraction des données, nous avons découvert des chiffres intéressants. Nous souhaitons les partager ici, car on y trouve certaines similitudes et différences entre bibliothèques.

<!--more-->

[Pour rappel](/rero-ils-s-expose-aux-tests), nous développons RERO ILS avec l'aide de bibliothèques pilotes, qui testent le système et nous fournissent un retour d'expérience de la part de professionnel·le·s du terrain. Nos six bibliothèques pilotes sont les suivantes:

* [Bibliothèque cantonale jurassienne](https://www.jura.ch/occ/bicj)
* [Bibliothèque de Bulle](https://musee-gruerien.ch/)
* [Bibliothèque de la Ville de la Chaux-de-Fonds](http://cdf-bibliotheques.ne.ch/)
* [Bibliothèque municipale de Delémont](http://www.delemont.ch/fr/Tourisme-culture-et-loisirs/Vie-culturelles/Bibliotheque/Bibliotheque.html)
* [Bibliothèque publique et universitaire de Neuchâtel](http://bpun.unine.ch/)
* [Médiathèque Valais](https://www.mediatheque.ch/) (et ses 4 sites de Brigue, Martigny, St-Maurice, Sion)

## Où est-on le plus friand de prédictions?

Nous sommes tombé·e·s sur ces chiffres plus ou moins par hasard; nous ne voulons donc accuser personne... mais on peut tout de même constater que les Valaisan·ne·s ont une tendance plus forte à vouloir contrôler l'entrée des fascicules 🤭

{{< bootstrap-table "table table-striped table-bordered" >}}
| Bibliothèque pilote                                     | Nombre de holdings | Nombre de holdings avec prédiction | Ratio |
|---------------------------------------------------------|-------------------:|-----------------------------------:|------:|
| Médiathèque Valais (Sion)                               |              17710 |                               3892 |   22% |
| Bibliothèque cantonale jurassienne                      |               6788 |                                993 |   15% |
| Médiathèque Valais (St-Maurice)                         |               1218 |                                141 |   12% |
| Médiathèque Valais (Brigue)                             |               2209 |                                210 |   10% |
| Bibliothèque de Bulle                                   |               2411 |                                223 |    9% |
| Bibliothèque publique et universitaire de Neuchâtel     |              18761 |                               1672 |    9% |
| Médiathèque Valais (Martigny)                           |               2333 |                                196 |    8% |
| Bibliothèque de la Ville de La Chaux-de-Fonds (sans BJ) |               7021 |                                435 |    6% |
| Bibliothèque municipale de Delémont (adultes et jeunes) |               1587 |                                102 |    6% |
{{< /bootstrap-table >}}

Nous n'avons pas approfondi l'analyse pour connaître les raisons de ces chiffres. Par ailleurs, on constate également que, à tailles comparables, la BPU Neuchâtel a beaucoup plus de holdings que La Chaux-de-Fonds. Là aussi, nous avons décidé de ne pas nous attarder sur cet aspect (nous n'excluons pas une erreur de notre part lors de l'extraction des données). Le ratio reste dans le même ordre de grandeur.

## Quelle périodicité est-elle préférée?

L'image ci-dessous présente les fréquences des prédictions pour l'ensemble des bibliothèques pilotes.

{{< figure src="/img/periodicite_globale.svg" caption="Fréquences des prédictions pour l'ensemble des bibliothèques pilotes" alt="Graphique: fréquences des prédictions pour l'ensemble des bibliothèques pilotes" >}}

Attention! Ce camembert illustre uniquement la répartition pour les publications en série faisant l'objet de bulletinage.

On constate que les annuels, trimestriels, semestriels et mensuels se partagent les ¾ du gâteau, si l'on peut s'exprimer ainsi.

## Petit benchmark des bibliothèques

Pour détailler l'analyse, nous avons sélectionné le top 5 des périodicités par bibliothèque (image ci-dessous). On peut notamment constater que:

* les bibliothèques à mission patrimoniale bulletinent plus de publications annuelles. On pense ici aux rapports d'activités et aux divers documents émis par des organes régionaux et collectés dans un but historique.
* les bibliothèques plus petites, pratiquant le moins de bulletinage (selon le tableau ci-dessus), se concentrent plutôt sur les mensuels. 

Quelques faits marquants:

* Les hebdomadaires sont plus appréciés à Delémont qu'ailleurs.
* La Bibliothèque cantonale jurassienne n'a d'yeux que pour les annuels. Par contre, si vous êtes un mensuel, ne vous promenez pas à Porrentruy, cela pourrait être dangereux pour vous.
* Martigny a un crush pour les mensuels qui ne paraissent que onze fois par an.

D'autres interprétations sont bien entendu possibles, n'hésitez pas à nous en faire part sur Twitter ([@rero_centrale](https://twitter.com/rero_centrale)) ou par e-mail ([info@rero.ch](mailto:info@rero.ch))!

{{< figure src="/img/periodicite_par_bibliotheque.svg" caption="Fréquences des prédictions par bibliothèque (top 5)" alt="Graphique: fréquences des prédictions par bibliothèque (top 5)" >}}
