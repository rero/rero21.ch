---
title: "How to test RERO ILS?"
date: 2019-04-29
draft: false
tags: ["rero-ils"]
---

You have already heard several times about <span style="font-variant: small-caps">rero ils</span>, but you would like to see what it concretely looks like? To make up your own mind, get your hands dirty? How perfect: <span style="font-variant: small-caps">rero ils</span> is an open source software, developed in a fully transparent approach.

<!--more-->

Here's how to do it, at three levels.

### Step by step

#### Level 1: anonymous user

* Go to [ils.test.rero.ch](http://ils.test.rero.ch/)

That is where you will find our public demo website. At this stage, you only have access to features for people who are not logged in.

#### Level 2: patron

* Open the help page of <span style="font-variant: small-caps">rero ils</span> (*Menu* > *Help*) or click [directly here](https://github.com/rero/rero-ils/wiki/Public-demo-help#sign-up-and-log-in)
* Copy the login data of a patron, under *Sign up and Log in*, for example of Simonetta (`reroilstest+simonetta@gmail.com` / `123456`)
* Come back to <span style="font-variant: small-caps">rero ils</span> and log in (*My account* > *Login*)

At this level, you are able to consult your account or request documents.

#### Level 3: librarian

* Follow the procedure of level 2, but copy instead the login data of Astrid for example (`reroilstest@gmail.com` / `123456`)

Here, you are going to test <span style="font-variant: small-caps">rero ils</span> as a system librarian, therefore with extended rights! You can, among other things, make loans, configure their duration and the number of possible renewals, register patrons, catalogue documents or manage the opening hours of your library.

### An alert for every new version of RERO ILS?

The [Github account of RERO](https://github.com/rero) hosts the different software projects of the network. There you will find among others the [RERO ILS](https://github.com/rero/rero-ils/) project and its successive [versions/releases](https://github.com/rero/rero-ils/releases).

1. Via **RSS feed**:
	* Go to the [releases of RERO ILS](https://github.com/rero/rero-ils/releases)
	* Take the URL and add `.atom` to it: https://github.com/rero/rero-ils/releases.atom
	* Insert this URL in your RSS reader!
2. By **e-mail** (Github account required)
	* Go to the [releases of RERO ILS](https://github.com/rero/rero-ils/releases)
	* At the top right, click on *Watch*, and then *Release only*
	* Specify in your [settings](https://github.com/settings/notifications), section *Watching*, that you want to receive notifications by e-mail

### Go further... and report a bug or provide suggestions

Are some basic features missing?

* Our *backlog*, the journal of the upcoming planned developments, is freely accessible on our collaboration tool [Taiga](https://tree.taiga.io/project/rero21-reroils/backlog). Exploring a little further, you will find the ongoing tasks of the developers and the full history of the implemented user stories.

You encountered a bug?

* If you really want to do it right, check the already reported [issues](https://github.com/rero/rero-ils/issues). You can even open an issue yourself if you have a Github account.
* If there is no corresponding issue (and even if you haven't checked), your feedback is welcome by [e-mail](mailto:info@rero.ch) or via our [public chatroom](https://gitter.im/rero/reroils) (authentication required). We will get back to you!

Thank you in advance for your participation and your tests!
