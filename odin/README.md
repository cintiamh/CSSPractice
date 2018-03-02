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

#### HTML Coding practices

* Write standards-compliant markup: HTML is forgiving, but can be unpredictable.
* Make use of semantic elements: more semantic == more accessible
* Use the proper document structure: always use `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>`
* Keep the syntax organized:
  - lowercase within elements names, attributes, and values
  - indent nested elements
  - double quotes
  - use `/` at the end of self-closing elements
  - omit values on boolean attributes
* Use practical id and class values: values related to content (not style)
* Use the alternative text attribute on images
  - `<img src="puppy.jpg" alt="A beautiful, two-year-old hound mix puppy">`
* Separate content from style: don't use inline style within HTML.
* Avoid a case of "Divitis": avoid adding DIVs just to help with styling - prefer semantic elements.
* Continually refactor code: remember to remove old code and styles as necessary.

#### CSS coding practices

* Organize code with comments: logical groups with comments, build a table of contents at the top with comments.
* Write CSS using multiple lines & spaces
* Use proper class names
* Build proficient selectors: avoid ids, nest only 2 to 3 levels deep, shorter and primarily direct selectors.
* Use specific classes when necessary
* Use shorthand properties & values: instead of using `margin-top, margin-right, margin-left, margin-bottom`, just use `margin`
* Use shorthand hexadecimal color values
* Drop units from zero values
* Group and align vendor prefixes: group and indent individual vendor prefixes so that the property names stack vertically, as do their values.
* Modularize styles for reuse

## Linking internal and external pages

### The difference between absolute and relative paths

* Relative path
* Absolute path: the browser goes back to the internet and finds your site, and finds the file within your directory.

  If you're linking to pages on your own site, using relative path will make your site respond quicker.

### CSS Link pseudo-classes

* `:link` - unvisited links
* `:visited` - visited links
* `:hover` - hover state
* `:active` - activated state (short duration when clicking)
* `:focus` - focused state

#### Combining pseudo-classes

```css
a:link:hover {
  color: green;
}
```

#### Order of pseudo-classes

1. `a { }`
2. `a:link { }`
3. `a:visited { }`
4. `a:hover {}`
5. `a:focus { }`
6. `a:active { }`

In modern browsers, `:link` and `:visited` will behave differently in order to protect the privacy of a visitor's history.

## Working with images, video and other media

* Optimize your image sizes and filetypes.
* Trade-offs: image size x quality.

### Adding media
https://learn.shayhowe.com/html-css/adding-media/

#### Adding images

```html
<img src="dog.jpg" alt="A black, brown, and white dog wearing a kerchief">
```

Most supported image formats:
* `gif`
* `jpg`: photographs - (faster load times) high color counts while maintaining a decent file size.
* `png`: icons & background patterns - Images with transparency or low color counts.

The `<img>` element is `inline` by default.

To have the page content around the image element, you need to use `float`:

```css
img {
  background: #eaeaed;
  border: 1px solid #9799a7;
  float: right;
  margin: 8px 0 0 20px;
  padding: 4px;
}
```
