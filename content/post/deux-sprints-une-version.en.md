---
title: "Two sprints, one version"
publishdate: 2020-09-28
draft: false
tags: ["rero-ils", "release", "tests", "pilot libraries", "authorities"]
---

These last two months the RERO ILS team has worked successively on sprints [33](https://tree.taiga.io/project/rero21-reroils/taskboard/sprint-33-108) and [34](https://tree.taiga.io/project/rero21-reroils/taskboard/sprint-34-93) of the development. This work has resulted in a version `v0.12.0` offering many new features and deployed in time for the second phase of testing by the pilot libraries, which started at the end of September. Here are the major changes in this release, with full notes available on Github [`v0.12.0`](https://github.com/rero/rero-ils/blob/dev/RELEASE-NOTES.rst#v0120).

<!--more-->

## Link to contributing person-authorities

A new field `contribution` replaces the `author` field when cataloguing documents, in order to comply with current standards, in particular RDA cataloging rules. Documents are put in relation with contributing agents, whose authorities come from verified repositories (IdRef and GND). The role of each agent in the production of a document is also indicated by an RDA relationship code. If the authority is not found in the repositories, it can also be recorded manually as a character string in the same field.

{{< figure src="/img/contribution.jpg" caption="The `contribution` field newly added to the document data model">}}

## Circulation density under control

A great deal of behind-the-scenes work has been done on the backend of the circulation module, in order to solve the problems observed during the first pilot tests in March 2020 and to correctly implement all the [circulation actions](https://github.com/rero/rero-ils/blob/dev/doc/circulation/actions.md) identified, on the one hand. On the other hand, automated tests have also been developed in order to be able to check the proper functioning of this module with each new version and to identify any unexpected errors when work is carried out on other parts of the software.

## Need help ?

With the ongoing progress of RERO ILS' functionalities, it was necessary to document its operation for the end-user. This is now done with a [help platform](https://ils.test.rero.ch/help/home/) accessible from the professional and public interfaces of RERO ILS. This application offers, on the same platform, the public and professional help of RERO ILS to guide users and support their training on the system.

{{< figure src="/img/public-help.JPG" caption="The RERO ILS help interface developed with [flask-wiki](https://github.com/rero/flask-wiki)">}}

## Listing of new acquisitions

A field that should be interesting for the highlighting of collections has been implemented in the item data model: `new_acquisition`. This field is used to indicate whether an item should be part of _new acquisitions_ according to each library's criteria. This allows to exclude certain documents from this list (heritage documents, repurchases, older books, or others). This field also includes a date that can be used to build URLs to display the list of a library's new acquisitions. This list can be filtered by date, but also by other criteria (location, status, etc.), which offers great flexibility.

A common use case of this feature is to be able to include a link to the list of new acquisitions for a given month on the library’s website. The URLs created are permanent and point directly to a list of documents in the public interface of RERO ILS. The construction of URLs for these lists is also documented in the [professional help](https://ils.test.rero.ch/help/recherche/#nouvelles-acquisitions).

## Import of external records by API

To wrap up the new features of `v0.12.0`, let's mention the opening of an API access point that allows an authenticated user to import `marcxml` data directly into RERO ILS using a script or an external application. In the context of our pilot libraries, the [EZPump](http://www.ngscan.com/ezpump/) software is used to import MARC records from many reservoirs. It is currently being tested for adaptation to the RERO ILS environment through this access point.

## Second phase of pilot tests

This version is also an opportunity to continue our collaboration with our [pilot libraries](/reroils/early_adopters/). Indeed, the second round of tests was launched on September 24th. The RERO central is pleased to count on the cooperation of a new partner for these tests, the Médiathèque de Monthey.