---
title: "Aligner les autorités RERO avec celles d’IdRef : le travail est en cours"
date: 2020-07-28T15:10:18+02:00
publishdate:
draft: false
tags: ["autorités", "métadonnées", "data-alignment", "idref", "rero-ils", "slsp"]
---

La migration prochaine des données de RERO dans [SLSP][1] et RERO ILS implique de traiter non seulement des notices bibliographiques, mais également des notices d'autorité : plus de 2.5 millions d'autorités personnes, collectivités, titres et noms géographiques ont été créées par le réseau  au fil des années. Qu'adviendra-t-il de cette précieuse base de données à l'horizon 2021 et quel traitement doit être entrepris ? Etienne Attinger s'est penché sur ces questions dans le cadre d'un travail de Bachelor en information documentaire de la HEG Genève (annoncé dans un [billet précédent](/vers-l-integration-des-autorites-rero-dans-le-referentiel-francophone-idref/)), mandaté et suivi par RERO.

<!--more-->

## IdRef, un outil de production collaboratif pour les autorités

Fruits d'un travail de catalogage et d'indexation de longue haleine, les autorités de RERO sont un enjeu de taille pour les institutions et leurs usagers et usagères, quel que soit le nouveau logiciel de bibliothèque qui sera utilisé. Dans ce contexte, ces notices d'autorité seront intégrées au référentiel d’autorités francophone du réseau SUDOC (réseau des bibliothèques de l’Enseignement supérieur français) géré par l’[ABES](2) via l'application [IdRef][3].

IdRef est un outil de production qui permet une alimentation et une exploitation indépendantes et extérieures au SUDOC. Il peut être utilisé par des systèmes de bibliothèques distincts. L’application est ouverte et dispose d’un triple store RDF, elle participe ainsi pleinement au [web des données (Linked Data)][4]. Le réseau SUDOC est, tout comme RERO, partie prenante du projet [VIAF][5], qui a pour but d’aligner internationalement les autorités de nombreuses bibliothèques nationales et réseaux, leur offrant une visibilité importante.

{{< figure src="/img/viaf.png" caption="Exemple d'un cluster d'autorité VIAF">}}

L’objectif du projet est d’aligner les autorités noms propres RERO (personnes, collectivités, titres et lieux) avec celles déjà présentes dans IdRef ainsi que d’enrichir IdRef soit par des ajouts d’autorités, soit par des ajouts d’informations non présentes. L’enjeu est celui de la conservation d’un travail long de plusieurs décennies fait par tou·te·s les professionnel·le·s ayant travaillé sur les autorités du catalogue RERO. Du reste, un certain nombre de ces notices sont d’importance régionale et/ou patrimoniale.

## En finir avec la double saisie pour les “sujets” noms propres et les “auteurs”

Jusqu’ici les autorités personnes et collectivités RERO étaient produites de manière séparée selon leur rôle vis-à-vis du document catalogué : un fichier contenait les autorités ATC (Auteur-Titre-Collectivité), et un autre les autorités-matières (lorsqu’une entité est sujet et non contributrice pour un document). Dans IdRef, une entité fait l’objet d’une seule notice d’autorité quel que soit son rôle sur le document. Le travail d’alignement permettra ainsi de réaliser un projet en attente depuis longtemps : la fusion des autorités ATC et matières RERO.

## Analyse des données

Le travail d'Etienne Attinger avait pour but d'évaluer et analyser des données fournies par l'ABES et résultant d'alignements automatiques, afin de définir et documenter les traitements et vérifications manuels requis avant la migration des données. Ce travail est impératif pour limiter les erreurs d'alignement.

Les tests d'alignement ont débuté à l'ABES sur des échantillons d'autorités "personnes" permanentes fournis par RERO : d'abord 10'000, puis 80'000, et enfin 200'000 notices. Ces données ont été comparées par machine à celles d'IdRef en plusieurs fois via un logiciel dédié nommé _QE_ (prononcer "key") : 
- Une première comparaison se fait entre les données de RERO et celles d'IdRef
- Une seconde comparaison avec les données de VIAF permet d'améliorer et consolider les premiers résultats
- Enfin, les alignement VIAF entre les autorités RERO et celles de la BnF sont à leur tour utilisés pour comparer les données et aligner le plus d'autorités possible

L'ABES a ensuite fourni à RERO des fichiers contenant les conflits, doublons et autres incertitudes à résoudre manuellement. Malgré l'efficacité impressionnante du traitement logiciel de ces alignements par l'ABES, environ 2.3% des alignements doivent encore bénéficier d'un travail manuel de vérification afin d'être pleinement validés. La pratique habituelle de RERO de n'indiquer les dates de vie d'un auteur qu'en cas de doublon interne s'est révélée être un handicap, parmi d'autres, pour ce travail d'alignement. Le fait que les autorités ATC et matières soient traitées par RERO dans deux bases de données séparées qui doivent être fusionnées pour cette migration, tel qu'indiqué plus haut, complique également ce processus.

{{< figure src="/img/alignements.png" caption="Exemple d'un problème d'alignement identifié par _QE_ et nécessitant une vérification manuelle">}}

## Quel travail concret ?

Dans l'idéal, les bibliothécaires du réseau devraient vérifier manuellement plusieurs séries d'autorités fournies par le logiciel de l'ABES. Selon les résultats obtenus par le logiciel d'alignement, ces cas sont plus ou moins complexes et demandent un temps de traitement variable. L'auteur a identifié et documenté les procédures requises tout en estimant le temps que pourraient prendre ces vérifications. Seuls les alignements vérifiés ou considérés comme valides seront intégrés aux notices RERO pour les migrations de fin 2020 et 2021.

En multipliant les estimations de temps de traitement par le nombre de notices identifiées et en extrapolant le résultat obtenu pour les échantillons de notices à la totalité du fichier, on obtient un résultat d'environ 5'212 heures de travail pour ces vérifications. "Ramené à une équipe de 5 personnes à plein temps cela représenterait au bas mot 26 (!) semaines de travail."

Il est évident que le temps et les ressources manquent à toutes les bibliothèques du réseau, actuellement aux prises avec la préparation d'une migration d'envergure. Néanmoins, la richesse du catalogue d'autorités de RERO mérite qu'on ne laisse pas cet élément de côté, comme le constate Etienne Attinger dans son travail. C'est pourquoi les travaux concrets de vérification ont d'ores et déjà commencé dans les bibliothèques de RERO afin que le plus d'autorités possible soient alignées avec IdRef avant les migrations. La Commission de catalogage (COCA) et le Groupe Indexation ont ensemble récemment priorisé et réparti ce travail et les bibliothécaires sont à l'oeuvre pour vérifier les alignements incertains identifiés par l'ABES dans les échantillons d'autorités traités.

## Bilan de la centrale

L'équipe de la centrale, représentée dans ce travail par Thierry Clavel, est très satisfaite du déroulement de ce projet et des perspectives de collaboration qu'il ouvre. Elle remercie vivement Etienne Attinger pour la réalisation de ce travail, ainsi que l'ABES pour son accompagnement et les compétences mises à disposition.

__Référence :__ ATTINGER, Etienne, 2020. _Étude, éléments de réalisation et évaluation de l’intégration des autorités RERO dans le référentiel francophone IdRef_. Genève : Haute école de gestion de Genève. Travail de Bachelor.

[1]: https://slsp.ch/
[2]: http://www.ABES.fr/Autorites-et-referentiels/IdRef-Identifiants-et-Referentiels
[3]: https://www.idref.fr/
[4]: https://fr.wikipedia.org/wiki/Web_des_données
[5]: https://viaf.org/