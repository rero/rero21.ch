---
title: "Kick-off des RERO ILS-Migrationsprojekts"
publishdate: 2020-12-08
draft: false
tags: ["migration", "rero-ils", "go-live"]
slug: kick-off-du-projet-de-migration-rero-ils
---

Die Auftaktsitzung des RERO ILS-Migrationsprojekts fand am 3. Dezember in (natürlich virtueller) Anwesenheit von Vertretern der 41 Bibliotheken statt, die an diesem Abenteuer teilnehmen. Es war eine Gelegenheit, den Kontext des Projekts in Erinnerung zu rufen, die Umrisse der Version 1.0.0 im Detail darzustellen, den Entwicklungsmodus ab 2021 zu erläutern und natürlich den Zeitplan für die Migration vorzustellen.

<!--more-->

## Eine Version 1.0.0

Die Nomenklatur der Versionen folgt etablierten [Konventionen][1]. Zum ersten Mal werden wir Ende Dezember die erste Ziffer iterieren und zu 1... übergehen, was eine vollständigere und stabilere Version ankündigt. Damit soll das reibungslose Funktionieren des Systems in der Produktion ab Juli 2021 sichergestellt werden.

[1]: https://semver.org/

In der Zwischenzeit werden mit dieser Version vollständige Laden von Bibliotheksdaten durchgeführt, um das Testen, Parametrisieren und Verfeinern der Migrationsspezifikationen zu ermöglichen. Das Entwicklungsteam wird sich auf Fehlerbehebungen und kleine Verbesserungen konzentrieren. Sie wird auch an der Verbesserung der Leistungsfähigkeit (z.B. Laden von Seiten), der Konfiguration von Monitoring-Werkzeugen (Warnung bei Fehlern oder Ausfällen) und der Einrichtung einer Produktionsumgebung arbeiten.

## Prioritäre Funktionalitäten

Die Version 1.0.0 enthält nicht alle von den Bibliotheken gewünschten Funktionalitäten. Das Team wird von daher die Entwicklung des Systems fortsetzen, auch wenn aufgrund des Personalabbaus in der Zentrale, des Migrationsprojekts und der Stabilisierungsarbeit weniger Ressourcen zur Verfügung stehen werden.

Die vorrangigen Funktionalitäten wurden in Absprache mit der Systemgruppe festgelegt, die die Migration überwacht und die 41 RERO ILS-Bibliotheken vertritt. Die Prioritäten werden je nach Bedarf regelmässig neu bewertet.

Und nach dem Go-Live wird die Entwicklung von RERO ILS fortgesetzt. In der Tat werden RERO und sein Partner, die Katholische Universität Löwen, die Aktualisierung der Softwarekomponenten garantieren und an der Hinzufügung neuer Funktionalitäten arbeiten.

## Das Migrationsprojekt

Zwei Projektteams wurden gebildet, um die Migration zu überwachen und Spezifikationen zu erstellen:

* Die Systemgruppe. Sie ist zuständig für Parametrisierung, Ausleihe, Erwerbungen, Zeitschriftenverwaltung und Statistik, und befasst sich auch mit Tests, Priorisierung und Konvertierungsspezifikationen.
* Die Metadatengruppe. Sie ist für die Katalogisierung und die öffentliche Schnittstelle zuständig, und arbeitet auch bei den Tests, der Verfeinerung der Konvertierung bibliographischer Daten und der Definition von Katalogisierungsprozessen und -regeln mit.

Die Zentrale freut sich, auf das Fachwissen von Menschen vor Ort zählen zu können, die das Entwicklungsteam bei dieser Migration begleiten!

Der Migrationszeitplan (siehe unten) hat 4 wichtige Meilensteine:

* `Ende Februar`: 1. vollständiges Laden der Daten
* `März/April`: Train-the-Trainer-Kurse
* `Ende April`: 2. vollständiges Laden der Daten
* `12. Juli 2021`: Go-Live

{{< figure src="/img/calendrier_migration.svg" caption="Migrationszeitplan (auf Französisch)" alt="Migrationszeitplan (auf Französisch)" link="/img/calendrier_migration.svg" >}}

