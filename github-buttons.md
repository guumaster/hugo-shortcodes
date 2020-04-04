## Github buttons

Add any of the [Github Buttons](https://buttons.github.io/) to your site with a simple shortcode.


## Setup

* Add the required JS somewhere on your header or partial templates:

```gotemplate
<script async defer src="//buttons.github.io/buttons.js"></script>
```

* Copy [github-button.html](layout/shortcodes/github-button.html) to your `layout/shortcodes` folder. 


## Usage

Add the shortcode to your markdown:

* All three buttons star/fork/issues:
```gotemplate

{{<github-button repo="guumaster/hostctl" >}}
{{<github-button repo="guumaster/hostctl" type="fork" >}}
{{<github-button repo="guumaster/hostctl" type="issues" >}}
```

Optional properties:

* _repo_: set the `owner/repo` you want to link to.

* _type_: set the base URL of the button `star|fork|issues`.

* _size_: the size of the buttons. `<empty>|large`.

* _theme_: the base color of the buttons. `ligth|dark`

* _label_: Change the text of the button. Defaults to the type of button.

* _count_: set it to `true/false` to show counters or not.

