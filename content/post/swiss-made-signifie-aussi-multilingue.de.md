---
title: "\"Swiss made\" bedeutet auch mehrsprachig"
publishdate: 2021-02-18
draft: false
tags: ["rero-ils", "Mehrsprachigkeit", "Entitäten"]
slug: swiss-made-signifie-aussi-multilingue
---

Mit der Integration der lokalen Autoritäten in sein Datenmodell, verwirklicht RERO&nbsp;ILS das vom MEF-Projekt versprochene und ehrgeizige Ziel der Mehrsprachigkeit. Nicht nur die Oberfläche wird in mehreren Sprachen angeboten, sondern auch die *Daten*. Das ist eine Schweizer Verpflichtung! 🇨🇭

<!--more-->

## So funktioniert Mehrsprachigkeit

Die Mehrsprachigkeit der Daten basiert auf dem Projekt [MEF - Multilingual Entity File](https://www.rero.ch/de/produits/mef). Die Projektseite erklärt im Detail, wie der Service funktioniert. Hier sind die Prinzipien zusammengefasst:

1. Bei der Katalogisierung werden Dokumente mit Akteuren[^1] verknüpft, die in den Entitätsdateien IdRef[^2] (auf Französisch) oder GND[^3] (auf Deutsch) beschrieben sind.
2. Jeden Monat führt das VIAF-System die IdRef- und GND-Entitäten zusammen, die dieselben Akteure repräsentieren.
3. MEF ruft diese Daten ab und RERO&nbsp;ILS kann dann in der öffentlichen Schnittstelle die Anzeige anpassen:
    * die IdRef-Version, wenn die Schnittstellensprache Französisch ist.
    * die GND-Version, wenn die Schnittstellensprache Deutsch ist.

Die Mehrsprachigkeit hat gewisse Grenzen:

* Sie funktioniert im Moment nur für Deutsch und Französisch.
* Sie funktioniert nur für Dokumente mit einem Link zu einer Entität, die sowohl in IdRef als auch in GND vorhanden ist (und die von VIAF geclustert wurde).
* Sie ist besonders nützlich für Namen von Körperschaften, aber weniger für Namen von Personen, die nicht von einer Sprache in eine andere übersetzt werden.

Schliesslich sind auch die Referenzdatenbanken IdRef und GND zwei wesentliche Elemente der Katalogisierung im SLSP-Netzwerk. RERO sorgt also für eine gute Dateninteroperabilität.

## Ein echter Mehrwert für die Endnutzerin und den Endnutzer

Die Mehrsprachigkeit zeichnet sich durch drei Funktionalitäten in der Oberfläche aus.

**1. Anzeige der Namen von Personen und Körperschaften für Dokumente**

Diese Namen sind in verschiedenen Teilen des Systems zu finden: Ergebnisliste, Detailansicht eines Dokuments, und Online-Lesekonto (Ausleihen, Historie, Bestellungen, usw.). Wenn die Sprache der Oberfläche geändert wird, zeigt das System die deutschsprachige oder französischsprachige Form an.

Im Bild unten wird ein Dokument präsentiert: links in der deutschen Oberfläche, rechts in der französischen Oberfläche. Nicht nur die Oberflächenelemente passen sich der Sprache an, sondern auch die Namen der Autoren. Die transkribierten Daten, wie z.B. die Verantwortlichkeitsangabe, passen sich natürlich nicht an, da sie das Dokument originalgetreu darstellen müssen.

{{< figure src="/img/multilingualism_display.png" caption="Detailansicht eines Dokuments, auf Deutsch und auf Französisch">}}

**2. Die Autorenfacette**

Wenn sich die Sprache der Oberfläche ändert, wird die deutschsprachige oder französischsprachige Form angezeigt.

{{< figure src="/img/multilingualism_facet.png" caption="Autorenfacette, auf Deutsch und auf Französisch">}}

**3. Die Suchleiste und die Autovervollständigung**

Wenn sich die Sprache der Benutzeroberfläche ändert, werden die Suchvorschläge auf Französisch oder auf Deutsch angezeigt. Die Suche wird natürlich in allen Sprachen durchgeführt.

Im Bild unten ist die Oberfläche in Deutsch, aber der Benutzer sucht in Französisch. RERO&nbsp;ILS präsentiert daher Suchvorschläge nach Möglichkeit in deutscher Sprache.

{{< figure src="/img/multilingualism_search.png" caption="Die Suchvorschläge passen sich der Sprache der Oberfläche an.">}}

## Katalogisierung mit oder ohne Entität

Mehrsprachigkeit funktioniert also nur, wenn eine Verbindung zu einer Entität besteht. Wenn dies nicht der Fall ist, kann die katalogisierende Person wählen, ob sie die Entität erstellt (direkt in den IdRef- oder GND-Tools) oder einen normierten Sucheinstieg ohne Entität eingibt (siehe Abbildung unten).

{{< figure src="/img/multilingualism_local_entity.png" caption="Eingabe der verschiedenen Informationen eines Sucheinstieges für eine Körperschaft in RERO&nbsp;ILS">}}

## Entität oder Autorität?

Wir verwenden die beiden Wörter indifferent, bevorzugen aber eindeutig *Entität*. In der Tat stammt der Ausdruck *Autorität* aus den Verweisungen innerhalb von Zettelkatalogen in Schubladen. Im Zeitalter des semantischen Webs ist es immer üblicher geworden, von *Entitäten* zu sprechen. Diese beschränken sich nicht mehr nur auf eine normierte Form und zusätzliche Sucheinstiege, sondern können auch viele andere strukturierte Daten integrieren. Daher halten wir diese Terminologie für angemessener.

[^1]: Der Begriff "Akteur" stammt aus der offiziellen RDA-Terminologie. Er umfasst Personen, Familien und Körperschaften.
[^2]: [IdRef](https://www.idref.fr/) ist eine Referenzdatenbank von französischsprachigen Autoritäten, die von der Agence bibliographique française (ABES) verwaltet wird. Sie wird von verschiedenen Plattformen französischer wissenschaftlicher Einrichtungen genutzt.
[^3]: [GND](https://www.dnb.de/DE/Professionell/Standardisierung/GND/gnd_node.html), für Gemeinsame Normdatei, ist ein Referenzdatenbank deutschsprachiger Autoritäten, die von der Deutschen Nationalbibliothek gepflegt, aber von verschiedenen deutschen, österreichischen und schweizerischen Bibliotheken genutzt wird. Die GND wird insbesondere von den deutschsprachigen Bibliotheken des SLSP-Verbundes genutzt.