---
title: "What's new in the March release?"
date: 2019-05-06
tags: ["rero-ils"]
---

End of March, a new <span style="font-variant: small-caps;">rero ils</span> version (v0.1.0a21) was released:

- The [release note](https://github.com/rero/rero-ils/releases/tag/v0.1.0a21) lists the changes and additions.
- The public demo website : [ils.test.rero.ch](https://ils.test.rero.ch).
- The public demo help page : [github.com/rero/rero-ils/wiki/Public-demo-help](https://github.com/rero/rero-ils/wiki/Public-demo-help).

Below is a short description of the main new features.

<!--more-->

They mainly involve:

1. the circulation module,
1. the user interface,
1. the person authorities.

# Circulation.

During summer 2018, the <span style="font-variant: small-caps;">rero ils</span> development team worked together with the [<span style="font-variant: small-caps">cern</span>](https://home.cern)'s [<span style="font-variant: small-caps">cds</span>](http://cds.cern.ch) team to rewrite the [`invenio-circulation`](https://github.com/inveniosoftware/invenio-circulation) module, accordingly to a generic [state chart](https://github.com/rero/rero-ils/blob/master/doc/circulation_statechart/circulation_item_statechart.pdf), in the hope that it could be adapted to most library use cases. This module is now fully integrated and used for each circulation transaction within <span style="font-variant: small-caps;">rero</span>.

This version also fulfills an important part of the circulation module, namely the setting of circulation policies and the fact that theses policies are taken into account for each circulation transaction. For a *patron type* / *item type* specific pair, a circulation policy determines whether the check-out or the extension is possible, and its duration. Note that the minimal circulation module setting requirement is to create only one default circulation policy. For each transaction, depending on the patron type and the item type, the system searches for a corresponding circulation policy, firstly at the libray level, then at the organisation level. If it doesn't find any, the default policy will then be used.

{{< figure src="/img/0a21-circ-pol.png" caption="Circulation policy example" alt="Circulation policy editor screenshot" >}}

## The user interface.

The user interface has been completely redesigned to simplify and somewhat harmonize the structure of the pages according to their type (search, record view… ). A new sorting between public pages, sometimes with enhanced functionalities depending on the logged in user, and professional ones, has been made.

As the user types a query into the search input field, suggestions are displayed. These consist of a list of document titles or a list of physical person authorities, matching the query being typed. As the user selects a document suggestion, a query with the title words is launched, but if it's a person authority which is selected, then the specific person record is displayed.

{{< figure src="/img/0a21-suggestion-recherche.png" caption="Search suggestions" alt="Search suggestions screenshot, as a query is being typed" >}}

## Les autorités personnes.

The use of [<span style="font-variant: small-caps;">mef</span>](https://mef.test.rero.ch) <span style="font-variant: small-caps;">rero ils</span> has increased considerably. A substantial job was done on the <span style="font-variant: small-caps;">mef</span>'s service itself, which grew from 96 person records during the tests to the full batch of 6.8 million records.

In <span style="font-variant: small-caps;">rero ils</span>, the existing links between bibliographical records and person authorities have been imported and are materialized by hyperlinks to display the person record. From a technical point of view, the person record is not imported into <span style="font-variant: small-caps;">rero ils</span>, but is remotely interrogated in real time.

During cataloguing, the editor enables you to search in real time via the <span style="font-variant: small-caps;">mef</span> service, for a person authority among the 6.8 million existing authorities and to register a link if the desired authority exists. Otherwise, the author's data is stored in text form in the bibliographic record. The mechanism of temporary authorities has yet to be modelled and developed.

{{< figure src="/img/0a21-edit-authority.png" width="300px" caption="Search of an person authority as cataloging a new document" alt="Search of an person authority as cataloging a new document screenshot" >}}
