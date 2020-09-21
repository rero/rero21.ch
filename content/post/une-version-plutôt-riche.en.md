---
title: "A feature-rich version"
publishdate: 2020-06-04
draft: false 
tags: ["rero-ils", "release", "search", "circulation", "metadata", "display"]
---

A new version of RERO ILS has been released, fairly rich in
new features, which of course we are delighted about. Below is a brief summary
of the main new features. The full release note, consisting mostly of technical
information, is available in English on the GitHub project: [`v0.9.0`][1].

<!--more-->

## Research improvement

For a long time now, the team of librarians have been insisting on this point
and the [pilot library tests][2] have confirmed this: to search in a library
catalogue, the default application of the boolean operator `AND` is expected,
in order to reduce noise, even if it means there is no result. This is now
completed. At the same time, the whole indexing of data and the search function
have been reviewed and the improvements are significant.

## Closed stacks

[UCLouvain][3], which actively collaborates in the development of
RERO ILS, had suggested the implementation of *closed 
stacks*, i.e. the ability to block requests or to restrict pick-up locations for
a given location. After suggesting it, [UCLouvain][3] achieved that
development.

{{< figure src="/img/rero-ils-paging.png" caption="Editing a location, with restrictions on the pick-up locations" >}}

## Manual blocking of readers

It is now possible to block a reader manually. A free text note can be added to
explain the reason for this blocking. The blocked person can no longer borrow
items or place requests.  In his/her account, he/she is notified of the
blockage and the reason for it. The Librarian is also notified during loan
transactions that are no longer possible (lending or placing a request for the
reader).

## Metadata and display of records

Work on implementing the data model carries on with the fields of physical
description of the documents: material importance, duration, format,
illustrations, colours and material elements. These fields are clearly based on
the RDA standard, with a finer granularity, whereas MARC
used to gather different types of information within the same sub-field. While
working to display these fields in the record (the detailed view of the
documents), the layout has been reviewed and improved: essential information is
highlighted at the top and additional bibliographical details appear in a
dedicated tab.

{{< video src="new-document-detailed-view" legend="Reorganization of the bibliographic record (professional interface)" >}}


[1]: https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v090
[2]: /en/rero-ils-s-expose-aux-tests/
[3]: https://uclouvain.be/en/libraries
