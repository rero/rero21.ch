---
title: "Towards integrating RERO authorities into the French-language IdRef reference system"
date: 2020-03-12T12:00:00+02:00
draft: false
tags: ["autorities", "idref", "rero-ils", "slsp"]
---

The RERO network will be split into two groups of libraries by 2020-2021, one integrating the Swiss Library Services Platform (SLSP) and the other adopting the {{< smallcaps "rero ils" >}} solution. In order to avoid a situation leading to the creation of two divergent copies of its current French-language authority file, RERO decided to discontinue this file in favour of a solution that is more widely recognized and firmly rooted in a wider community, and that can be equally used by both SLSP and {{< smallcaps "rero ils" >}}.

<!--more-->

An agreement of principle was reached with the [ABES (Agence bibliographique de l’enseignement supérieur, France)](http://www.abes.fr/) in July 2019 to integrate the RERO authorities *proper nouns* in the French-language [IdRef file](https://www.idref.fr/).

For libraries of French-speaking Switzerland, this solution offers many advantages:

* Continue producing French-language authorities after the transition. 
* Use and enrich a large and high-quality authority file (3.5 million authorities) which will eventually merge with the BnF (Bibliothèque nationale de France) file as part of the [FNE project](https://www.transition-bibliographique.fr/fne/fichier-national-entites/) (présenté à la [journée RERO](https://www.rero.ch/pdfview.php?section=communique&filename=JR19_FNE_journee_RERO.pdf) (presented at the RERO day in March 2019).
* Increase the visibility of RERO authorities.
* Benefit from the [MEF service](https://mef.test.rero.ch/) (Multilingual Entity File) developed by RERO with the aim of implementing multilingual metadata management in ILSs.

A more complete presentation of the scenario was given in November 2019 at the BnF, see *[Approche multilingue des autorités RERO avec le projet Multilingual Entity File](https://www.transition-bibliographique.fr/2019-09-26-inscriptions-ouvertes-4e-journee-metadonnees-bibliotheques-15-novembre-2019/)* (presentation + video, in French).

### Fundamentals of the solution

* Input by the cataloguers and indexers of the new *proper nouns* authorities directly into IdRef via the web application
* Linkage to IdRef and RERO-RAMEAU authorities by entering identifiers in the access points of bibliographic records
* Separate management of the [RERO-RAMEAU (common nouns)](https://www.rero.ch/pdfview.php?section=ressources&filename=rameau_dans_le_reseau_suisse_rero_20141106.pdf) system, which we have been adapting since 2012 to post-coordinated indexing, with monthly transfers to Alma/SLSP and MEF/{{< smallcaps "rero ils" >}}
* Regular harvesting of [IdRef's OAI PMH server](http://www.abes.fr/Autorites-et-referentiels/Services-disponibles/Entrepot-OAI-PMH-IdRef) to to Alma/SLSP and MEF/{{< smallcaps "rero ils" >}} for updates
* Transmission of the RAMEAU suggestions to the BnF by the RAMEAU correspondents of the French-speaking SLSP and RERO sites, as up to now

### Preparation stages

1. The RERO *proper nouns* authority file stops being fed before the go-live of the end of 2020
1. RERO authorities are integrated into IdRef through alignments, enrichments and additions for the persons, collective agents, geographical names and titles entities
1. IdRef is integrated into {{< smallcaps "rero ils" >}} (through MEF) and into Alma’s Community Zone in MARC 21 format

{{< figure src="/img/migration_idref.png" caption="Transition from RERO authorities to IdRef" alt="Figure: Transition from RERO authorities to IdRef" >}}

### Work progress in March 2020

ABES, RERO, SLSP and the Ex Libris company are actively collaborating in order to implement this project succesfully within the given timeframe. So far, the following developments have been carried out:

* (Very promising) alignment tests on 10’000 person authorities
* Alignments on 200’000 person authorities (in progress)
* Integration of PPN IdRef identifiers on about 200'000 bibliographic records for the third SLSP data loading test
* Mapping UNIMARC authorities -> MARC 21 authorities
* Preparation of the OAI PMH IdRef server in MARC21 version (in progress)

### Beginning of a Bachelor thesis on this project

RERO centrale is delighted to assist Etienne Attinger, a student at the HEG Geneva and also librarian at the University of Geneva, in carrying out a Bachelor thesis on the subject of the alignment of authorities. This assignment began in February and is due to end in July 2020. Its temporary title is *Study, elements of implementation and evaluation of the integration of the RERO authorities into the French-language IdRef system*.