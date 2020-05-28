---
title: "Eine ziemlich reichhaltige Version"
publishdate: 2020-06-04
draft: false 
tags: ["rero-ils", "release", "suche", "ausleihe", "metadaten", "anzeige"]
---

Eine neue Version von {{< smallcaps "rero ils" >}} wurde veröffentlicht,
ziemlich reich an Neuheiten, was uns natürlich erfreut. Nachstehend finden Sie
eine kurze Zusammenfassung der wichtigsten neuen Funktionen. Die vollständigen,
aber technischen Versionshinweise sind über das GitHub-Projekt erhältlich:
[`v0.9.0`][1].

<!--more-->

## Verbesserung der Suche

Das Bibliothekarteam besteht schon seit langem darauf, und die [Tests der
Pilotbibliotheken][2] haben es bestätigt: bei der Suche in einem
Bibliothekskatalog wird die Anwendung der booleschen Operators `UND` als
Standard erwartet, um die Relevanz zu erhöhen, auch wenn kein Ergebnis gefunden
wird. Dies ist nun erfolgt. Gleichzeitig wurden die Datenindexierung und die
Suchfunktionalitäten überarbeitet, und die Verbesserungen sind bemerkbar.

## Geschlossene Silos

[UCLouvain][3], der aktiv an der Entwicklung von {{< smallcaps "rero ils" >}}
mitarbeitet, hatte die Implementierung von *geschlossenen Silos* vorgeschlagen,
d.h. die Möglichkeit, für jeden Standort die Bestellungen zu blockieren oder
die Abholorte einzuschränken. Sobald gesagt, sobald getan: [UCLouvain][3] hat
diese Funktionalität entwickelt.

{{< figure src="/img/rero-ils-paging.png" caption="Bearbeitung eines Standortes, mit Einschränkung der möglichen Abholorte." >}}

## Manuelle Sperrung von Leserinnen und Lesern

Es ist nun möglich, eine Leserin oder einen Leser manuell zu blockieren. Eine
freie Textnotiz kann hinzugefügt werden, um den Grund für die Sperrung zu
erklären. Die gesperrte Person kann keine Bücher mehr ausleihen oder
Bestellungen vornehmen. In ihrem Konto wird sie über die Sperre und den Grund
dafür informiert. Der Bibliothekar wird auch benachrichtigt, wenn
Ausleihvorgänge nicht mehr möglich sind (Ausleihe oder Bestellung für diese
Person).

## Metadaten und Anzeige der Datensätze

Die Arbeit an der Implementierung des Datenmodells setzt sich in den Bereichen
der physischen Beschreibung der Dokumente fort: Umfang, Dauer, Format,
Illustrationen, Farben und Begleitmaterial. Diese Felder basieren eindeutig auf
dem RDA-Standard, mit einer feineren Granularität, während in 
{{< smallcaps "marc" >}} verschiedene Arten von Informationen innerhalb 
desselben Unterfeldes gruppiert wurden. Bei der Arbeit an der Anzeige dieser
Felder im Datensatz (in der Detailansicht der Dokumente) wurde die Anzeige
überarbeitet und verbessert: wesentliche Informationen werden oben
hervorgehoben und zusätzliche bibliografische Angaben erscheinen in einem
eigenen Tab.

{{< video src="new-document-detailed-view" legend="Reorganisation des bibliographischen Datensatzes (professionelle Schnittstelle)" >}}


[1]: https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v090
[2]: /de/rero-ils-s-expose-aux-tests/
[3]: https://uclouvain.be/en/libraries
