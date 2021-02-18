---
title: "\"Swiss made\" also means multilingual"
publishdate: 2021-02-18
draft: false
tags: ["rero-ils", "multilingualism", "entities"]
slug: swiss-made-signifie-aussi-multilingue
---

With the integration of corporate bodies in its data model, RERO&nbsp;ILS makes the ambitious objective of multilingualism a reality, as promised by the MEF project. The end user will not only have access to an interface in several languages, but also to *data* in several languages. This is a Swiss obligation! 🇨🇭

<!--more-->


## How multilingualism works

The multilingual nature of the data is based on the project [MEF - Multilingual Entity File](/en/mef/). The project page explains in detail how the service works. The principles are summarised below:

1. During cataloguing, the documents are linked to agents[^1] described in the entity files IdRef[^2] (in French) or GND[^3] (in German).
1. Each month, the VIAF system merges the IdRef and GND (and other) entities representing the same agents.
1. MEF retrieves these data and RERO&nbsp;ILS can then display, in the public interface
    * the IdRef version if the interface language is French.
    * the GND version if the interface language is German.

Multilingualism has certain limits:

* For the moment, it only works for German and French.
* It only works for documents with a link to an entity present in both IdRef and GND (and which has been clustured by VIAF).
* It is particularly useful for the names of corporate bodies, but less so for names of persons that are not translated from one language to another.

Finally, the IdRef and GND reference datasets are also two building blocks of cataloguing within the SLSP network. RERO therefore ensures good data interoperability.

## Real added value for the end user

Multilingualism is characterised by three functionalities in the interface.

**1. Displaying the names of persons and corporate bodies for the documents**

These names are present in the result list, in the detailed view of a document and in the patron account (loans, history, requests, etc.). When the language of the interface changes, the German or French form is displayed.

In the image below, a document is shown on the left in the German interface and on the right in the French interface. It is not only the interface elements that adapt to the language, but also the names of the authors. The transcribed data, such as the statement of responsibility, obviously do not adapt, since they must represent the document faithfully.

{{< figure src="/img/multilingualism_display.png" caption="Detailed view of a document, in German and in French">}}

**2. The author facet**

When the interface language changes, the German or French form is displayed.

{{< figure src="/img/multilingualism_facet.png" caption="Author facet, in German and in French">}}

**3. The search bar and autocompletion**

When the interface language changes, the suggestions are displayed in French or in German. The search is of course performed in all languages.

In the image below, the interface is in German but the user searches in French. RERO&nbsp;ILS will therefore provide suggestions in German if possible.

{{< figure src="/img/multilingualism_search.png" caption="Search suggestions that adapt to the interface language">}}

## Cataloguing with or without entities

Multilingualism therefore only works if there is a link to an entity. When this is not the case, the librarian can choose to create the entity (directly in the IdRef or GND tools) or to enter an authorised access point without an entity (see image below).

{{< figure src="/img/multilingualism_local_entity.png" caption="Entering the different parts of an access point for a corporate body in RERO&nbsp;ILS">}}

## Entity or authority?

We use the two words indifferently, but we clearly prefer *entity*. Indeed, the expression *authority* dates from the references within card catalogues in drawers. In the semantic web era, it has become more common to speak of *entities*. These are no longer limited to a retained form and rejected forms, but can also include many other structured data. It is therefore a terminology that we consider to be more appropriate.

[^1]: The word "agent" comes from the official RDA terminology. It includes persons, families and corporate bodies.
[^2]: [IdRef](https://www.idref.fr/) is a dataset of French-speaking authorities, maintained by the French Bibliographic Agency (ABES) and used by different platforms of French scientific institutions.
[^3]: [GND](https://www.dnb.de/DE/Professionell/Standardisierung/GND/gnd_node.html), for Gemeinsame Normdatei, is a dataset of German-speaking authorities managed by the German National Library, but used by various German, Austrian and Swiss libraries. GND is used in particular by the German-speaking libraries of the SLSP network.