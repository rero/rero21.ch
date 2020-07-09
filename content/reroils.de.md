---
title: "RERO ILS: Open Source integrietes Bibliothekssystem"
language: "de"
date: 2020-07-13
---

RERO ILS ist ein Open Source integriertes Bibliotheksverwaltungssystem (ILS), das von RERO in Zusammenarbeit mit der [Katholischen Universität Löwen (UCLouvain)](https://uclouvain.be/) entwickelt wurde. ILS ist eine englische Abkürzung für *Integrated Library System*. Dabei handelt es sich um eine Softwarekategorie, die für die Verwaltung des täglichen Bibliotheksbetriebs (Dokumentenerwerb, Ausleihe, Katalogisierung, Suche) verwendet wird und den Benutzern eine öffentliche Schnittstelle bietet.

Aus technischer Sicht basiert RERO ILS auf dem [Invenio](https://invenio-software.org) Framework, das am [CERN](https://home.cern/) entwickelt wurde.

Eine öffentliche Testinstallation ist online unter folgendem Link zugänglich: [ils.test.rero.ch](https://ils.test.rero.ch)

### Kontext von RERO

RERO ILS stellt den Grundstein des Umwandlungsprojekts [RERO 21](/de/about) dar.

Auf der Grundlage von mehr als 30 Jahren Erfahrung in der Verwaltung eines grossen Bibliotheksverbunds begann die RERO-Zentrale 2017 mit der Entwicklung von RERO ILS mit dem Ziel, bis 2021 die derzeit im Netzwerk implementierte proprietäre Software zu ersetzen. Dank eines Open Source Systems kann die Zentrale das volle Potenzial ihrer Fähigkeiten ausschöpfen, um den aktuellen und zukünftigen Bedürfnissen ihrer Mitgliedsbibliotheken bestmöglich gerecht zu werden.

Der von RERO angebotene Service RERO ILS richtet sich in erster Linie an öffentliche, Schul- und Kantonsbibliotheken und Bibliotheksnetzwerke in der Schweiz. Er ist in Französisch, Deutsch, Italienisch und Englisch erhältlich.

### Was macht RERO ILS?

Eine erste stabile Version ist für Ende 2020 geplant, die im Laufe des Jahres 2021 in der Produktion eingesetzt werden soll, mit den folgenden Funktionalitäten:

* Eine öffentliche Schnittstelle
	* Funktionen für Bibliotheksbenutzenden: Suche, persönliches Konto, Bestellungen, usw.
	* Single-Sign-On-Authentifizierungssystem
	* Eine Schnittstelle für jedes Netzwerk oder jede Organisation
	* Eine gemeinsame Schnittstelle, die alle Organisationen abdeckt
* Eine professionelle Schnittstelle
	* Verwaltung: Einstellungen von Bibliotheken und Standorten, Ausleihpolitiken
	* Benutzerverwaltung
	* Gebührenverwaltung: Verspätung, Abonnements
	* Katalogverwaltung: Suche, Beschreibung (RDA-Standard), Metadaten-Import und -Export, Exemplarverwaltung
	* Mehrsprachige Verwaltung von Autoritäten mit MEF
	* Ausleiheverwaltung: Ausleihen, Rückgaben, Verlängerungen, Bestellungen, interbibliothekarischer Dokumententransit
	* Verwaltung von fortlaufenden Ressourcen: Vorhersagen, Empfang von Lieferungen, Bestände
	* Verwaltung der Erwerbung: Budgets, Konten, Lieferanten, Bestellungen, Rechnungen
* Konsortialfunktion
	* Drei Ebenen: Organisationen, Bibliotheken, Standorte
	* Organisationen sind innerhalb des Systems unabhängig, teilen aber bibliografische Daten

Gegenwärtig befinden sich einige dieser Funktionalitäten noch in der Entwicklung.

### Early Adopter Bibliotheken

Etwa 40 Bibliotheken, die derzeit Mitglieder von RERO sind, haben ihre Absicht mitgeteilt, von der RERO ILS-Lösung zu profitieren, wobei ein Go-Live für den Sommer 2021 geplant ist. Unter ihnen arbeiten sechs Pilotbibliotheken am partizipativen Entwicklungsprozess mit:

* [Bibliothek von Bulle](https://musee-gruerien.ch/)
* [Kantonsbibliothek Jura](https://www.jura.ch/occ/bicj)
* [Mediathek Wallis](https://www.mediatheque.ch/)
* [Öffentliche und Universitätsbibliothek Neuenburg](http://bpun.unine.ch/)
* [Stadtbibliothek Delémont](http://www.delemont.ch/fr/Tourisme-culture-et-loisirs/Vie-culturelles/Bibliotheque/Bibliotheque.html)
* [Stadtbibliothek La Chaux-de-Fonds](http://cdf-bibliotheques.ne.ch/)

Ergänzt durch das Fachwissen der UCLouvain-Bibliotheken bildet diese Benutzergruppe die Bezugsbasis für die Orientierungen von RERO ILS. Das Entwicklungsteam freut sich sehr, auf diese Beteiligung zählen zu können!

### Zu RERO ILS beitragen

Sie können die neueste Version unter [ils.test.rero.ch](https://ils.test.rero.ch/) testen. Wenn Sie Fragen haben, wenden Sie sich bitte an das RERO-Team über unser [chat Gitter](https://gitter.im/rero/reroils).

Das RERO ILS [GitHub Repository](https://github.com/rero/rero-ils/) enthält Informationen darüber, wie das System installiert werden kann und wie Sie zur Entwicklung von RERO ILS beitragen können.
