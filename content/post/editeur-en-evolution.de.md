---
title: "Ein sich entwickelnder Editor"
date: 2020-08-03T14:53:42+02:00
publishdate: 2020-08-04
draft: false
tags: ["rero-ils", "release", "Anzeige", "Metadaten"]
---

Neuer Monat verstrichen, neue Version von {{< smallcaps "rero ils" >}} auf [der Testoberfläche][1] verfügbar. Die Arbeit des Entwicklungsteams zur Verbesserung der Software wird mit einem neuen Update fortgesetzt, das für Katalogisierer·innen von Interesse sein dürfte. Vollständigere Versionshinweise sind auf Github zu finden: [`v0.11.0`][2].

<!--more-->

## Pro Schnittstelle: der Dokumenteneditor wird verwöhnt

Da es sich um eines der Hauptinstrumente der Bibliothekarinnen und Bibliothekare handelt, insbesondere für die Katalogisierung, muss der Dokumenteneditor eine klare und ergonomische Schnittstelle bieten. Dies ist umso mehr der Fall, als dieses Modul häufig komplexe Daten nach nicht immer offensichtlichen Regeln anzeigen muss.

Die Arbeiten zur Verfeinerung dieser Schnittstelle sind konstant und spiegeln sich in dieser Version in einer Verbesserung der Lesbarkeit wider.

{{< figure src="/img/rero-ils-improvededitor.png" caption="Der Editor hat in dieser Version deutlich an Lesbarkeit gewonnen.">}}

Diese visuelle Verbesserung wird von mehreren Anpassungen begleitet: 
* Hinzufügen der Felder `partOf` (Host-Dokument), `seriesStatement` (Gesamttitelangabe) und `issuance` (Erscheinungsweise). Dadurch ist es möglich, saubere Verknüpfungen zwischen Dokumenten herzustellen, eine kleine Revolution innerhalb des Verbundes, wo diese Verknüpfungen bisher ausschliesslich auf Zeichenketten basierten.
* Die Anzeige einiger Übersetzungen wurde korrigiert, insbesondere im Formular _Feld hinzufügen_. Bitte beachten Sie, dass nicht alle Übersetzungen in dieser Version auf dem neuesten Stand sind, da ein Wechsel der Übersetzungsplattform im Gange ist. Diese Probleme werden in der nächsten Version korrigiert werden.
* Fehler bei der Speicherung von Dokumenten wurden behoben.
* Die Shortcut-Links _Gehe zu_ im rechten Panel sind jetzt funktionsfähig

## Inventarlisten

Eine weitere neue Funktion dieser `v0.11.0` sind Inventarlisten. Sie sind in der professionellen Schnittstelle über das Menü _Berichte & Monitoring_ zugänglich und erlauben es, Inventarlisten anzuzeigen, sie zu filtern und sie direkt im `CSV`-Format zu exportieren.

Gleichzeitig haben die Exemplare auch ein neues Feld `second_call_number`, das ihnen eine zweite Signatur verleiht, die auch in den Inventarlisten angezeigt wird.

[1]: https://ils.test.rero.ch
[2]: https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v0110