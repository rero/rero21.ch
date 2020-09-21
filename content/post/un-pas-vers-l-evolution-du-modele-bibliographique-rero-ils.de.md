---
title: "Ein Schritt zur Entwicklung des RERO ILS bibliographischen Modells: die Vernetzung der Daten"
date: 2019-08-07T08:00:00+02:00
draft: false
tags: ["rero ils", "enrichment", "lrm", "works", "bibliostratus", "data alignment"]
---

Werk, Expression, Manifestation, Exemplar, ein, zwei, drei, vier... Steter Refrain, mit dem die Mitarbeitenden in Bibliotheken nun vertraut sind. In der Tat werden diese vier Konzepte regelmässig auf Fachkonferenzen und in bibliothekswissenschaftlichen Kursen skandiert. Im Allgemeinen spiegeln sie eine Entwicklung der bibliographischen Modellen (LRM), der Katalogisierungsregeln (RDA) und der Datenaustauschformaten (Bibframe) wider. Unsere französischen Nachbarn nennen diese Bewegung "Transition bibliographique". Und das Projekt RERO ILS entkommt ihr nicht, ganz im Gegenteil: es ist voll davon durchdrungen. Die Nutzung von Bibliostratus zeigt dies.

<!--more-->

### Das Tool Bibliostratus

Bibliostratus ist eine Open-Source-Software, die in Frankreich im Rahmen des Programms [Transition bibliographique] (https://www.transition-bibliographique.fr) (Gruppe "Système et données") entwickelt wird, welches von der [Abes] (http://www.abes.fr/) und der [BnF] (https://www.bnf.fr/) gemeinsam geleitet wird. Bibliostratus, das über [Github](https://github.com/Transition-bibliographique/bibliostratus) zum Download verfügbar ist, dient dazu, bibliografische Daten mit Sudoc- und BnF-Daten automatisch abzugleichen[^1].

Hierfür funktioniert es in drei Schritten:

1. Konvertierung von MARC21- oder UNIMARC-Dateien in `.txt`-Dateien mit einer Auswahl wichtiger Felder
2. Abgleich durch Abfragung von Sudoc und BnF
3. Abruf der kompletten Sudoc- oder BnF-Datensätze

Schritt 2 ist der herausforderndste Teil, denn er besteht im Vergleichen von Feldern untereinander, um festzustellen, ob zwei Datensätze dem gleichen Objekt entsprechen. Bei Büchern, die im Fachjargon als "Textmonographien" bezeichnet werden, sind die wichtigsten Vergleichselemente ISBN, Titel, Autor und Datum.

Bibliostratus unterstützt die Abstimmung von Manifestationen und Autoritäten (Personen und Körperschaften). Da letztere bereits durch VIAF miteinander verbunden sind, ist RERO derzeit nur an Manifestationen interessiert.

##### Welchen Nutzen hat RERO ILS?

Das bibliographische Modell von RERO ILS beinhaltet die Entität "Werk", zur Zeit nicht im Katalog. Allerdings stellt die automatische Generierung der Werke auf der Grundlage der Manifestationen ein äusserst komplexer Prozess dar, welcher starke Bemühungen erfordert, wenn die Daten der Definition von "Werk" gemäss LRM entsprechen sollen.

In der gegenwärtigen Situation verfügt RERO nicht über die Mittel, um solche Entwicklungen durchzuführen. Hingegen geben sich die BnF und die Abes die Möglichkeit, diese Anreicherungen und Abgleiche zu machen. Durch einen Prozess in Etappen und mit Teilmengen von Daten, um eine bestimmte Qualität zu gewährleisten, hat die BnF bereits Tausende von Werk-Manifestation-Links in ihre Produktionsdatenbank integriert[^2]. Die Abes seinerseits untersucht die Möglichkeiten ihrer CBS-Software mit demselben Ziel[^3].

Für RERO besteht das kurzfristige Ziel darin, die richtigen Datenabgleiche mit den Manifestationdatensätzen von BnF und Sudoc zu sammeln und in die Virtua-Produktionsdatenbank zu integrieren. Damit werden ab 2021 alle Bibliotheken davon profitieren.

Mittel- und langfristig wird es dadurch möglich sein, bestimmte RERO-Manifestationen mit in Frankreich erstellten Werkdatensätzen guter Qualität zu verbinden.

##### Umsetzung

Der RERO-Katalog enthält rund 6,1 Millionen Manifestationen, die Bibliostratus beim Schritt 1 aus Sicht des Arbeitsspeichers ins Schwitzen gebracht haben. Die Datei wurde deshalb in Pakete von 500.000 Datensätzen aufgeteilt. Dies ermöglichte es dann, den Schritt 2 - den zeitaufwendigsten - parallel für mehrere Dateien zu starten, ansonsten hätte diese Verarbeitung mehrere Monate gedauert 😱. All dies wurde auf einem PC gemacht; hier unten ist eine kleine Vorschau:

{{< figure src="/img/bibliostratus_screen.png" caption="Bibliostratus am Werk auf einem unserer PC" alt="Screenshot von Bibliostratus am Werk auf einem unserer PC" >}}

### Fehler vermeiden durch eine strenge Methodologie

Die meisten automatischen Abgleiche, die auf Ähnlichkeitsvergleiche basieren, generieren Fehler, die als falsche Positive bezeichnet werden: die Feststellung einer falschen Äquivalenz.

Um diese falschen Positive zu minimieren, wurde Bibliostratus an einer repräsentativen Stichprobe des Katalogs von 10'000 Datensätzen getestet. Die Äquivalenzen wurden dann ausgewählt und ausgewertet. Die Ergebnisse dieser Analyse wurden den Entwicklern der Software mitgeteilt, die dann Bibliostratus angepasst haben.

Im Auswahlschritt werden unnötige Daten verworfen, wie z.B. Daten mit mehreren Äquivalenzen für einen Datensatz oder gar keine Äquivalenz. Die ausgewählten Daten werden dann nach Art des Generierungsalgorithmus sortiert. Bibliostratus verwendet je nach bibliographischen Datensätzen mehr als 700 verschiedene Algorithmen, um Übereinstimmungen herzustellen (es gibt eine Dokumentation auf [Github](https://github.com/Transition-bibliographique/bibliostratus/wiki/2_annexe.-Le-m%C3%A9canisme-d'alignement)). Es werden nur die ausgewählt und ausgewertet, die die meisten Äquivalenzen erzeugt haben. So vergleicht beispielsweise der Algorithmus, der die meisten Äquivalenzen mit der BnF erzeugt hat, ISBNs und dann den ganzen Titel (46% der Fälle).

Die häufigsten falschen Positive sind Fälle, in denen zwei verschiedene Manifestationen derselben Expression zusammengeführt werden. In einigen Situationen wird vermutet, dass die beiden Manifestationen tatsächlich gleich sind, aber dass die Daten unterschiedlich eingegeben wurden. Gründe dafür können unterschiedliche Katalogisierungsregeln, eine abweichende Analyse durch den Katalogisierer oder noch  menschliches Versagen sein.

Nach der Validierung der Qualität einer Methode können die Ergebnisse in die Produktion integriert werden, im Wissen, dass das Fehlerrisiko insbesondere bei Dokumenten ohne ISBNs nicht vollständig ausgeschlossen werden kann. Ein falsches Positiv ist jedoch im Allgemeinen nicht völlig falsch, da es fast immer zwei Manifestationen derselben Expression zusammenführt.

### Einige Zahlen aus dem RERO-Katalog

Die nachstehenden Tabelle bezieht sich nur auf die Textmonographien im RERO-Katalog, vorzugsweise in Übereinstimmung mit der BnF, ansonsten mit dem Sudoc.

{{< bootstrap-table "table table-striped table-bordered" >}}
| Ergebnis des Abgleichs     | Häufigkeit | % der RERO-Monographien | % des ganzen RERO |
|:---------------------------|-----------:|------------------------:|------------------:|
| Keine Äquivalenz           | 2'954'451  | 65.2%                   | 48.1%             |
| 1 BnF-Äquivalenz           | 1'213'557  | 26.8%                   | 19.8%             |
| 1 Sudoc-Äquivalenz         | 243'569    | 5.4%                    | 4.0%              |
| Mehrere BnF-Äquivalenzen   | 108'693    | 2.4%                    | 1.8%              |
| Mehrere Sudoc-Äquivalenzen | 12'896     | 0.3%                    | 0.2%              |
{{< /bootstrap-table >}}

Zunächst werden die Abgleiche mit einer einzelnen Übereinstimmung nach Validierung durch die Qualitätskontrolle in die Produktion integriert. Dies entspricht etwa 15-20% aller RERO-Datensätze.

### Quellenangabe

[^1]: Bibliostratus. Transition bibliographique des catalogues vers le web de données [online]. 2. Juli 2019. [Konsultiert am 17.07.2019]. Verfügbar unter: https://www.transition-bibliographique.fr/systemes-et-donnees/bibliostratus/

[^2]: BNF. Programme national Transition bibliographique. Bibliothèque nationale de France [online]. 2019. [Konsultiert am 17.07.2019]. Verfügbar unter: https://www.bnf.fr/fr/programme-national-transition-bibliographique

[^3]: ABES. La FRBRisation des données du Sudoc en questions / réponses [online]. 20. Oktober 2017. Abes. [Konsultiert am 17.07.2019]. Verfügbar unter: http://documentation.abes.fr/sudoc/autres/FRBRisationDuSudoc.pdf


