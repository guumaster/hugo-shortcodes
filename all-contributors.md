
## All Contributors

This shortcode is based on the [All Contributors spec](https://github.com/all-contributors/all-contributors)

### Setup

copy `.all-contributorsrc` to your hugo site `<hugo-site-root>/data/contributors.json` before running `hugo` command.


### Usage 

Add the shortcode wherever you want to show the list of contributors.

```
## Contributor list:

{{<contributors>}}

```

**IMPORTANT**: CSS is not included, you can add [css](layout/partials/all-contributors.html) to your head css or tweak the following code as you like. 

```css
  ul.contributors {
    list-style-type: none;
  }

  ul.contributors:after {
    content: '';
    width: 100%;
  }

  .contributors li {
    text-align: center;
    display: inline-block;
    padding-bottom: 20px;
    margin-left: 10px;
    width: 150px;
  }

  .contributors li img {
    text-align: center;
    width: 100px;
    border-radius: 50%;
  }
```

