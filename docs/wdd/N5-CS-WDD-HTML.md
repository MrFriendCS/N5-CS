# Hypertext Markup Language (HTML) 

## HTML

HTML uses elements to display content.  An element normally consists of opening (`<tag>`) and closing (`</tag>`) tags, with the content to be display contained between the tags.

HTML is not whitespace sensitive.  This means a statement can be all on a single line or split over multiple lines.

``` html
<tag>content</tag>

<tag>
    content
</tag>
```

Opening tags can have attributes.

``` html
<tag attribute="value">
    content
</tag>
```

All elements in a HTML document are contained within the opening and closing `html` tags.

``` html
<!DOCTYPE html>
<html lang="en-gb">

</html>
```

## Information

### Comments

Single line comment.

``` html
<!-- This comment is not displayed -->
```

Multiline comment.

``` html
<!--
This comment is not displayed
This comment is not displayed
-->
```

### Display information

Without HTML tags information is displayed as plain text, but with tags it will have the formatting associated with the tag.

``` html
Hello world
```

## HTML document (Webpage)

A HTML documen has two main parts:

 * __head__: information about the page
 * __body__: the content that is displayed

``` html
<!DOCTYPE html>
<html lang="en-gb">

    <head>
    </head>

    <body>
    </body>

</html>
```

### Head

### Title

The webpage title will be displayed on the browser tab:

``` html
<title>My Web Page</title>
```

### Style

#### Internal

The [CSS](#css) for a webpage can be internal using the `style` tag.

``` html
<style>
    <!-- CSS rules go here -->
</style>
```

#### External

The [CSS](#css) for a webpage can be in an external file using the `link` element.

``` html
<link href="styles.css" rel="stylesheet" type="text/css">
```

___Note___: A few HTML elements do not have a closing tag, and `link` is one of them.



## Body

### Heading

There are six levels of heading.

``` html
<h1>Highest level heading</h1>

<h3>Mid-level heading</h3>

<h6>Lowest leveleast heading level</h6>
```

### Paragraph

``` html
<p>A paragraph of text.</p>
<p>Another paragraph of text.</p>
<p>Plus another paragraph of text.</p>
```

### Lists

Lists can be ordered (`ol`) or unordered `ul`).  Both types of lists contain list items (`li`).

#### Ordered list - Numbered


``` html
<ol>
    <li>First list item</li>
    <li>Another list item</li>
    <li>Last list item</li>
</ol>
```

#### Unorderd list - Bullet points


``` html
<ul>
    <li>First list item</li>
    <li>Another list item</li>
    <li>Last list item</li>
</ul>
```



## Division

The `<div>` tag is used to divide the webpage into different parts.

``` html
<div>
	<h1>First area</h1>
<div>

<div>
	<h1>Second area</h1>
<div>
```

## Anchor (Hyperlinks)

### External


Link to an external website, using absolute addressing.

``` html
<a href="https://mrfriendcs.github.io/">N5 CS Help</a>
```

### Internal

Link to another webpage, in the same folder, using relative addressing.

``` html
<a href="home.html">Home</a>
```

## Media

To ensure that media is displayed / played correctly the `type` attribute is used.

| File type | Type |
| --------- | ---- |
| jpeg / jpg | image/jpeg |
| png | image/png |
| mp3 | audio/mpeg |
| mp4 | video/mp4 |

### Image

The image tag (`<img>`) has two attributes.  The first (`src`) is where the image is located, and can use relative or absolute addressing.  The second (`alt`) is the alternative text that will be displayed if the image can't be displayed, and is used by screen readers.

``` html
<img src="laptop.jpg" alt="Laptop on a table">
```

### Audio

``` html
<audio controls src="clapping.mp3">  
    No audio player available
</audio>
```

### Video

``` html
<video controls src="clapping.mp4">  
	No video player available
</video>
```

## Classes and IDs

HTML elements can have additional attributes for `class` and `id` which are used for applying CSS rules to specific elements, and can be used by JavaScript.

A class can be assigned to one or more cascading Style Sheets (CSS), whereas an ID can only be applied to one element on a page.

### Classes

``` html
<p class="highlight">A paragraph.</p>
<p>Another paragraph.</p>
<p class="highlight">Plus another.</p>
```

### IDs

``` html
<p id="main">A paragraph.</p>
<p>Another paragraph.</p>
<p>Plus another.</p>
```

### Classes and IDs

An element can have an ID and a class.

``` html
<p id="main" class="highlight">A paragraph.</p>
<p>Another paragraph.</p>
<p class="highlight">Plus another.</p>
```
