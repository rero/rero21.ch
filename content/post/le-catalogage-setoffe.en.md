---
title: "New cataloguing developments"
date: 2020-07-06T08:23:38+02:00
publishdate: 2020-07-06
draft: false
tags: ["rero-ils", "release", "acquisition", "display", "metadata", "predictions"]
slug: le-catalogage-setoffe
---

A new sprint ends for RERO ILS with a version full of new features. Thanks to an increasingly stable technical foundation, the development team can now focus on user-oriented functionality. The full release notes are available as usual on Github: [`v0.10.0`][1].

<!--more-->

## Interface improvements

UI work on the public and professional interfaces continues. This version brings many adjustments, and in particular a redesign of the metadata editor (cataloguing interface) to improve its readability. The editor is now displayed across the full width of the screen and the fields are easier to distinguish visually with the titles of the main fields now in bold and some sub-fields that can be displayed inline.

{{< figure src="/img/rero-ils-editeur.png" caption="Displaying sub-fields inline instead of in blocks and field titles in bold">}}

## Importing records

Being able to import records from external catalogues streamlines much of the cataloguing work for librarians. RERO ILS offers the possibility to do so via [the SRU protocol][2]. The librarian can search for the desired record in the selected catalogue (currently only BnF) using a simple query (keywords for the author, title, date, ISBN…). They can choose the record that they want to import. This record can then be freely edited in the cataloguing interface before being saved.

## New feature: receive an issue

Another brand new feature of the `v0.10.0` release is the journal arrivals module. The holding's **frequency** field, based on [RDA standards][3], enables the system to automatically predict the dates of the next regular issues and to receive them with one click. It is of course also possible to receive an irregular issue. When an issue is marked as *received*, the system automatically creates an item in the holding. 

{{< video src="rero-ils-receiveissue" legend="Quick reception of regular issues according to frequency" >}}

The video above shows an example of the *quick receive* function:

1. *Obtenir* (*Get*) displays the items
1. Predictions for future issues are displayed
1. A click on the quick receive button creates the new item for the next issue. If necessary, the other button can be used to edit the item before marking it as *received*. 

## Items: duly noted

A `notes` field has been added to the items' template. Such notes can be of four types:

* **Public note**: is displayed in the detailed view of the public and professional interface.
* **Private note**: is displayed only in the detailed view of the professional interface.
* **Checkin Note**: displays an alert upon item checkin.
* **Checkout note**: displays an alert upon item checkout.

These notes address an essential need expressed by several of our pilot libraries as well as by our partners at UC Louvain.

{{< figure src="/img/item-notes.png" caption="Item notes in the professional interface">}}

[1]: https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v0100
[2]: https://www.bnf.fr/fr/protocole-sru-vue-densemble
[3]: http://www.rdaregistry.info/termList/frequency/