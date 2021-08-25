---
title: "Petit retour sur le go-live RERO ILS"
publishdate: 2021-09-13
draft: false
tags: ["rero-ils", "go-live"]
---

Le lundi 12 juillet 2021 est une date dont RERO+ se souviendra longtemps: [58 bibliothèques](/reroils/migration2021-libraries/) ont effectué leur transition vers le nouveau système RERO ILS. Deux mois plus tard, nous jetons un regard sur cet événement et sur ses écueils.

<!--more-->

## Les écueils

Commençons par les obstacles rencontrées, car ce sont eux qui impactent l'expérience des utilisatrices et utilisateurs ainsi que le travail quotidien des collègues en bibliothèques. Des problèmes ont été constatés à trois niveaux:

1. **Performance.** La lenteur de réponse de RERO ILS a perturbé l'exploitation durant la première semaine. RERO+ a monitoré et suivi la situation de près afin d'apporter progressivement des solutions. L'infrastructure (capacité des serveurs notamment) a été redimensionnée pour mieux correspondre à l'amplitude de l'utilisation. D'un autre côté, RERO ILS a été optimisé à plusieurs niveaux pour être moins gourmand, car plusieurs requêtes étaient inutiles ou effectuées à double lors de l'utilisation de l'interface et le calcul automatique de certaines facettes coûtait cher en ressources.
2. **Bugs fonctionnels.** Les problèmes les plus dérangeants ont été identifiés à deux niveau: les notifications envoyées (rappels, avis de disponibilité, demandes, etc.) et l'interface SIP2 communiquant avec les bornes de prêt en self-service.
3. **Bugs engendrés par les données migrées**. Certaines données migrées avec des erreurs ont déclenché divers bugs qui étaient difficiles à anticiper. Cette situation est notamment due à la migration très complète depuis Virtua, puisque nous y avons récupéré les prêts, demandes et frais de retard, ce qui n'est pas le cas de beaucoup d'autres projets de ce genre. Nous corrigeons les données durant la phase de stabilisation.

## Un succès pour un pari ambitieux

Faisons un pas en arrière pour observer la fresque dans son ensemble:

* La date du go-live a été tenue.
* Le prêt et l'interface publique fonctionnent correctement, sauf cas particuliers.
* Le catalogage n'a pas mis en évidence de problème urgent, bien qu'il se réalise dans un format totalement novateur selon les règles RDA.

Globalement, RERO+ tire donc de cette migration un bilan positif, surtout en considérant le défi dont il s'agissait. En effet, cette migration s'est faite selon des échéances extrêmement serrées par rapport au développement des fonctionnalités, et sur un système jeune et totalement différent du précédent dans son fonctionnement. Par ailleurs, certaines migrations vécues ou connues ont parfois mené à des interruptions de service prolongées, ce qui n'a pas été le cas en 2021.

Nous saluons en particulier l'excellente collaboration avec les partenaires, en premier lieu les bibliothèques RERO ILS, mais aussi les fournisseurs de bornes de prêt tels qu'Infomedis et Bibliotheca.

{{< figure src="/img/reroplus-catalogs.png" caption="Les nouveaux catalogues de RERO+" alt="Capture d'écran des pages d'accueil des catalogues de RERO+." link="https://bib.rero.ch" >}}