---
title: "Two new releases"
date: 2019-06-03T08:33:41+02:00
publishDate: 2019-07-10
draft: false 
tags: ["rero-ils", "release"]
---

Since the [RERO Day](https://www.rero.ch/page.php?section=communique&pageid=reroday2019_fr) in March 2019, two versions of RERO ILS have been released. They provide a consolidation of the existing system, early support of the consortial model, an improvement of the search engine and circulation notifications.

The version notes are as follows:

- https://github.com/rero/rero-ils/releases/tag/v0.1.0a22
- https://github.com/rero/rero-ils/releases/tag/v0.2.0

<!--more-->

## v0.1.0a22, Consolidation and consortium features

### Focus on code quality

This version highlights sprint 17 which aimed to solve as many identified problems as possible ([GitHub issues](https://github.com/rero/rero-ils/issues)), as well as to improve the quality of the code by increasing its coverage through [unit tests](https://en.wikipedia.org/wiki/Unit_testing) and by ensuring that it is better documented. At the end of the sprint, the code coverage by the tests increased from 77% to 89% (it now exceeds 91%) and there was no more uncommented code part left. Finally, 11 issues, listed at the end of the [release note](https://github.com/rero/rero-ils/releases/tag/v0.1.0a22), have been resolved.

### Multiple organisations: RERO ILS becomes multi-tenant

In addition to improvements to the user interface, both professional and non-professional, and to the circulation module, the support of the consortial model has been implemented. By consortial model, we mean the existence of several **organisations**, most often including several **libraries**, which in turn cover several **locations**. The existence of more than one organisation in RERO ILS implies that the data and actions of each organisation are properly isolated and processed.

### Better integration of ebooks

At the same time, the harvesting of ebook metadata from the *Cantook* platform for incorporation into the catalogue was rewritten in order to directly query the supplier's API and obtain better quality data, particularly the language of the document and the subjects.

## v0.2.0, Search and notifications

### Improvement of the search engine

Sprint 18 focused on improving research and extending loan notifications. Concerning the search engine, a more detailed examination was carried out on the fields to be indexed and on how to process the text before indexing (such as **removing accents and plural marks**), based on the types of search desired depending on each case. Indeed, one does not search in the same way in documents as in patrons’ files.

The next step is to improve the order in which the results are displayed, with a default display from most to least relevant. A **field boosting** has also been added, for example to give more importance to a result containing the searched word in the title rather than in a note.

### Loan notifications

As for notifications, a new resource (a distinct object type) has been created in RERO ILS, in order to manage them[^1]. This involves sending a notification (currently by e-mail and in English only, but [the next step is already planned](https://tree.taiga.io/project/rero21-reroils/us/703)) to the patron, for example when the requested book is available for him or her at the loan office, or when the due date for the borrowed documents is close.

### Enhanced professional roles

A new role, **system librarian**, is being implemented in addition to the two existing roles, **librarian** and **patron**. Permissions for these different roles have been defined, or redefined as the case may be, to take into account the simple consortial model. The *librarian* role generally has rights at the library level, while the *system librarian* role has rights extended to the entire organisation, but not beyond. This is the beginning of a somewhat more realistic rights management within our new system.

### Formalism

From this publication, the version number follows the [Semantic versioning](https://semver.org) recommendations, in order to be more accurate about the value of a release. As a result, the version number has been changed from `v0.1.0a22` to `v0.2.0`. This is still a version under active development, as the first digit is zero. It is therefore a new minor version (the second digit changes). Note that since this publication, an error in the generation of example data has had to be fixed, resulting in the release of patches, `v0.2.1`, `v0.2.2.2` and `v0.2.3`.

### To test and learn more

The latest published version is as always publicly available on [ils.test.rero.ch](https://ils.test.rero.ch), as well as a short help page on the [GitHub project wiki](https://github.com/rero/rero-ils/wiki/Public-demo-help), where you will find the login and password for the accounts available to test the demo site.   
If you encounter any problems, which is likely, do not hesitate to contact us through the following channels:

- the Gitter [reroils](https://gitter.im/rero/rero-ils) room,
- the [GitHub issues](https://github.com/rero/rero-ils/issues),
- the [email](mailto:info@rero.ch),
- the Twitter account [@rero_centrale](https://twitter.com/rero_centrale).

[^1]: The creation of this resource was leveraged to use a new version of the `invenio-records` module that allows the creation of one table per resource.
