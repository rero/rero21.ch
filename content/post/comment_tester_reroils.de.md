---
title: "Wie Sie RERO ILS testen können"
date: 2019-04-29
draft: false
tags: ["rero ils"]
---

Sie haben schon mehrmals von <span style="font-variant: small-caps">rero ils</span> gehört, aber Sie würden gerne mal konkret sehen, wie es aussieht? Sich Ihre eigene Meinung bilden und sich die Hände schmutzig machen? Das trifft sich gut: <span style="font-variant: small-caps">rero ils</span> ist eine freie Software, die völlig transparent entwickelt wird.

<!--more-->

So geht's, auf drei Ebenen.

### Schritt um Schritt

#### Ebene 1: anonymer Nutzer / anonyme Nutzerin

* Besuchen Sie [ils.test.rero.ch](http://ils.test.rero.ch/)

Hier befindet sich die öffentliche Demo-Website. Auf dieser Ebene können Sie auf alle Funktionalitäten zugreifen, die für nicht angemeldete Personen vorhanden sind.

#### Ebene 2: Leser/Leserin

* Öffnen Sie die <span style="font-variant: small-caps">rero ils</span>-Hilfeseite (*Menü* > *Hilfe*) oder klicken Sie [einfach hier](https://github.com/rero/rero-ils/wiki/Public-demo-help#sign-up-and-log-in)
* Kopieren Sie die Login-Daten eines Lesers, unter *Sign up and Log in*, zum Beispiel die von Simonetta (`reroilstest+simonetta@gmail.com` / `123456`)
* Kommen Sie zurück auf <span style="font-variant: small-caps">rero ils</span> und melden Sie sich an (*Mein Konto* > *Login*)

Auf dieser Ebene können Sie unter anderem Ihr Konto anzeigen und Dokumente bestellen.

#### Ebene 3: Bibliothekar/Bibliothekarin

* Befolgen Sie die Schritte der Ebene 2, aber verwenden Sie eher die Login-Daten von Astrid zum Beispiel (`reroilstest@gmail.com` / `123456`)

Hierbei werden Sie <span style="font-variant: small-caps">rero ils</span> als Systembibliothekar testen, das heisst mit erweiterten Rechten! Es wird unter anderem möglich sein, Ausleihen durchzuführen, die Ausleihdauer und Anzahl erlaubter Verlängerungen einzustellen, Leser/Leserinnen zu registrieren, Dokumente zu katalogisieren oder die Öffnungszeiten einer Bibliothek zu verwalten.

### Eine Benachrichtigung für jede neue Version von RERO ILS?

Das [Github-Konto von RERO](https://github.com/rero) sammelt die verschiedenen Software-Projekte der Zentrale. Da befindet sich unter anderem das Projekt [RERO ILS](https://github.com/rero/rero-ils/) und seine aufeinanderfolgenden [Versionen/Releases](https://github.com/rero/rero-ils/releases).

1. Über **RSS-Feeds**:
	* Gehen Sie auf die [RERO ILS-Releases](https://github.com/rero/rero-ils/releases)
	* Kopieren Sie die URL und fügen Sie `.atom` hinzu: https://github.com/rero/rero-ils/releases.atom
	* Fügen Sie diese URL in ihr RSS-Tool!
2. Über **E-Mail** (setzt voraus, dass Sie ein Github-Konto haben oder erstellen)
	* Gehen Sie auf die [RERO ILS-Releases](https://github.com/rero/rero-ils/releases)
	* Oben rechts, klicken Sie auf *Watch*, und dann *Release only*
	* Geben Sie in Sektion *Watching* Ihrer Einstellungen an, dass Sie die Benachrichtigungen per E-Mail bekommen möchten

### Noch einen Schritt weiter... und uns Bugs oder Anregungen mitteilen

Es fehlen wesentliche Funktionalitäten?

* Der *Backlog*, eine Liste der nächsten vorgesehenen Entwicklungen, ist auf unserem Kollaborationswerkzeug [Taiga](https://tree.taiga.io/project/rero21-reroils/backlog) öffentlich zugänglich. Beim Erkunden der Plattform werden Sie die bei den Entwicklern laufenden Aufgaben und die ganze Historie der bereits implementierten *User Stories* finden.

Sie haben einen Fehler gefunden?

* Wenn Sie alles richtig machen wollen, bitte konsultieren Sie die [Probleme](https://github.com/rero/rero-ils/issues) (*Issues* im Github-Jargon), die bereits gemeldet worden sind. Sie können sogar selbst ein Issue öffnen, falls Sie ein Github-Konto besitzen.
* Wenn es in den Issues nichts gibt (und auch wenn Sie es nicht geprüft haben), können Sie uns gerne Ihre Rückmeldungen per [E-Mail](info@rero.ch) oder über den [öffentlichen Chat](https://gitter.im/rero/reroils) (Anmeldung erforderlich) senden. Wir verpflichten uns, Ihnen zu antworten!

Vielen Dank im Voraus für Ihre Teilnahme und Ihre Tests!