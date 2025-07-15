# HTML Interview Questions & Answers

## Name of topic.

- HTML Doctype and Versions
- Semantic and Non-semantic Elements
- HTML Comments and Case Sensitivity
- HTML Page Structure
- Heading Tags
- Formatting Tags (`<b>`, `<i>`, `<u>`, etc.)
- Superscript and Subscript Tags
- Anchor (`<a>`) Tag and Attributes
- Target Attribute in Links
- Absolute vs Relative URLs
- Image Tag and Attributes
- Image Linking
- Inline vs Block Elements
- Iframe and Video Embedding
- Lists in HTML (`<ul>`, `<ol>`, `<dl>`)
- Nesting Lists
- HTML Table Basics
- Table Tags: `<thead>`, `<tbody>`, `<tfoot>`
- Colspan and Rowspan
- `<th>` vs `<td>`


---

## ✅ 1. What is HTML and why is it called a markup language?

**Answer:**
HTML means **HyperText Markup Language**. It is used to **create the structure of a webpage**, like headings, paragraphs, images, links, etc.
It is called a **markup language** because it uses **tags** (like `<p>`, `<h1>`, `<img>`) to "mark" parts of content — to tell the browser **what each part is**.

👉 Simple Example:

```html
<p>This is a paragraph.</p>
```

Here, `<p>` is a tag. It tells the browser: "This text is a paragraph."

---

## ✅ 2. What are the basic building blocks of an HTML document?

**Answer:**
Every HTML page is built using a **basic structure** with some important tags:

1. `<!DOCTYPE html>` – tells browser this is HTML5
2. `<html>` – main container for the whole page
3. `<head>` – contains hidden info like title, CSS, metadata
4. `<body>` – contains all visible content like text, images, forms

👉 Example:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Welcome</h1>
    <p>This is my first page.</p>
  </body>
</html>
```

---

## ✅ 3. What is the role of `<!DOCTYPE html>`?

**Answer:**
`<!DOCTYPE html>` tells the browser,
**"This page is written in HTML5."**

It helps the browser understand **how to read and show** your HTML content correctly.

If you don’t write this, browser may show the page with **old rules**, which can cause layout or display issues.

---

## ✅ 4. What is the difference between `<head>` and `<body>`?

**Answer:**

* `<head>` = for **information about the page** (not visible to users)
* `<body>` = for **everything that user can see** on the webpage

**`<head>` contains:** title, CSS links, meta info, favicon, etc.
**`<body>` contains:** text, headings, images, videos, buttons, etc.

👉 Simple View:

```html
<head>
  <title>This is title</title>   <!-- You see this in browser tab -->
</head>
<body>
  <h1>This is visible content</h1>  <!-- You see this on the page -->
</body>
```

---

## ✅ 5. What are void (empty) elements? Give examples.

**Answer:**
Void elements are **tags that do not have closing tags**.
They are self-closing — they don’t wrap any content.

👉 Examples:

* `<br>` – line break
* `<img>` – image
* `<hr>` – horizontal line
* `<input>` – input field
* `<meta>` – metadata info

👉 Example:

```html
<p>Hello<br>World</p>
```

Here `<br>` adds a new line between "Hello" and "World".

---

## ✅ 6. What is the difference between `<div>` and `<span>`?

**Answer:**
Both are container tags but used differently:

* `<div>` is a **block-level** element → takes full width
* `<span>` is an **inline** element → takes only the space it needs

Use `<div>` when you group **big sections**.
Use `<span>` when you style or group **small words/phrases** inside a line.

👉 Example:

```html
<div>This is a block</div>
<span>This is inline</span>
```

---

## ✅ 7. What is the difference between `<br>`, `<hr>`, and `<p>` tags?

**Answer:**

* `<br>` = line break (goes to next line without space)
* `<hr>` = horizontal line (used for section break)
* `<p>` = paragraph (adds space before and after text)

👉 Example:

```html
<p>First paragraph</p>
<hr>
<p>Second paragraph</p>
```

---

## ✅ 8. How does the `<pre>` tag work and where should it be used?

**Answer:**
`<pre>` means **preformatted text**.
It shows text **exactly as you type** — spaces, tabs, new lines are preserved.

Useful when showing code or poetry.

👉 Example:

```html
<pre>
  Hello World
    This is indented
</pre>
```

---

## ✅ 9. What are semantic tags? Why are they important for SEO and accessibility?

**Answer:**
Semantic tags describe the **meaning** of the content. They make the code more **understandable** for both browsers and screen readers.

👉 Examples: `<header>`, `<footer>`, `<nav>`, `<section>`, `<article>`

They help:

* Search engines understand your page
* Screen readers help disabled users
* Developers understand the layout better

---

## ✅ 10. Compare `<div>` with semantic tags like `<section>`, `<article>`, etc.

**Answer:**
`<div>` has **no meaning**, it is just a box.
Semantic tags **tell the purpose** of the content.

👉 Use:

* `<section>` for a section of the page
* `<article>` for a blog/news post
* `<nav>` for links

This improves code readability, SEO, and accessibility.

---

## ✅ 11. How is a form created in HTML? What are its attributes?

**Answer:**
A form is created using the `<form>` tag. It contains input fields and buttons.

Important attributes:

* `action`: where to send form data (URL)
* `method`: how to send data (GET or POST)

👉 Example:

```html
<form action="/submit" method="post">
  <input type="text">
  <input type="submit">
</form>
```

---

## ✅ 12. What is the purpose of `action` and `method` in `<form>`?

**Answer:**

* `action` → Tells **where to send** form data (like a server URL)
* `method` → Tells **how to send** data: `GET` (URL) or `POST` (hidden)

---

## ✅ 13. Explain different input types like text, radio, checkbox, etc.

**Answer:**
Some common input types:

* `text`: single-line input
* `password`: hides characters
* `radio`: choose one option
* `checkbox`: select multiple options
* `submit`: form submission button
* `email`, `file`, `date`, `range`, etc.

---

## ✅ 14. What is the role of `name`, `id`, and `value` attributes in input elements?

**Answer:**

* `name`: key sent to backend (important for form data)
* `id`: used to link with `<label>` or JavaScript
* `value`: default or pre-filled input value

---

## ✅ 15. How do `<fieldset>` and `<legend>` enhance forms?

**Answer:**
They are used to group related form elements and label them.

* `<fieldset>`: groups related inputs
* `<legend>`: gives a heading to that group

👉 Improves form organization and accessibility.

---

## ✅ 16. How does `required`, `placeholder`, and `autocomplete` affect user experience?

**Answer:**

* `required`: field must be filled before submit
* `placeholder`: hint text inside input box
* `autocomplete`: browser fills saved values automatically

---

## ✅ 17. How is a hyperlink created in HTML?

**Answer:**
Use the `<a>` tag:

```html
<a href="https://example.com">Click Here</a>
```

* `href`: URL to link to
* Text inside the tag is clickable

---

## ✅ 18. What are the possible values of the `target` attribute in `<a>`?

**Answer:**

* `_self`: open in same tab (default)
* `_blank`: open in new tab
* `_parent`, `_top`: used in frames

---

## ✅ 19. How can we create anchor links for sections on the same page?

**Answer:**

* Give `id` to a section
* Link with `#id`

👉 Example:

```html
<a href="#about">Go to About</a>
...
<h2 id="about">About Section</h2>
```

---

## ✅ 20. What is the difference between absolute and relative URLs?

**Answer:**

* **Absolute URL**: full address (starts with `http://` or `https://`)
  → Example: `https://site.com/page.html`
* **Relative URL**: depends on current location
  → Example: `images/photo.jpg`

---


---

## ✅ 21. How is an image added in HTML and what are its key attributes?

**Answer:**
Use the `<img>` tag with these attributes:

* `src`: path of the image
* `alt`: text if image fails to load (important for SEO)
* `width`, `height`: image size in pixels or %

👉 Example:

```html
<img src="image.jpg" alt="A cat" width="200">
```

---

## ✅ 22. Difference between `alt`, `title`, `width`, `height` in `<img>`?

**Answer:**

* `alt`: shows if image can't load (also used by screen readers)
* `title`: shows tooltip when mouse hovers
* `width`, `height`: set image size

---

## ✅ 23. How to make an image responsive in HTML/CSS?

**Answer:**
Use CSS:

```css
img {
  width: 100%;
  height: auto;
}
```

This makes image scale with screen size.

---

## ✅ 24. How do you embed audio and video in HTML?

**Answer:**
Use `<audio>` and `<video>` tags with `controls`:

```html
<audio controls>
  <source src="sound.mp3">
</audio>

<video controls width="320">
  <source src="movie.mp4">
</video>
```

---

## ✅ 25. What are the attributes used in `<audio>` and `<video>` tags?

**Answer:**

* `controls`: show play/pause buttons
* `autoplay`: start automatically
* `loop`: repeat forever
* `muted`: no sound initially
* `poster` (in `<video>`): shows image before video plays

---

## ✅ 26. How to provide fallback content in media tags?

**Answer:**
Write a message inside the tag:

```html
<video controls>
  <source src="video.mp4">
  Your browser does not support the video tag.
</video>
```

---

## ✅ 27. What is an iframe and how is it used?

**Answer:**
An `<iframe>` shows another webpage inside your page.

```html
<iframe src="https://example.com" width="400" height="300"></iframe>
```

---

## ✅ 28. What are the security issues related to iframes?

**Answer:**

* Can be used for phishing (clickjacking)
* Use `sandbox` to limit iframe power

👉 Safe usage:

```html
<iframe src="..." sandbox></iframe>
```

---

## ✅ 29. Use of `sandbox`, `allow`, and `srcdoc` in iframes?

**Answer:**

* `sandbox`: limits features (like forms, scripts)
* `allow`: gives permission (like camera, autoplay)
* `srcdoc`: writes inline HTML in iframe

👉 Example:

```html
<iframe srcdoc="<h1>Hello</h1>" sandbox></iframe>
```

---

## ✅ 30. What are different types of lists in HTML?

**Answer:**

* `<ul>`: unordered list (bullets)
* `<ol>`: ordered list (numbers)
* `<dl>`: description list (term + definition)

👉 Example:

```html
<ul><li>Item</li></ul>
<ol><li>Item</li></ol>
<dl><dt>Term</dt><dd>Definition</dd></dl>
```

---
