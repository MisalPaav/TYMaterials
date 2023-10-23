# Unit 2: Introduction to HTML

- [Unit 2: Introduction to HTML](#unit-2-introduction-to-html)
    - [What is HTML?](#what-is-html)
    - [HTML Documents](#html-documents)
    - [Basic Structure of an HTML Document](#basic-structure-of-an-html-document)
    - [Creating an HTML Document](#creating-an-html-document)
    - [Markup Tags](#markup-tags)
    - [Heading-Paragraphs](#heading-paragraphs)
    - [Line Breaks](#line-breaks)
    - [HTML Tags](#html-tags)

### What is HTML?

HTML, which stands for HyperText Markup Language, is the standard language used to create web pages and web applications. It provides a structured way to define the content and elements on a web page, including text, images, links, and multimedia. HTML documents are interpreted by web browsers to render the visual presentation of a website, and they form the foundation of the World Wide Web.

HTML is composed of various elements and tags that structure content and provide the necessary instructions to browsers on how to display the information. These tags are written in angle brackets, such as `<tagname>`, and are used to define and wrap around elements within a web page.

### HTML Documents

An HTML document, often referred to as an HTML file or web page, is a text file with an .html or .htm extension that contains the content and structure of a web page. HTML documents are comprised of various HTML elements, and they can also include CSS (Cascading Style Sheets) and JavaScript to enhance the presentation and functionality of the page.

An HTML document typically includes the following components:

- **Document Type Declaration (DOCTYPE):** This declaration specifies the HTML version being used and is placed at the very beginning of the document to ensure the correct rendering of the page.

- **`<html>`:** The root element that encloses all content on the web page.

- **`<head>`:** Contains metadata about the document, including the title, character encoding, and links to external resources like CSS and JavaScript files.

- **`<title>`:** Sets the title of the web page, which is displayed in the browser's title bar or tab.

- **`<body>`:** Contains the visible content of the web page, including text, images, links, and other elements.

Here's a simple example of an HTML document structure:

```html
`<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>My First Web Page</title>
</head>
<body>
    <h1>Welcome to My Web Page</h1>
    <p>This is a simple HTML document.</p>
</body>
</html>
```

### Basic Structure of an HTML Document

The basic structure of an HTML document is as follows:

- **<!DOCTYPE html>:** This declaration defines the document type and version of HTML being used. In HTML5, `<!DOCTYPE html>` is used to specify the document type.

- **`<html>`:** The root element that encapsulates the entire HTML document.

- **`<head>`:** This section contains metadata about the document, such as character encoding, title, and links to external resources like CSS and JavaScript files.

- **`<title>`:** The title element specifies the title of the web page, which is displayed in the browser's title bar or tab.

- **`<body>`:** The body element contains the visible content of the web page, including text, images, links, and other elements.

### Creating an HTML Document

Creating an HTML document is a straightforward process. You can use any text editor, such as Notepad (Windows), TextEdit (macOS), or dedicated code editors like Visual Studio Code or Sublime Text. Follow these steps to create a basic HTML document:

1. **Open a Text Editor:** Launch your preferred text editor.

2. **Start with the Document Type Declaration:** Begin your HTML document with the `<!DOCTYPE html>` declaration. This tells the browser that you're using HTML5.

3. **Create the HTML Structure:** Build the basic structure of your document by adding the `<html>`, `<head>`, and `<body>` elements.

4. **Set the Document Title:** Inside the `<head>` section, use the `<title>` element to set the title of your web page.

5. **Add Content:** In the `<body>` section, insert various HTML elements to create the content of your page, including text, images, and links.

6. **Save the File:** Save the file with an .html extension. For example, you can name it `index.html`.

7. **Preview in a Web Browser:** Open the HTML file in a web browser to see how your web page is displayed.

### Markup Tags

HTML uses tags to define and structure elements within a web page. Tags are enclosed in angle brackets, and most have an opening tag `<tagname>` and a closing tag `</tagname>`. The opening tag signifies the beginning of an element, and the closing tag indicates the end. Some HTML elements are self-closing and do not require a closing tag.

Here are some common HTML tags and their usage:

- `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`: Headings of different levels. `<h1>` is the highest level, and `<h6>` is the lowest.

```html
<h1>This is a top-level heading</h1>
<h2>This is a subheading</h2>
```

- `<p>`: Defines a paragraph of text.

html

`<p>This is a paragraph of text.</p>`

- `<a>`: Creates hyperlinks. It uses the `href` attribute to specify the destination URL.

html

`<a href="https://www.example.com">Visit Example.com</a>`

- `<img>`: Embeds images in a web page. It uses the `src` attribute to specify the image file.

html

`<img src="image.jpg" alt="Description of the image">`

- `<br>`: Represents a line break within the text, useful for creating line breaks or spacing within content.

```html
This is the first line.<br>
This is the second line.
```

### Heading-Paragraphs

Headings and paragraphs are essential for structuring the content of a web page. Headings are used to create section titles and subtitles, while paragraphs are used to present textual content. HTML provides six levels of headings, from `<h1>` (the highest level) to `<h6>` (the lowest level). Paragraphs are created using the `<p>` tag.

Here's an example of using headings and paragraphs in an HTML document:

```html
<h1>Main Heading</h1>
<p>This is a paragraph of text. Paragraphs are used to structure textual content within a web page.</p>

<h2>Subheading</h2>
<p>Another paragraph providing additional information.</p>
```

In this example, `<h1>` is used for the main heading, `<h2>` for a subheading, and paragraphs are created with `<p>` tags. These elements help organize content and improve readability.

### Line Breaks

HTML uses the `<br>` tag to insert line breaks within text. This tag is particularly useful when you want to create a new line without starting a new paragraph. It's often used in cases where you need to control the line breaks within content.

For example, if you want to create a list with line breaks, you can use the `<br>` tag like this:

```html
<ul>
    <li>Item 1<br></li>
    <li>Item 2<br></li>
    <li>Item 3</li>
</ul>
```

In this example, the `<br>` tag is used within the list items to ensure each item is on a new line. This can be especially handy when customizing the formatting of your content.

### HTML Tags

HTML tags are the building blocks of HTML documents, and they define the structure and content of a web page. Tags are enclosed in angle brackets and typically come in pairs, consisting of an opening tag and a closing tag. Some tags are self-closing, meaning they don't require a separate closing tag. Here are some essential HTML tags:

- **`<!DOCTYPE html>`:** Specifies the document type and version of HTML. For HTML5, it's simply `<!DOCTYPE html>`.

- **`<html>`:** The root element that encloses all other elements on the web page.

- **`<head>`:** Contains metadata about the document, such as the character encoding, title, and links to external resources.

- **`<title>`:** Sets the title of the web page, which is displayed in the browser's title bar or tab.

- **`<meta>`:** Defines metadata about the document, including character encoding.

- **`<link>`:** Establishes links to external resources like CSS stylesheets.

- **`<script>`:** Embeds JavaScript code within the HTML document.

- **`<style>`:** Contains CSS styles for styling the web page.

- **`<body>`:** Contains the visible content of the web page, including text, images, and other elements.

- **`<h1>`, `<h2>`, ..., `<h6>`:** Create headings of different levels. `<h1>` is the highest level, and `<h6>` is the lowest.

- **`<p>`:** Defines paragraphs of text.

- **`<a>`:** Creates hyperlinks. The `href` attribute specifies the destination URL.

- **`<img>`:** Embeds images in the web page. The `src` attribute specifies the image file.

- **`<br>`:** Represents a line break within the text.

- **`<ul>`:** Defines an unordered list.

- **`<ol>`:** Defines an ordered (numbered) list.

- **`<li>`:** Represents list items within `<ul>` or `<ol>` lists.

- **`<table>`:** Defines a table.

- **`<tr>`:** Represents a table row.

- **`<th>`:** Defines table headers (for column or row headers).

- **`<td>`:** Defines table data (for cells within the table).

- **`<div>`:** A container element used for grouping and applying styles to content.

These are just a few of the many HTML tags available for creating web pages. HTML tags are combined to create the structure and appearance of web content, and they are essential for building websites and web applications.
