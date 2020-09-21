---
title: "Two important releases"
date: 2020-04-20T06:20:38+02:00
publishdate: 2020-04-23
draft: false 
tags: ["rero-ils", "release"]
---

At RERO, we're witnessing an acceleration of space-time,
especially in the RERO ILS project, and in this haste, we
"forgot" to inform you that two new releases have been published!

Below, a summary of the added features of these releases is proposed, but the
detailed notes can be accessed through the following links:

- [`v0.6.0`](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v060)
- [`v0.7.0`](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v070)

<!--more-->

## Release `v0.6.0`

Version `v0.6.0` (and its sibling `v0.6.1`, which is only a patch [as indicated
by its version number](https://semver.org "Semantic versioning explanations"))
separates the public interface from the professional interface. The public
interface, accessible to all with or without authentication, includes the
shared catalogue and the organisations' catalogues, as well as patron accounts
and the action that is available to them, such as requesting an item. The
professional interface gives access to all action undertaken by library staff,
as for instance searching in the catalogue, cataloguing or parameter setting.

This logical separation is partly the consequence of the introduction in the
version `v0.3.0`[^1] of views per organization. It became difficult to define
and clearly present the possible actions to be taken by a member of staff on
a particular view, or the information intended for any visitor or online
reader. Furthermore, the professional interface benefits from being dynamic, in
order to avoid recharging the page after each action, while the public
interface is more easily indexed by search engines if the pages are static,
which is relevant for bibliographic records. Finally, this choice allows to
share part of the professional interface between RERO ILS
and [SONAR](https://sonar.ch) projects and, thus, to
mutualize the development effort[^2].

The development of `v0.6.0` has been largely determined by the
[workshops](/en/tags/workshops) carried out and the establishment of a specific
instance for [pilot libraries’ tests](/en/rero-ils-s-expose-aux-tests). From
this point of view, it is now possible to customize the views of different
organizations with a specific header colour and logo. Most importantly, the
processes for Virtua's data migration to RERO ILS have been
completed in order to import an entire RERO institution.

The interface for the circulation module has been redesigned and now offers
more information on circulation events upon return of items requested, late or
in transit. The librarian now has a unified view of the reader's account in
different tabs: borrowed items, requests, fees, personal information. As for
the public interface, the account also offers new functionalities such as
extending loans, accessing loan history and cancelling requests.

Work continues on the data model with publication and editing fields, as well
as an editor supporting embedding of fields on four levels or more. And work on
the acquisition module has begun with the addition of fiscal years, accounts,
orders, order lines and suppliers.

## Release `v0.7.0`

Librarians are now able to place a request on an item for a reader, as shown in
the animation below. Professionals have a tab for the readers' fees with the
possibility of paying partially or completely for the fees, to cancel them, to
mark them as contested, or, conversely, to  resolve a dispute. A detailed
history is provided for the fees, along with the details of all events. These
fees are generated automatically when a loan has exceeded the return deadline.
They may also be related to other library services, such as photocopies,
interlibrary loans, subscriptions or for when an item has been damaged or lost. 

{{< video src="request_as_a_librarian" legend="Make a request on behalf of a patron" >}}

As for the data model, complex work has been carried out for the title and the
transformations needed for the conversion from MARC to JSON, as well as for the
URL addresses. A wiki has also been added in order to have  online help
available for the professional.

[^1]: See [release
  note](https://github.com/rero/rero-ils/blob/master/RELEASE-NOTES.rst#v030).
[^2]: For those of you who are interested in how it works under the hood, this
  change resulted in the creation of two more repositories on GitHub:
  [ng-core](https://github.com/rero/ng-core), an angular project that brings
  together what's common to RERO ILS and SONAR, as well as 
  [rero-ils-ui](https://github.com/rero/rero-ils-ui),
  also an angular project that implements the RERO ILS of
  the professional interface.
