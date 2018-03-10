# Learn to Code HTML & CSS
https://learn.shayhowe.com/html-css/

1. [Building your first web page](#building-your-first-web-page)
2. [Getting to know HTML](#getting-to-know-html)
3. [Getting to know CSS](#getting-to-know-css)
4. [Opening the box model](#opening-the-box-model)
5. [Positioning content](#positioning-content)

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

* `<header>` used to identify the top of a page, article, section, or other segment of a page.
* `<nav>` identifies a section of major navigational links on a page.
* `<article>` is used to identify a section of independent, self-contained content within the element could be replicated elsewhere without any confusion.
* `<section>` used to identify a thematic grouping of content.
* `<aside>` holds content, such as sidebars, inserts, or brief explanations, that is related to the content surrounding it.
* `<footer>` identifies the closing or end of a page, article, section.

## Creating Hyperlinks

```html
<a href="http://shayhowe.com">Shay</a>
```

### Relative & Absolute paths

* Relative paths: do not include the domain. Pointing to another page in the same website.
* Absolute path: links to other websites outside of the current one.

### Linking to an email address

```html
<a href="mailto:shay@awesome.com?subject=Reaching%20Out&body=How%20are%20you">Email Me</a>
```

### Opening links in a new window

```html
<a href="http://shayhowe.com/" target="_blank">Shay Howe</a>
```

### Linking to parts of the same page

```html
<body id="top">
  ...
  <a href="#top">Back to top</a>
  ...
</body>
```

# Getting to know CSS

Within CSS, all styles cascade from the top of a style sheet to the bottom.

## Calculating specificity

1. `0-0-1`: type selector
2. `0-1-0`: class selector
3. `1-0-0`: ID selector

## Combining selectors

When selectors are combined they should be read from right to left.

```css
.hotdog p.mustard {
  background: yellow;
}
```

The best practice is to not prefix a class selector with a type selector.

## Layering Styles with multiple classes

```html
<a class="btn btn-danger">...</a>
<a class="btn btn-success">...</a>
```

```css
.btn {
  font-size: 16px;
}
.btn-danger {
  background: red;
}
.btn-success {
  background: green;
}
```

## Common CSS property values

### Color

Adobe Kuler: https://color.adobe.com/create/color-wheel/

### RGB & RGBa

RGB colors have the ability to create semi-transparent colors using RGBa.

```css
.task {
  background: rgba(128, 0, 0, .25);
}
.count {
  background: rgba(255, 255, 0, 1);
}
```

### Length

* Absolute lengths
  - Pixels: 1px == 1/96 in.
* Relative lengths
  - Percentages(`%`): are defined in relation to the length of another object.
    - helpful for setting the height and width of elements and building out a web page's layout.
  - Em (`em`): its length is calculated based on an element's font size.
    - When a font size is not explicitly state for an element, the `em` unit will be relative to the font size of the closest parent element with a stated font size.
    - Used for:
      - styling text (font size)
      - spacing around text (margin & padding)

# Opening the box model

## How are elements displayed?

### Display

* `display`
  - `block`
  - `inline`
  - `inline-block`: allow element to behave as a block-level element, accepting all box model properties. However, the element will be displayed in line with other elements, and it will not begin on a new line by default.
  - `none`: completely hide an element, as if that element doesn't exist.

## What is box model

Every element on a page is a rectangular box and may have `width`, `height`, `padding`, `border`, and `margin`.

![](box-model.png?raw=true)

* `width`
  - block-level: default width `100%`
  - inline-level expand and contract horizontally to accommodate their content.
  - Inline-level elements cannot have a fixed size, thus the width and height properties are only relevant to non-inline elements.
* `height`
  - default height is determined by its content.
* `border`
  - `width`
  - `color`
  - `style`
    - `solid`
    - `double`
    - `dashed`
    - `dotted`
    - `none`
* `border-radius`
* `box-sizing`
  - `content-box`: default. The size of an element begins with the `width` and `height` properties, and then any `padding`, `border`, and `margin` property values are added from there.
  - `padding-box`
  - `border-box`

```css
*,
*:before,
*:after {
	-webkit-box-sizing: border-box;
	   -moz-box-sizing: border-box;
	       -box-sizing: border-box;
}
```

# Positioning content
