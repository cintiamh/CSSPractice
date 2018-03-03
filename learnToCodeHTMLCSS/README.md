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

## Semantics overview

Semantic code describes the value of content on a page, regardless of the style or appearance of that content.

## Identifying Divisions & Spans

`<div>` & `<span>` are HTML elements that act as containers solely for styling purposes.

### Block vs Inline elements

* Block-level elements begin on a new line, stacking one on top of the other, and occupy any available width.
* Inline-level elements do not begin in a new line. They fall into the normal flow of a document, and only maintaining the width of their content.

## Using text-based elements

### Headings

Headings help to quickly break up content and establish hierarchy.

They also help search engines to index and determine the content on a page.

```html
<h1>Heading Level 1</h1>
<h2>Heading Level 2</h2>
<h3>Heading Level 3</h3>
<h4>Heading Level 4</h4>
<h5>Heading Level 5</h5>
<h6>Heading Level 6</h6>
```

### Paragraphs

```html
<p>Steve Jobs was a co-founder and longtime chief executive officer at Apple. On June 12, 2005, Steve gave the commencement address at Stanford University.</p>
```

### Bold text with strong

* `<strong>` is semantically used to give *strong importance* to text.
* `<b>` semantically means to *stylistically offset* text.

```html
<!-- Strong importance -->
<p><strong>Caution:</strong> Falling rocks.</p>

<!-- Stylistically offset -->
<p>This recipe calls for <b>bacon</b> and <b>baconnaise</b>.</p>
```

### Italicize text with emphasis

* `<em>` is used semantically to place *stressed emphasis* on text.
* `<i>` is used semantically to convey text in an alternative voice or tone, almost as if it were placed in quotation marks.

```html
<!-- Stressed emphasis -->
<p>I <em>love</em> Chicago!</p>

<!-- Alternative voice or tone -->
<p>The name <i>Shay</i> means a gift.</p>
```

## Building structure

HTML5 introduced new structurally based elements.

![](building-structure.png?raw=true)
