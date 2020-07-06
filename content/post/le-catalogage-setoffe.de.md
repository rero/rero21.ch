---
title: "Die Katalogisierung wird erweitert"
date: 2020-07-06T08:23:38+02:00
publishdate: 2020-07-06
draft: false
tags: ["rero-ils", "release", "Erwerbungen", "Anzeige", "Metadaten", "Vorhersagen"]
slug: le-catalogage-setoffe
---

Ein neuer Sprint endet für {{< smallcaps "rero ils" >}} mit einer Version voller Neuheiten. Dank einer zunehmend stabilen technischen Grundlage kann sich das Entwicklungsteam auf nutzerorientierte Funktionalitäten konzentrieren. Die vollständigen Versionshinweise sind wie üblich auf der Github-Seite verfügbar: [`v0.10.0`][1].

<!--more-->

## Verbesserungen der Schnittstelle

Die Arbeit an den öffentlichen und professionellen Schnittstellen wird fortgesetzt. Diese Version bringt viele Anpassungen und insbesondere eine Neugestaltung des Metadaten-Editors (Katalogisierungsoberfläche), um seine Lesbarkeit zu verbessern. Der Editor nimmt jetzt die gesamte Bildschirmbreite ein, und die Felder sind optisch besser voneinander getrennt; die Titel der Hauptfelder sind jetzt fett gedruckt, und einige Unterfelder können *inline* angezeigt werden. 

{{< figure src="/img/rero-ils-editeur.png" caption="Anzeige von Unterfeldern inline statt untereinander und fettgedruckte Feldtitel">}}

## Fremddatenübernahme

Die Möglichkeit, Datensätze aus externen Katalogen zu importieren, erleichtert und rationalisiert einen Grossteil der Katalogisierungsarbeit. {{< smallcaps "rero ils" >}} bietet die Möglichkeit, dies über [das SRU-Protokoll][2] zu tun. Es besteht die Möglichkeit, im gewählten Katalog (zurzeit nur BnF) nach Stichworten (Autor, Titel, Datum, ISBN, usw.) zu suchen und den zu importierenden Datensatz auszuwählen. Dieser Datensatz kann dann in der Katalogisierungsoberfläche frei bearbeitet werden, bevor er gespeichert wird. 

## Einführung der Zeitschriftenverwaltung

Ein weiteres neues Merkmal dieser Version `v0.10.0` ist der Eingang von Zeitschriftenlieferungen. Ein Feld **Häufigkeit** im Bestand, das den [RDA-Standard][3] verwendet, ermöglicht es Ihnen, die Daten der nächsten regelmässigen Lieferungen automatisch vorauszusagen und sie mit einem einfachen Klick schnell zu empfangen. Es ist natürlich auch möglich, eine unregelmässige Lieferung zu empfangen. Das System erstellt automatisch ein Exemplar für jede erhaltene Nummer.

{{< video src="rero-ils-receiveissue" legend="Schneller Eingang einer regelmässigen Lieferung nach ihrer Häufigkeit" >}}

Im obigen Video wird ein Beispiel für einen schnellen Empfang gezeigt:

1. *Obtenir* (*Zugreifen* auf Deutsch) zeigt die Liste der Exemplare an
1. Vorhersagen für zukünftige Lieferungen werden geöffnet
1. Ein Klick auf die Schaltfläche des schellen Eingangs erstellt das Exemplar. Falls notwendig, können Sie mit der anderen Schaltfläche das Exemplar bearbeiten, bevor Sie es empfangen.

## Verschiedene Anmerkungen für das Exemplar

Schliesslich ist zu beachten, dass das Exemplar mit einem Feld "Anmerkung" erweitert wurde. Eine Anmerkung kann von vier Typen sein:

* **Öffentliche Anmerkung** : wird in der Detailansicht der öffentlichen und professionellen Schnittstellen angezeigt.
* **Interne Anmerkung** : wird nur in der Detailansicht der professionellen Schnittstelle angezeigt.
* **Rückgabeanmerkung** : erzeugt eine Meldung bei der Rückgabe.
* **Ausleihanmerkung** : erzeugt eine Meldung bei der Ausleihe.

Diese Anmerkungen entsprechen einem wichtigen Bedürfnis, das sowohl von mehreren unserer Pilotbibliotheken als auch von unseren Partnern an der UC Louvain geäussert wurde.

{{< figure src="/img/item-notes.png" caption="Die Exemplaranmerkungen in der professionellen Schnittstelle">}}

[1]: https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v0100
[2]: https://www.bnf.fr/fr/protocole-sru-vue-densemble
[3]: http://www.rdaregistry.info/termList/frequency/?language=de