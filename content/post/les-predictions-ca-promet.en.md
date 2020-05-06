---
title: "Predictions? Very promising!"
date: 2020-05-05T07:14:42+02:00
publishdate: 2020-05-06
draft: false 
tags: ["rero-ils", "release"]
---

While 
[sprint
29](https://tree.taiga.io/project/rero21-reroils/wiki/sprint-info-page-29) 
is over and [sprint
30](https://tree.taiga.io/project/rero21-reroils/wiki/sprint-info-page-30) is already well underway, [version
`v0.8.0`](https://github.com/rero/rero-ils/releases/tag/v0.8.0) of {{<
smallcaps "rero ils" >}} is published ([complete release
notes](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v080)).
Below is a brief summary of what's new.

<!--more-->

Predictions for serials have become possible, with a flexibility which enables
to encode the most common cases. Specifically, the *holdings* for serials can
be edited and a section of the form is dedicated to prediction. This is done in
two steps, the first to parameterize the sequence itself, and the second to
configure its display, by means of a *template* mechanism. Ten of the most
frequent predictions in RERO network libraries have been successfully imported.

## Transaction history 

The reader account as seen by the librarian is enriched with a tab displaying
the history of transactions. For the time being, and in accordance with the
rules in force, this history lists the transactions over the last six months.
In the future, the reader may decide whether this history is accessible or not.
However, it will be necessary for the proper functioning of libraries to keep a
transaction history for an item, although limited in time.

## Yearly subscriptions

Fee management now allows to manage yearly subscriptions, which is an existing
practice in some cantons or municipalities in Switzerland.

## Manual edition of the list of requests

The librarian was already able to place a request on an item for a reader, he
or she can now edit the list of existing requests for an item: add a new
request, delete one, or change the pickup location of one of the requests.

## Search results filtered by organization

Search in the professional interface now filters the results on the basis of
the organization of the connected person, as he or she works mostly on items
belonging to his/her network. A new organizational facet, with the relevant
organization selected by default, allows to restrict the results to a specific
library, or on the contrary to extend the search to the entire catalogue of
{{< smallcaps "rero ils" >}} organizations, for instance to attach an item to an
existing bibliographic record of another organization.\
This default filter also applies to the search suggestions generated when
typing a request.

{{< video src="ils-pro-result-filter" legend="Default filter for search results" >}}

## Integration of IdRef authorities into MEF

Finally, it can be pointed out that the person authorities of the IdRef
authority file have been added to the multilingual authority server
[{{< smallcaps "mef" >}}](https://mef.test.rero.ch) and are visible in
{{< smallcaps "rero ils" >}}, in view of the day when the
{{< smallcaps "rero" >}} authorities will be uploaded to this file.
