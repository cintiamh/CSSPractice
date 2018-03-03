# Learn to Code HTML & CSS
https://learn.shayhowe.com/html-css/

1. [Building your first web page](#building-your-first-web-page)
2. [Getting to know HTML](#getting-to-know-html)

# Building your first web page

* HTML (HyperText Markup Language) - gives **content structure** and meaning.
* CSS (Cascading Style Sheets) - presentation language created to style the **appearance** of content.

## Common HTML terms

* Elements `div`
* Tags
  - Opening tag: `<div>`
  - Closing tag: `</div>`
  - Content in between these tags is the content of that element.
* Attributes: properties used to provide additional information about the element.

![](html-syntax-outline.png?raw=true)

## Setting up the HTML document structure

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Hello World!</title>
</head>
<body>
  <h1>Hello World!</h1>
  <p>This is a web page.</p>
</body>
</html>
```

### Self-closing elements

* `<br>`
* `<embed>`
* `<hr>`
* `<img>`
* `<input>`
* `<link>`
* `<meta>`
* `<param>`
* `<source>`
* `<wbr>`

## Common CSS terms

* Selectors
* Properties
* Values

![](css-syntax-outline.png?raw=true)

## Working with selectors

* Type selectors: element type
  - `div { ... }`
* Class selectors: element's class attribute (multiple)
  - `.awesome { ... }`
* ID selectors: element's id attribute (unique)
  - `#cintia { ... }`
* Additional selectors (later)

## Referencing CSS

```html
<head>
  <link rel="stylesheet" href="main.css">
</head>
```

## Using CSS resets

Eric Meyer's reset https://meyerweb.com/eric/tools/css/reset/

# Getting to know HTML
