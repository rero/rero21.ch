This project is the source code of the [rero21.ch](https://rero21.ch) website.

## Install

To run rero21.ch :

1. Install [Hugo](https://gohugo.io/getting-started/installing/)
1. Fork and/or clone the repo : `git clone https://github.com/rero/rero21.ch.git`
1. Initialize the [theme submodule](https://github.com/rero/hugo-bootstrap) with `git submodule update --init`
1. Run the site locally with `hugo server -D`

## Shortcodes

### Smallcaps

In order to add acronym in small caps, you can use the following shortcode:

   {{< smallcaps "rero" >}}

### Images

Put the image in the `static/img/` folder and use the hugo built-in
[figure shorcode](https://gohugo.io/content-management/shortcodes/#figure)

### Videos

To add video, put your video in `webm` and `mp4`, with the exact same file name
in the `static/vid/` folder and use the following shortcode:

   {{< video src="<filename>" legend="<the legend below the video>" >}}
