[![Netlify Status](https://api.netlify.com/api/v1/badges/f6815aee-b7dc-4af9-b407-84744d1722ac/deploy-status)](https://app.netlify.com/sites/rero-21/deploys)

This project is the source code of the [rero21.ch](https://rero21.ch) website.

## Install

To run rero21.ch :

1. Install [Hugo](https://gohugo.io/getting-started/installing/)
1. Fork and/or clone the repo : `git clone
   https://github.com/rero/rero21.ch.git`
1. Initialize the [theme submodule](https://github.com/rero/hugo-bootstrap)
   with `git submodule update --init`
1. Run the site locally with `hugo server -D`

## Shortcodes

### Smallcaps

In order to add acronyms in small caps, you can use the following shortcode:

     {{< smallcaps "rero" >}}

### Tables

In order to add Bootstrap styling to a markdown table, wrap your markdown table
inside the shortcode like so: 

     {{< bootstrap-table "table table-striped table-bordered" >}}
     | Résultat de l'alignement     | Fréquence | % des monographies RERO |
     |:-----------------------------|----------:|------------------------:|
     | Aucune équivalence           | 2'954'451 |          65.2%          |
     {{< /bootstrap-table >}}

Use [bootstrap-table](https://getbootstrap.com/docs/4.4/content/tables/)
classes inside the `""` to customize your table.

### Images

Put the image in the `static/img/` folder and use the hugo built-in
[figure shorcode](https://gohugo.io/content-management/shortcodes/#figure)

### Videos

To add video, put your video in `webm` and `mp4`, with the exact same file name
in the `static/vid/` folder and use the following shortcode:

     {{< video src="<filename>" legend="<the legend below the video>" >}}
