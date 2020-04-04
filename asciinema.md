## Asciinema player

Instead of embedding an image and go to [asciinema.org](https://asciinema.org) you can add directly a player on your site with this shortcode.


### Setup 

* Player CSS

Add this code somewhere on your CSS partials:

```gotemplate
{{ if .Params.asciinema }}
  <link rel="stylesheet" type="text/css" href="{{ .Site.BaseURL }}css/asciinema-player.css"/>
{{ end }}
```

* Player JS

Add this code somewhere on your JS partials:

```gotemplate
{{ if .Params.asciinema }}
  <script src="{{ .Site.BaseURL }}js/asciinema-player.js"></script>
{{ end }}
```

* Copy [asciinema.html](layout/shortcodes/asciinema.html) to your `layout/shortcodes` folder. 

### Usage

To use this shortcode you need to enable the player on your front-matter properties and add the shortcode somewhere on the markdown:

```yaml
---
title: My post with a player
description: Step-by-step tutorial 
asciinema: true
---

# Watch the tutorial

{{<asciinema key="tutorial.cast" >}}

```

Your casts must be placed in `static/casts/<key>.cast` 

### Optional properties

This shortcode accepts the options that `<asciinema></asciinema>` tag support. Here is a list with default values:

With defaults:
* `cols=640`
* `rows=10`
* `start-at=0`
* `speed=1`

Only if setup:

* `autoplay`
* `preload`
* `loop`
* `idle-time-limit`
* `poster`
* `font-size`
* `theme`
* `title`
* `author`
* `author-url`
* `author-img-url`
