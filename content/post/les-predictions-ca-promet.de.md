---
title: "Die Vorhersagen? Das kann ja heiter werden!"
date: 2020-05-05T07:14:42+02:00
publishdate: 2020-05-06
draft: false 
tags: ["rero-ils", "release"]
---

Während der [Sprint
29](https://tree.taiga.io/project/rero21-reroils/wiki/sprint-info-page-29)
vorbei ist und der [Sprint
30](https://tree.taiga.io/project/rero21-reroils/wiki/sprint-info-page-30)
bereits begonnen hat, wird die [Version
`v0.8.0`](https://github.com/rero/rero-ils/releases/tag/v0.8.0) von 
{{< smallcaps "rero ils" >}} veröffentlicht ([vollständige
Versionshinweise](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v080)).
Es folgt ein kurzer Überblick der Neuigkeiten.

<!--more-->

Die Vorhersagen für Zeitschriften werden möglich, und zwar mit einer
Flexibilität, die es erlaubt, die häufigsten Fälle zu kodieren. Genauer gesagt
können die *Holdings* von fortlaufenden Publikationen bearbeitet werden, und
ein Teil des Formulars ist der Vorhersage gewidmet. Diese wird in zwei
Schritten erstellt: zuerst definiert man die Sequenz selbst, und dann kann man
ihre Anzeige, mittels eines *template*-Mechanismus, einstellen. Zehn der
häufigsten Vorhersagen in den RERO-Mitgliedsbibliotheken wurden erfolgreich
importiert.

## Transaktionshistorie

Das Benutzerkonto, wie es vom Fachpersonal gesehen wird, ist mit einem Reiter
angereichert, der die Transaktionshistorie anzeigt. Im Moment und in
Übereinstimmung mit den geltenden Richtlinien enthält diese Historie nur die
Transaktionen der letzten sechs Monate. In Zukunft kann die Leserin oder der
Leser entscheiden, ob diese Geschichte zugänglich sein wird oder nicht. Für das
ordnungsgemässe Funktionieren von Bibliotheken wird jedoch weiterhin eine
zeitlich begrenzte Transaktionsgeschichte von einem Exemplar erforderlich sein.

## Jährliche Abonnements

Die Gebührenverwaltung ermöglicht nun Jahresabonnements, was einer bestehenden
Praxis in einigen Kantonen oder Gemeinden der Schweiz entspricht.

## Manuelle Bearbeitung der Bestellungsliste

Die Bibliothekarin oder der Bibliothekar konnte bis jetzt eine Bestellung für
einen Benutzenden stellen, nun kann er auch die Liste der vorhandenen
Bestellungen auf ein Exemplar bearbeiten, um eine Bestellung hinzuzufügen oder
zu löschen, oder um den Abholort zu ändern.

## Suchergebnisse nach Organisation gefiltert

Die Suche in der professionellen Schnittstelle filtert nun die Ergebnisse auf
der Grundlage der Organisation der eingeloggten Person, denn diese Person
arbeitet am häufigsten mit den zu ihrem Netzwerk gehörenden Exemplaren. Eine
neue hierarchische Facette, bei der die betreffende Organisation standardmässig
ausgewählt ist, ermöglicht es, die Ergebnisse auf eine bestimmte Bibliothek zu
beschränken, oder im Gegenteil, sie auf den gesamten Katalog aller
Organisationen von {{< smallcaps "rero ils" >}} auszudehnen. So kann man zum
Beispiel ein Exemplar zu einem bibliographischen Record anhängen, der nur in
einer anderen Organisation existiert.\
Dieser Standardfilter gilt auch für Suchvorschläge im Hauptsuchfeld.

{{< video src="ils-pro-result-filter" legend="Standardfilterung der Surchergebnisse" >}}

## Integration der IdRef-Autoritäten IdRef in MEF

Abschliessend kann festgestellt werden, dass die Personenautoritäten des
IdRef-Referenzsystems dem mehrsprachigen Autoritätsserver
[{{< smallcaps "mef" >}}](https://mef.test.rero.ch) hinzugefügt wurden und in
{{< smallcaps "rero ils" >}} sichtbar sind. Dies wurde im Hinblick auf den Tag
durchgeführt, an dem die {{< smallcaps "rero" >}}-Autoritäten in IdRef migriert
werden.
