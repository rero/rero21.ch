---
title: "Predictions: between hate and passion"
date: 2020-05-28T15:00:00+02:00
publishdate: 2020-05-28
draft: false 
tags: ["rero-ils", "acquisition", "predictions", "pilot libraries"]
---

Some love them, some hate them. Today we look into predictions and their periodicity among the data from the {{< smallcaps "rero ils" >}} pilot libraries. Indeed, the work on the implementation of the serial function is leading the RERO central office to analyze this aspect based on existing data. (For the experts, these predictions can be found in the MARC field 853 of the holdings).

After extracting the data, we came across some interesting figures. We would like to share them here, as there are some similarities and differences between libraries.

<!--more-->


[As explained in a previous post](/en/rero-ils-s-expose-aux-tests), we are developing {{< smallcaps "rero ils" >}} with the help of pilot libraries, which are testing the system and providing us with feedback from field professionals. Our six pilot libraries are the following:

* [Jura Cantonal Library](https://www.jura.ch/occ/bicj)
* [Library of Bulle](https://musee-gruerien.ch/)
* [Public and University Library of Neuchâtel](http://bpun.unine.ch/)
* [Public Library of Delémont](http://www.delemont.ch/fr/Tourisme-culture-et-loisirs/Vie-culturelles/Bibliotheque/Bibliotheque.html)
* [Public Library of La Chaux-de-Fonds](http://cdf-bibliotheques.ne.ch/)
* [Valais Media Library](https://www.mediatheque.ch/) (and its four sites in Brig, Martigny, St-Maurice, Sion)

## Where is the greatest appetite for predictions?

We came across these figures more or less by chance, so we don't want to incriminate anyone... but we can all the same observe that the people in Valais have a stronger tendency to want to control the entry of the leaflets.🤭

{{< bootstrap-table "table table-striped table-bordered" >}}
| Pilot library                                                      | Number of holdings | Number of holdings with prediction | Ratio |
|--------------------------------------------------------------------|-------------------:|-----------------------------------:|------:|
| Valais Media Library (Sion)                                        |              17710 |                               3892 |   22% |
| Jura Cantonal Library                                              |               6788 |                                993 |   15% |
| Valais Media Library (St-Maurice)                                  |               1218 |                                141 |   12% |
| Valais Media Library (Brigue)                                      |               2209 |                                210 |   10% |
| Library of Bulle                                                   |               2411 |                                223 |    9% |
| Public and University Library of Neuchâtel                         |              18761 |                               1672 |    9% |
| Valais Media Library (Martigny)                                    |               2333 |                                196 |    8% |
| Public Library of La Chaux-de-Fonds (without children's libraries) |               7021 |                                435 |    6% |
| Public Library of Delémontt (adults and children)                  |               1587 |                                102 |    6% |
{{< /bootstrap-table >}}

We have not conducted further analysis to determine the reasons for these figures. Furthermore, it can also be seen that, for comparable sizes, Public and University Library of Neuchâtel has many more holdings than La Chaux-de-Fonds. Here too, we chose not to elaborate further on this aspect (we cannot rule out an error on our part when extracting the data). The ratio remains in the same range.

## What is the favourite frequency?

The image below shows the prediction frequencies for all the pilot libraries.

{{< figure src="/img/periodicite_globale.svg" caption="Prediction frequencies for all pilot libraries" alt="Graph: prediction frequencies for all pilot libraries" >}}

Please note that this pie chart shows only the distribution for the serial publications which are checked in.

We can observe that annual, quarterly, semi-annual and monthly share the ¾ of the cake, if we can put it that way.

## Let’s have a quick library benchmark

To analyse in detail, we have selected the top 5 periodicities per library (image below). In particular, we can see that:

* Libraries with a heritage mission check in more annual publications. These include activity reports and various documents issued by regional bodies and collected for historical purposes.
* Smaller libraries with a lower check-in activity (according to the table above) tend to focus on monthly publications.

Some noteworthy facts:

* Weekly newspapers are more popular in Delémont than elsewhere.
* The Jura Cantonal Library only has eyes for annual publications. On the other hand, if you are a monthly publication, don't hang around in Porrentruy, it could be dangerous for you.
* Martigny has a crush for monthly publications which only have 11 issues a year.

Other interpretations are of course possible, feel free to let us know on Twitter (@rero_centrale) or by email (info@rero.ch)!

{{< figure src="/img/periodicite_par_bibliotheque.svg" caption="Prediction frequencies per library (top 5)" alt="Graph: prediction frequencies per library (top 5)" >}}
