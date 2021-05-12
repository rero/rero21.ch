---
title: "V1.2.0 is out: thanks for the translations!"
date: 2021-05-20
draft: false
tags: ["multilinguism", "release", "rero-ils"]
---

After another intense sprint at RERO+ and UCLouvain, the arrival of version
`v1.2.0` brings its share of new features and fixes to stabilize RERO ILS
before the *go-live* on July 12th. The complete release notes are available on
[GitHub][release-notes]. This is an opportunity for us to highlight the
community aspect of RERO ILS with the system's translation processes.

<!--more-->

## RERO ILS community translation

In order to be open and accessible, RERO ILS must also be multilingual. In this
perspective, the software is translated with the help of the [Weblate
service](https://hosted.weblate.org/projects/rero_plus/rero-ils/), which allows
the development team as well as external people to collaborate. Indeed, the
community can submit translations for the project. We would like to thank the
following members for their contributions:

- [Ambros Gattlen](https://hosted.weblate.org/user/ambgat/)
- [phlostically](https://hosted.weblate.org/user/phlostically/)
- [Adolfo Jayme Barrientos](https://hosted.weblate.org/user/Fito/)
- [Allan Nordhøy](https://hosted.weblate.org/user/kingu/)

If you would like to contribute as well, please visit [the project page on
Weblate](https://hosted.weblate.org/projects/rero_plus/#information).

## Several organisations for one patron

Among the many [new features][release-notes] of `v1.2.0` is the possibility of
registering at libraries of multiple organisations using the same account,
which is clearly a requirement of RERO+ libraries.

As previously [stated](/nouvelle-version-1.1.0/), user circulation data is not
shared between different organisations; however, it is likely that individuals
are registered in libraries of different organisations, for instance once in
the RERO Valais network and once in the RBNJ (Neuchâtel-Jura) network. Patrons
can now view their data (loans, history, fines, etc.) from their different
libraries through a dropdown menu on their account page. They don't need to
switch interfaces or log out to access this information.

{{< video src="patron-profile-several-orgs" legend="A patron consults her circulation data in different RERO ILS organizations" >}}

[release-notes]: https://github.com/rero/rero-ils/blob/dev/RELEASE-NOTES.rst#v120
