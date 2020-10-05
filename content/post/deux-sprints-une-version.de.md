---
title: "Zwei Sprints, eine Version"
publishdate: 2020-10-05
draft: false
tags: ["rero-ils", "release", "tests", "pilotbibliotheken", "autoritäten"]
---

Das RERO ILS-Team hat in den letzten zwei Monaten an den Sprints [33](https://tree.taiga.io/project/rero21-reroils/taskboard/sprint-33-108) und [34](https://tree.taiga.io/project/rero21-reroils/taskboard/sprint-34-93) der Entwicklung gearbeitet. Diese Arbeit hat zu einer Version `v0.12.0` geführt, die reich an neuen Funktionen ist und für die zweite Testphase der Pilotbibliotheken eingesetzt wird, die Ende September begann. Hier sind die wichtigsten Änderungen in dieser Version, deren vollständige Versionshinweise auf Github [`v0.12.0`](https://github.com/rero/rero-ils/blob/dev/RELEASE-NOTES.rst#v0120) zu finden sind.

<!--more-->

## Links zu Personenautoritäten als Beitragende

Ein neues Feld "Beitrag" ersetzt das Feld "Autor", so dass die Katalogisierung der Dokumente im Einklang mit den aktuellen Standards, insbesondere den RDA-Regeln, ist. Die Dokumente sind mit den Beitragenden verlinkt, deren Autoritäten aus verifizierten Quellen (IdRef und GND) stammen. Die Rolle jedes Akteurs bei der Erstellung eines Dokuments wird ebenfalls mit einem RDA-Beziehungscode angegeben. Wenn eine Autorität nicht in den Referenzquellen vorhanden ist, kann die Person auch als Zeichenkette im gleichen Feld erfasst werden.

{{< figure src="/img/contribution.jpg" caption="Das neu hinzugefügte Feld `Beitrag` im Datenmodell des Dokuments">}}

## Dichte des Ausleihmoduls unter Kontrolle

Viel Arbeit hinter den Kulissen wurde am Backend des Zirkulationsmoduls geleistet, um die bei den ersten Pilottests im März 2020 beobachteten Probleme zu lösen und alle identifizierten [Zirkulationsaktionen](https://github.com/rero/rero-ils/blob/dev/doc/circulation/actions.md) korrekt umzusetzen. Andererseits wurden auch automatisierte Tests entwickelt, um die korrekte Funktion dieses Moduls mit jeder neuen Version überprüfen zu können und um unerwartete Fehler bei der Arbeit an anderen Teilen der Software aufzudecken.

## Sie brauchen Hilfe?

Mit der ständigen Weiterentwicklung der Funktionalitäten von RERO ILS war es notwendig, den Betrieb von RERO ILS für die Endbenutzerin und den Endbenutzer zu dokumentieren. Dies ist nun getan mit einer [Hilfeplattform](https://ils.test.rero.ch/help/home/), die über die professionellen und öffentlichen Schnittstellen von RERO ILS zugänglich ist. Diese Anwendung bietet auf der gleichen Plattform die öffentliche und professionelle Hilfe von RERO ILS, um die Benutzer·innen zu führen und ihre Ausbildung zum Tool zu unterstützen.

{{< figure src="/img/public-help.JPG" caption="Die RERO ILS-Hilfeschnittstelle, die unter [flask-wiki](https://github.com/rero/flask-wiki) entwickelt wurde.">}}

## Auflistung von Neuerwerbungen

Ein Feld, das für die Aufwertung von Sammlungen interessant sein dürfte, wurde im Datenmodell des Exemplars implementiert: `new_acquisition`. Dieses Feld wird verwendet, um anzugeben, ob ein Exemplar gemäss den Kriterien jeder Bibliothek zu den _Neuerwerbungen_ gehören soll. Dies ermöglicht es, bestimmte Dokumente von dieser Liste auszuschliessen (historische Dokumente, Rückkäufe, ältere Bücher oder andere). Dieses Feld enthält auch ein Datum, das zur Erstellung von URLs zur Anzeige einer Liste von Neuerwerbungen für eine Bibliothek verwendet werden kann. Diese Liste kann nach Datum, aber auch nach anderen Kriterien (Ort, Status, usw.) gefiltert werden, was eine grosse Flexibilität bietet.

Eine häufige Anwendung dieser Funktion ist die Möglichkeit, direkt von der Website einer Bibliothek auf die Liste der Neuerwerbungen eines bestimmten Monats zu verlinken. Die erstellten URLs sind dauerhaft und verweisen direkt auf eine Liste von Dokumenten in der öffentlichen Schnittstelle von RERO ILS. Der Aufbau von URLs für diese Listen ist auch in der [professionellen Hilfe (zurzeit nur auf Französisch)](https://ils.test.rero.ch/help/recherche/#nouvelles-acquisitions) dokumentiert. 

## Übernahme externer Datensätze über API

Schliesslich umfassen die neuen Funktionen von der `v0.12.0` einen API-Zugangspunkt, der es einem authentifizierten Benutzer ermöglicht, `marcxml`-Daten mit Hilfe eines externen Skripts oder einer externen Anwendung direkt in RERO ILS zu importieren. Im Rahmen unserer Pilotbibliotheken wird die Software [EZPump](http://www.ngscan.com/ezpump/) verwendet, um MARC-Datensätze aus vielen Datenbanken zu importieren. Es wird derzeit für die Anpassung an die RERO ILS-Umgebung über diesen Zugangspunkt getestet.

## Zweite Phase der Pilottests

Diese Version ist auch eine Gelegenheit, unsere Zusammenarbeit mit unseren [Pilotbibliotheken](/de/reroils/early_adopters/) fortzusetzen. Tatsächlich wurde die zweite Welle von Tests am 24. September gestartet. Die Zentralstelle freut sich, mit der Médiathèque de Monthey einen neuen Partner für diese Tests zu gewinnen.