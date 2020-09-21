---
title: "Vorhersagen: zwischen Hass und Leidenschaft"
date: 2020-05-28T15:00:00+02:00
publishdate: 2020-05-28
draft: false 
tags: ["rero-ils", "Erwerbungen", "Vorhersagen", "Pilotbibliotheken"]
---

Einige Leute lieben sie, andere verabscheuen sie. Heute geht es um die Vorhersagen und um ihre Erscheinungsfrequenz in den Daten der RERO ILS-Pilotbibliotheken. Die Arbeiten zur Umsetzung der Zeitschriftenverwaltung führen die RERO-Zentrale tatsächlich dazu, diesen Aspekt auf der Grundlage der vorhandenen Daten zu analysieren. (Für die Experten sind diese Vorhersagen im MARC-Feld 853 der Holdings zu finden).

Nach der Extraktion der Daten, entdeckten wir einige interessante Zahlen. Wir möchten sie hier vorstellen, da es einige Gemeinsamkeiten und Unterschiede zwischen den Bibliotheken gibt.

<!--more-->

[Zur Erinnerung](/de/rero-ils-expose-to-test) entwickeln wir RERO ILS mit Hilfe von Pilotbibliotheken, die das System testen und uns Rückmeldungen von Fachleuten aus der Praxis geben. Unsere sechs Pilotbibliotheken sind die folgenden:

* [Bibliothek von Bulle](https://musee-gruerien.ch/)
* [Kantonsbibliothek Jura](https://www.jura.ch/occ/bicj)
* [Mediathek Wallis](https://www.mediatheque.ch/) (und ihre 4 Standorte in Brig, Martigny, St-Maurice, Sitten)
* [Öffentliche und Universitätsbibliothek Neuenburg](http://bpun.unine.ch/)
* [Stadtbibliothek Delémont](http://www.delemont.ch/fr/Tourisme-culture-et-loisirs/Vie-culturelles/Bibliotheque/Bibliotheque.html)
* [Stadtbibliothek La Chaux-de-Fonds](http://cdf-bibliotheques.ne.ch/)

## Wo ist man am meisten nach Vorhersagen gierig?

Wir sind eher zufällig auf diese Zahlen gestossen; wir wollen also niemanden beschuldigen... immerhin kann man feststellen, dass die Walliserinnen und Walliser stärker dazu neigen, den Eingang der Lieferungen kontrollieren zu wollen 🤭

{{< bootstrap-table "table table-striped table-bordered" >}}
| Pilotbibliothek                                         | Anzahl Holdings    | Anzahl Holdings mit Vorhersage     | Verhältnis |
|---------------------------------------------------------|-------------------:|-----------------------------------:|-----------:|
| Mediathek Wallis (Sitten)                               |              17710 |                               3892 |        22% |
| Kantonsbibliothek Jura                                  |               6788 |                                993 |        15% |
| Mediathek Wallis (St-Maurice)                           |               1218 |                                141 |        12% |
| Mediathek Wallis (Brig)                                 |               2209 |                                210 |        10% |
| Bibliothek von Bulle                                    |               2411 |                                223 |         9% |
| Öffentliche und Universitätsbibliothek Neuenburg        |              18761 |                               1672 |         9% |
| Mediathek Wallis (Martigny)                             |               2333 |                                196 |         8% |
| Stadtbibliothek La Chaux-de-Fonds (ohne Jugendbibl.)    |               7021 |                                435 |         6% |
| Stadtbibliothek Delémont (Erwachsenen und Jugendlichen) |               1587 |                                102 |         6% |
{{< /bootstrap-table >}}

Wir haben keine weitere Analyse durchgeführt, um die Gründe für diese Zahlen herauszufinden. Zudem zeigt sich, dass die Öffentliche und Universitätsbibliothek Neuenburg bei vergleichbarer Grösse weit mehr Holdings hat als La Chaux-de-Fonds. Auch hier haben wir beschlossen, auf diesen Aspekt nicht weiter einzugehen (wir können einen Fehler unsererseits bei der Extraktion der Daten nicht ausschliessen). Das Verhältnis bleibt jedoch in der gleichen Grössenordnung.

## Welche Erscheinungsfrequenz wird bevorzugt?

Das Bild unten zeigt die Erscheinungsfrequenzen der Vorhersagen für alle Pilotbibliotheken.

{{< figure src="/img/periodicite_globale.svg" caption="Erscheinungsfrequenzen der Vorhersagen für alle Pilotbibliotheken" alt="Graphik: Erscheinungsfrequenzen der Vorhersagen für alle Pilotbibliotheken" >}}

Vorsicht! Dieses Tortendiagramm zeigt nur die Verteilung für fortlaufende Publikationen, die mit der Zeitschriftenverwaltung empfangen werden.

Es ist zu erkennen, dass die jährlichen, vierteljährlichen, halbjährlichen und monatlichen Veröffentlichungen drei Viertel des Kuchens decken, wenn man das so sagen kann.

## Kleiner Benchmark der Bibliotheken

Um die Analyse zu verfeinern, haben wir die 5 wichtigsten Erscheinungsfrequenzen pro Bibliothek ausgewählt (Bild unten). Folgendes kann insbesondere festgestellt werden:

* Bibliotheken mit einem historischen Auftrag empfangen am meisten jährliche Veröffentlichungen. Wir denken hier an Tätigkeitsberichte und verschiedene Dokumente, die von regionalen Gremien herausgegeben und zu historischen Zwecken gesammelt wurden.
* Kleinere Bibliotheken, die die Zeitschriftenverwaltung am wenigsten verwenden (gemäss obiger Tabelle), konzentrieren sich eher auf monatliche Publikationen.

Einige Höhepunkte:

* Wöchentliche Publikationen sind in Delémont beliebter als anderswo.
* Die Kantonsbibliothek Jura hat nur Augen für jährliche Zeitschriften. Sind Sie jedoch eine monatliche Zeitschrift, dann laufen Sie nicht in Pruntrut herum, das könnte gefährlich für Sie sein.
* Martigny ist in die Monatszeitschriften verknallt, die nur 11 Mal im Jahr erscheinen.

Andere Interpretationen sind natürlich möglich, zögern Sie nicht, dies uns auf Twitter ([@rero_centrale](https://twitter.com/rero_centrale)) oder per E-Mail ([info@rero.ch](mailto:info@rero.ch)) mitzuteilen!

{{< figure src="/img/periodicite_par_bibliotheque.svg" caption="Erscheinungsfrequenz der Vorhersagen pro Bibliothek (Top 5)" alt="Graphik: Erscheinungsfrequenz der Vorhersagen pro Bibliothek (Top 5)" >}}
