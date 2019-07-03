---
title: "Was ist neu Ende März 2019?"
date: 2019-05-06
tags: ["rero-ils", "release"]
---

Ende März wurde eine neue Version von <span style="font-variant: small-caps;">rero ils</span> (v0.1.a21) veröffentlicht:

- Die [Versionshinweise](https://github.com/rero/rero-ils/releases/tag/v0.1.0a21) beschreiben die Veränderungen und Ergänzungen.
- Die öffentliche Demo-Website: [ils.test.rero.ch](https://ils.test.rero.ch).
- Die Hilfeseite: [github.com/rero/rero-ils/wiki/Public-demo-help](https://github.com/rero/rero-ils/wiki/Public-demo-help).

Hier unten finden Sie eine kurze Beschreibung der wesentlichen Entwicklungen.

<!--more-->

Diese betreffen folgende Aspekte:

1. die Ausleihe,
1. die Benutzerschnittstelle,
1. die Personenautoritäten.

## Die Ausleihe.

Im Sommer 2018 haben die Entwicklungsteams von <span style="font-variant: small-caps;">rero ils</span> und [<span style="font-variant: small-caps">cds</span>](http://cds.cern.ch) des [<span style="font-variant: small-caps">cern</span>](https://home.cern) dabei zusammengearbeitet, das [`invenio-circulation`](https://github.com/inveniosoftware/invenio-circulation)-Modul auf der Grundlage einer [Modellierung](https://github.com/rero/rero-ils/blob/master/doc/circulation_statechart/circulation_item_statechart.pdf) umzuschreiben, die generisch genug ist, um die Anforderungen der meisten Bibliotheken zu erfüllen.  
Dieses Modul ist nun völlig integriert und wird für jede Ausleihtransaktion in <span style="font-variant: small-caps;">rero ils</span> verwendet.

Diese vollständige Version wird zudem mit einem wichtigen Bestandteil der Ausleihe ergänzt, nämlich die Parametrierung der Ausleihpolitiken und ihre Berücksichtigung bei Transaktionen. Eine Ausleihpolitik sagt, für ein bestimmtes *Lesertyp*/*Exemplartyp*-Paar, ob eine Ausleihe und Verlängerungen erlaubt sind, und ihre Dauer. Die Mindestanforderung für die Parametrierung des Ausleihmoduls ist eine einzige Ausleihpolitik, die als Standardpolitik markiert werden muss. Bei einer Transaktion sucht zunächst das System, je nach Leser- und Exemplartyp, nach einer treffenden Ausleihpolitik, zuerst auf der Ebene der Bibliothek und dann der Organisation. Wenn keine passt, wird die Standardpolitik angewendet.

{{< figure src="/img/0a21-circ-pol.png" caption="Beispiel einer Ausleihpolitik" alt="Screenshot des Editors von Ausleihpolitiken" >}}

## Die Benutzerschnittstelle.

Die Benutzerschnittstelle wurde völlig überarbeitet, um sie zu vereinfachen und die Struktur der Seiten je nach Typ (Suche, Recordanzeige, …) zu harmonisieren. Ausserdem wurde eine Umverteilung vorgenommen, zwischen den öffentlich zugänglichen Seiten, die manchmal für authentifizierte Bibliothekare zusätzlich Funktionalitäten anzeigen, und den Seiten, die immer nur für Bibliothekare zugänglich sind.

Das Suchfeld zeigt bei der Texteingabe Vorschläge. Es handelt sich um Titel von Dokumenten und Namen von Personen, die dem eingegebenen Text entsprechen. Ein Klick auf einen Titelvorschlag startet eine Suche mit den Wörtern des Titels, während ein Klick auf einen Personenvorschlag direkt zur Personenseite führt.

{{< figure src="/img/0a21-suggestion-recherche.png" caption="Suchvorschläge" alt="Screenshot der Suchvorschläge unter dem Suchfeld, bei der Texteingabe." >}}

## Die Personenautoritäten.

Die Verwendung von [<span style="font-variant: small-caps;">mef</span>](https://mef.test.rero.ch) durch <span style="font-variant: small-caps;">rero ils</span> hat sich deutlich entwickelt. Wichtige Arbeiten auf das <span style="font-variant: small-caps;">mef</span> selbst wurden durchgeführt, welches von 96 Records (Testphase) auf 6,8 Millionen Records physischer Personen erstreckte.

In <span style="font-variant: small-caps;">rero ils</span> wurden die bestehenden Links zwischen bibliographischen Records und diesen Personenautoritäten importiert, und in der Schnittstelle mit Hyperlinks angezeigt, die auf die Personenseiten führen. Technisch gesehen wird die Personenautorität nicht in <span style="font-variant: small-caps;">rero ils</span> importiert, sondern in Echtzeit abgefragt. 

Bei der Katalogisierung ist es möglich, immer in Echtzeit über den <span style="font-variant: small-caps;">mef</span>-Service, die 6,8 Millionen Personenrecords durchzusuchen und eine Autorität zu verlinken. Wenn die gesuchte Person als Autorität nicht vorhanden ist, werden die Daten als Text im bibliographischen Record gespeichert. Der Mechanismus der *temporären* Autoritätsrecords muss noch modelliert und entwickelt werden.

{{< figure src="/img/0a21-edit-authority.png" width="300px" caption="Suche nach einer Personenautorität bei der Katalogisierung eines bibliographischen Records" alt="Screenshot der Suche nach einer Personenautorität im Editor bei der Katalogisierung" >}}
