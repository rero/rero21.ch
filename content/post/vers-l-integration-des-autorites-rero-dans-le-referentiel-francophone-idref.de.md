---
title: "Zur Integration der RERO-Autoritäten in das französischsprachige Referenzsystem IdRef"
date: 2020-03-12T12:00:00+02:00
draft: false
tags: ["autoritäten", "idref", "rero-ils", "slsp"]
---

Das RERO-Netzwerk wird im Zeitraum 2020-2021 in zwei Bibliotheksgruppen aufgeteilt, von denen einige die Swiss Library Services Platform (SLSP) integrieren und andere die RERO ILS Lösung übernehmen. Um zu vermeiden, dass diese Situation zur Schaffung von zwei unterschiedlichen Kopien seiner derzeitigen französischsprachigen Autoritätsdatei führt, wollte RERO die Unterstützung seiner Autoritäten aufhören. Stattdessen soll eine Lösung eingesetzt werden, die in einer breiteren Gemeinschaft anerkannt und verankert ist und die gleichzeitig von SLSP und RERO ILS übernommen werden kann.

<!--more-->

Im Juli 2019 wurde eine grundsätzliche Vereinbarung mit der [ABES (Agence bibliographique de l’enseignement supérieur, Frankreich)](http://www.abes.fr/) getroffen, um die RERO-Autoritäten *Eigennamen* in die französischsprachige [IdRef-Datei](https://www.idref.fr/) zu integrieren.

Für die Bibliotheken der Westschweiz hat diese Lösung viele Vorteile:

* Nach dem Übergang weiterhin französischsprachige Autoritäten produzieren.
* Eine grosse und qualitativ hochwertige Autoritätsdatei (3,5 Millionen Autoritäten) nutzen und anreichern, welche mittelfristig mit der der BnF (Bibliothèque nationale de France) im Rahmen des [FNE-Projekts](https://www.transition-bibliographique.fr/fne/fichier-national-entites/) (vorgestellt auf der [RERO-Tagung](https://www2000.rero.ch/pdfview.php?section=communique&filename=JR19_FNE_journee_RERO.pdf) im März 2019) zusammengeführt wird.
* Die Sichtbarkeit der RERO-Autoritäten erhöhen.
* Den [MEF-Service](https://mef.test.rero.ch/) (Multilingual Entity File) in Anspruch nehmen, der von RERO mit dem Ziel entwickelt wird, eine mehrsprachige Metadatenverwaltung in Bibliothekssystemen umzusetzen.

Eine vollständigere Präsentation des Szenarios wurde im November 2019 an der BnF gemacht, siehe *[Approche multilingue des autorités RERO avec le projet Multilingual Entity File](https://www.transition-bibliographique.fr/2019-09-26-inscriptions-ouvertes-4e-journee-metadonnees-bibliotheques-15-novembre-2019/)* (Präsentation + Video, auf Französisch).

### Prinzipien der Lösung

* Erfassung der neuen Autoritäten *Eigennamen* durch die Katalogisierenden direkt in IdRef über die Webanwendung
* Erstellung von Verbindungen zu den Autoritäten IdRef und RERO-RAMEAU durch Eingabe von Identifikatoren in den Sucheinstiegen der Titelaufnahmen
* Getrennte Verwaltung des [RERO-RAMEAU-Datensatzes (Substantive)](https://www2000.rero.ch/pdfview.php?section=ressources&filename=rameau_dans_le_reseau_suisse_rero_20141106.pdf), welchen wir seit 2012 an die postkoordinierte Indexierung anpassen, mit monatlichen Übertragungen nach Alma/SLSP und MEF/RERO ILS
* Regelmässiges Harvesting des [OAI PMH-Servers von IdRef](http://www.abes.fr/Autorites-et-referentiels/Services-disponibles/Entrepot-OAI-PMH-IdRef) nach Alma/SLSP und MEF/RERO ILS für Updates
* Übermittlung der RAMEAU-Vorschläge an die BnF durch die RAMEAU-Korrespondenten der französischsprachigen SLSP- und RERO-Stellen, wie bisher

### Vorbereitende Schritte

1. Einstellung der Erfassung von RERO-Autoritäten *Eigennamen* vor den Go-Live Ende 2020
1. Integration der RERO-Autoritäten in IdRef durch Interlinking, Anreicherungen und Einfügungen für die Entitäten Personen, Körperschaften, Geografika und Werktitel
1. Integration von IdRef in RERO ILS (über MEF) und in die Alma Community Zone in MARC 21

{{< figure src="/img/migration_idref.png" caption="Übergang der RERO-Autoritäten zu IdRef" alt="Schema: Übergang der RERO-Autoritäten zu IdRef" >}}

### Stand der Fortschritte im März 2020

ABES, RERO, SLSP und die Firma Ex Libris arbeiten aktiv zusammen, um dieses Projekt innerhalb der vorgesehenen Zeit zu verwirklichen. Insbesondere wurde folgendes durchgeführt:

* Interlinking-Tests (vielversprechend) mit 10'000 Personenautoritäten
* Interlinking von 200'000 Personenautoritäten (in Arbeit)
* Integration von IdRef PPN-Identifikatoren in etwa 200'000 bibliographische Einträgen für den dritten SLSP-Test (Laden von Daten)
* Mapping UNIMARC Autoritäten -> MARC 21 Autoritäten
* Vorbereitung des OAI PMH-Servers von IdRef in der MARC21-Version (in Arbeit)

### Beginn einer Bachelor-Arbeit zu diesem Projekt

Die Zentrale freut sich sehr, Etienne Attinger, Student an der HEG Genève und gleichzeitig Bibliothekar an der Universität Genf, bei der Realisierung einer Bachelorarbeit zum Thema des Interlinkings von Autoritäten zu begleiten. Dieser Auftrag begann im Februar und soll im Juli 2020 enden. Sein vorläufiger Titel lautet *Studie, Umsetzungselemente und Bewertung der Integration der RERO-Autoritäten in das französischsprachige IdRef-Referenzsystem*.
