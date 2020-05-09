# Primitive Hugo theme

## Usage

### Linking to pages by route name

The theme includes a shortcode, whick allows you to link to a page by using it's `route` parameter.

For a page:

```
---
title: "Route page"
date: 2018-12-08T06:22:26+01:00
route: "page-route"
---

This is a page.

```
Using

```
{{< linkto route="page-route" >}}
```

will render:

```
<a href="page.html">Route page</a>
```

or

```
{{< linkto route="bulgaria" title="My Page title">}}
```
will render:

```
<a href="page.html">My Page title</a>
```

## Installation

In your Hugo site `themes` directory, run:

```
$ git clone https://github.com/aquilax/primitive
```

Next, open `config.toml` in the base of the Hugo site and ensure the theme option is set to `primitive`.

```
theme = "primitive"
```

For more information read the official [setup guide](https://gohugo.io/getting-started/installing/) of Hugo.

## License

This theme is released under the [MIT license](https://github.com/aquilax/primitive/blob/master/LICENSE).
