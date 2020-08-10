---
title: "MEF: Multilingual Entity File"
language: "en"
date: 2020-08-18
---

# What MEF does

MEF is a system that combines entities (or authorities) in several languages and makes them available, allowing:

* the end user: to search and display the contents (and not only the interface) in his or her own language
* libraries: to reuse as much as possible international repositories (GND, IdRef...). They can thus abandon the local management of an authority file and embrace the web of data.

MEF is an API making data available for other systems, especially for ILS. It can therefore be used by several different interfaces. For example, RERO ILS uses MEF. This service does not have its own user interface.

RERO is developing this service in an open approach and is making it available, for the time being in a test version, at [mef.test.rero.ch](https://mef.test.rero.ch "The MEF service, freely accessible").

# Entity types

MEF will eventually contain the types of resources as specified in the RDA and [Library Reference Model] standards (https://www.ifla.org/publications/node/11412 "Library Reference Model, on the IFLA website"):

* persons
* corporate bodies
* works
* common names
* places
* periods
* expressions

# How it works

MEF collects entities from different sources (GND, IdRef, etc.) and synchronises with them. It aggregates them automatically through [VIAF](https://viaf.org "Virtual International Authority File web site"), deriving (currently) German and French display labels when available.

The entities themselves are maintained and edited directly at source in agreement with their issuing institution. No entities are created or edited directly in MEF.

{{< figure src="/img/mef_fonctionnement.svg" caption="MEF operation" alt="MEF operation schema" >}}