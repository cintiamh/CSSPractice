# HTML5 and CSS3

https://www.theodinproject.com/courses/html5-and-css3

## Basic HTML page structure

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Hello World</title>
    <link rel="stylesheet" href="main.css">
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
```

CSS Reset templates:
* https://meyerweb.com/eric/tools/css/reset/

### Getting to know HTML

https://learn.shayhowe.com/html-css/getting-to-know-html/

#### Semantic overview

* use proper element to give meaning and structure.
* Benefits: screen readers, search engines, use semantic elements to interpret meaning.

#### Divs & Spans

* Containers for styling purposes. No meaning.
* `<div>`: block-level element. Large groupings of content.
* `<span>`: inline-level element. Smaller groupings of text within a block-level element.

#### Text based elements

* `<h1>` to `<h6>`: block-level elements. They are key identifiers for users and search engines.
* `<p>`: block-level element. Paragraph.
* `<strong>`: inline-level element. Makes the text bold and with strong importance.
* `<em>`: inline-level element. Italicize text and place emphasis on it.

#### Building structure

[Structure](https://learn.shayhowe.com/assets/images/courses/html-css/getting-to-know-html/building-structure.png)

* `<header>`: top of a page, article, section, or other segment of a page.
* `<nav>`: primary navigation sections only.
* `<section>`: a thematic grouping of content.
* `<article>`: section of independent, self-contained content that may be independently distributed or reused.
* `<aside>`: sidebars, brief explanations, that is related to the content surrounding it.
* `<footer>`: closing or end of a page, article, section, or other segment of a page.

#### Hyperlinks

Relative path:
```html
<a href="about.html">About</a>
```

Absolute path:
```html
<a href="http://www.google.com/">Google</a>
```

E-mail:
```html
<a href="mailto:shay@awesome.com?subject=Reaching%20Out&body=How%20are%20you">Email Me</a>
```

Opening links in a new window:
```html
<a href="http://shayhowe.com/" target="_blank">Shay Howe</a>
```

Linking to parts of the same page:
```html
<body id="top">
  ...
  <a href="#top">Back to top</a>
  ...
</body>
```

### Best practices
