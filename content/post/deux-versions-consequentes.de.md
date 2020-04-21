---
title: "Zwei bedeutende Versionen"
date: 2020-04-20T06:20:38+02:00
publishdate: 2020-04-23
draft: false 
tags: ["rero-ils", "release"]
---

Bei {{< smallcaps "rero" >}} erleben wir gerade eine Beschleunigung der
Raumzeit, insbesondere im Projekt {{< smallcaps "rero ils" >}}, und in dieser
Eile "vergassen" wir, Sie zu informieren, dass zwei neue Versionen
veröffentlicht worden sind!

Im Folgenden wird eine Zusammenfassung der zusätzlichen Funktionen dieser
Versionen angeboten, aber die detaillierten Angaben können über folgende Links
abgerufen werden:

- [`v0.6.0`](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v060)
- [`v0.7.0`](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v070)

<!--more-->

## Die Version `v0.6.0` 

Die Version `v0.6.0` (und ihre kleine Schwester `v0.6.1`, die nur eine
Nachbesserung ist, [wie ihre Versionsnummer andeutet](https://semver.org
"Erklärungen zur semantischen Versionierung")) trennt die öffentliche
Schnittstelle von der professionellen Schnittstelle. Die öffentliche
Schnittstelle, die für alle mit oder ohne Authentifizierung zugänglich ist,
umfasst den gemeinsamen Katalog und die Kataloge der Organisationen sowie die
Leserkonten und die ihnen zur Verfügung stehenden Aktionen, wie z.B. die
Bestellung eines Exemplars. Die professionelle Schnittstelle bietet Zugang zu
allen Aktionen, die vom Bibliothekspersonal durchgeführt werden, wie z.B. die
Suche im Katalog, die Katalogisierung oder die Parametereinstellung.

Diese logische Trennung ist zum Teil die Folge der Einführung von
Organisationssichten in der Version `v0.3.0`[^1]. Es wurde schwierig, die
möglichen Aktionen zu definieren und klar darzustellen, die von einem
Mitarbeitenden bei einer bestimmten Anzeige zu ergreifen sind, oder die
Informationen, die für irgendwelchen Besucher oder für eine eingeloggte
Benutzerin gemeint sind. Darüber hinaus profitiert die professionelle
Schnittstelle davon, dass sie dynamisch ist, um ein erneutes Aufladen der Seite
nach jeder Aktion zu vermeiden, während die öffentliche Schnittstelle einfacher
von Suchmaschinen indiziert werden kann, wenn die Seiten statisch sind, was für
bibliographische Datensätze relevant ist. Schliesslich erlaubt diese Wahl,
einen Teil der professionellen Schnittstelle zwischen den Projekten 
{{< smallcaps "rero ils" >}} und [{{< smallcaps "sonar" >}}](https://sonar.ch)
zu verteilen und somit die Entwicklungsanstrengungen zu bündeln[^2].

Die Entwicklung von `v0.6.0` wurde massgeblich durch die durchgeführten
[Workshops](/de/tags/workshops) und die Einrichtung einer spezifischen Instanz
für [die Tests von Pilotbibliotheken](/de/rero-ils-s-expose-aux-tests)
bestimmt. Unter diesem Blickpunkt ist es nun möglich, die Anzeigen
verschiedener Organisationen mit einer spezifischen Header-Farbe und einem
spezifischen Logo anzupassen. Am wichtigsten ist, dass die Prozesse für die
Datenmigration von Virtua nach {{< smallcaps "rero ils" >}} vervollständigt
wurden, um echte Daten für eine {{< smallcaps "rero" >}}-Institution zu
importieren.

Die Schnittstelle für das Ausleihmodul wurde neu gestaltet und bietet nun mehr
Informationen über Ausleihereignisse bei der Rückgabe bestellter, verspäteter
oder im Transit befindlicher Exemplare. Die Bibliothekarin oder der
Bibliothekar hat jetzt eine einheitliche Sicht auf das Leserkonto in
verschiedenen Tabs: ausgeliehene Exemplare, Bestellungen, Gebühren, persönliche
Informationen. Was die öffentliche Schnittstelle betrifft, so bietet das Konto
auch neue Funktionalitäten wie die Verlängerung von Ausleihen, den Zugriff auf
die Ausleihhistorie und die Stornierung von Bestellungen.

Die Arbeit am Datenmodell mit den Feldern für Veröffentlichungsangabe und
Ausgabevermerk, sowie mit einem Editor, der die Einbettung von Feldern auf vier
oder mehr Ebenen unterstützt, wird fortgesetzt. Schliesslich hat die Arbeit am
Erwerbungsmodul begonnen, mit dem Hinzufügen von Geschäftsjahren, Konten,
Bestellungen, Bestellzeilen und Lieferanten.

## Die Version `v0.7.0` 

Bibliotheksmitarbeitenden können nun ein Exemplar für eine Leserin oder einen
Leser bestellen, wie in der untenstehenden Animation gezeigt. Fachleute haben
einen Tab für die Lesergebühren mit der Möglichkeit, die Gebühren teilweise
oder ganz zu bezahlen, sie zu annullieren, als bestritten zu kennzeichnen oder,
im Gegenteil, einen Streitfall zu lösen. Für die Gebühren gibt es eine
detaillierte Historie mit den Details aller Ereignisse. Diese Gebühren werden
automatisch generiert, wenn eine Ausleihe die Rückgabefrist überschritten hat.
Später werden sie auch im Zusammenhang mit anderen Bibliotheksdiensten sein,
wie Fotokopien, Fernleihen, Abonnements, Beschädigungen oder Verlust eines
Exemplars.

{{< video src="request_as_a_librarian" legend="Eine Bestellung für eine Leserin oder einen Leser aufgeben" >}}

Du côté du modèle de données, un travail complexe a été réalisé pour le titre et
les transformations nécessaires pour passer du MARC au JSON, ainsi que sur les
adresses URL. Enfin, un wiki a été ajouté afin de rédiger en ligne l'aide
professionnelle.

Beim Datenmodell wurden komplexe Arbeiten für den Titel sowie für die
URL-Adressen durchgeführt, insbesondere für die erforderliche Umstellung von
MARC auf JSON. Ein Wiki wurde ebenfalls hinzugefügt, um eine Online-Hilfe für
Fachleute zur Verfügung zu stellen.

[^1]: Siehe die [Versionshinweise](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v030). 
[^2]: Für diejenigen, welche hinter die Fassade schauen möchten, hat diese
  Änderung zur Erstellung von zwei weiteren Repositorien auf GitHub geführt,
  für zwei Angular Projekte: [ng-core](https://github.com/rero/ng-core), das
  die Gemeinsamkeiten von {{< smallcaps "rero ils" >}} und {{< smallcaps
  "sonar" >}}zusammenführt, sowie
  [rero-ils-ui](https://github.com/rero/rero-ils-ui), das die {{< smallcaps
  "rero ils" >}} Version der professionellen Schnittstelle implementiert.
