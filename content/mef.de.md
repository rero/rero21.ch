---
title: "MEF: Multilingual Entity File"
language: "de"
date: 2020-08-18
---

# Was MEF tut

MEF ist ein Instrument, das Entitäten (oder Autoritäten) in mehreren Sprachen zusammenführt und sie zur Verfügung stellt, was insbesondere ermöglicht:

* Für den Endnutzer und die Endnutzerin: Suche und Anzeige des Inhalts (und nicht nur der Schnittstelle) in der eigenen Sprache
* An Bibliotheken: so viel wie möglich internationale Repositorien (GND, IdRef...) wiederverwenden. Sie können daher die Verwaltung einer lokalen Autoritätsdatei aufgeben und sich dem Semantic Web zuwenden.

MEF ist eine API, die Daten für andere Systeme, insbesondere für ILS, zur Verfügung stellt. Von daher kann MEF von mehreren verschiedenen Schnittstellen genutzt werden. RERO ILS verwendet es zum Beispiel. Dieser Service hat keine eigene Benutzerschnittstelle.

RERO entwickelt diese Dienstleistung in einer offenen Art und Weise und stellt sie derzeit in einer Testversion unter [mef.test.rero.ch](https://mef.test.rero.ch "Der MEF-Service, frei zugänglich") zur Verfügung.

# Arten von Entitäten

MEF wird schliesslich die Typen von Ressourcen enthalten, die in den Standards RDA und [Library Reference Model] (https://www.ifla.org/publications/node/11412 "Library Reference Model, auf der IFLA-Website") spezifiziert sind:

* Personen
* Körperschaften
* Werke
* Sachbegriffe
* Orte
* Perioden
* Expressionen

# Wie es funktioniert

MEF ruft Entitäten aus verschiedenen Quellen (GND, IdRef, etc.) ab und synchronisiert sich mit ihnen. Es aggregiert sie automatisch über [VIAF](https://viaf.org "Virtual International Authority File Website") und leitet daraus (derzeit) deutsche und französische Display-Labels ab, wenn verfügbar.

Die Entitäten selbst werden direkt an der Quelle in Absprache mit der herausgebenden Institution gepflegt und bearbeitet. Es werden keine Entitäten direkt in MEF erstellt oder bearbeitet.

{{< figure src="/img/mef_fonctionnement.svg" caption="Funktionieren von MEF" alt="Grafix des Funktionierens von MEF" >}}