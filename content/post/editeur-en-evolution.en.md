---
title: "The editor is making progress"
date: 2020-08-03T14:53:42+02:00
publishdate: 2020-08-04
draft: false
tags: ["rero-ils", "release", "display", "metadata"]
---

With another month elapsed, a new version of RERO ILS is available on the [test interface][1]. The work of the development team to improve the software continues with a new update that should be of interest to cataloguing professionals. Comprehensive release notes can be found on the project's Github page : [`v0.11.0`][2].

<!--more-->

## Professional interface: refining the document editor

As it is one of the librarians' main tools, particularly for cataloguing, the document editor must offer a clear and ergonomic interface, especially as this module must frequently display complex data according to rules that are not always obvious.

Work on fine-tuning this interface is constant and is evidenced in this version by an improvement in its readability.

{{< figure src="/img/rero-ils-improvededitor.png" caption="The readability of the editor has clearly been improved for this version">}}

This visual enhancement is accompanied by several adjustments: 
* New fields `partOf` (host document), `seriesStatement` (collection statement) and `issuance` (publishing mode) have been added. They allow the system to establish clean links between documents, a small revolution within the network where these links were previously based solely on character strings.
* The display of some translations has been fixed, especially in the _Add Field_ form. Please note that not all translations are up to date in this version due to a change of translation platform in progress. These problems will be corrected in the next version.
* Bugs in saving the documents have been fixed.
* The shortcut links _Go to_ in the right panel are now working.

## Inventory lists

Inventory lists are another new feature of the `v0.11.0`. Available in the professional interface through the _Reports & monitoring_ menu, they can display item lists, filter them and export them directly in `CSV` format.

At the same time, the items also have a new `second_call_number` field allowing them to have a second call number, which is also displayed in the inventory lists.

[1]: https://ils.test.rero.ch
[2]: https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v0110