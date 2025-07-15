# HTML Interview Questions & Answers


##  Topic Covered

- Ordered, Unordered, and Description Lists
- List Numbering Styles
- Nested Lists
- Table Structure & Tags
- Thead, Tbody, Tfoot
- Colspan, Rowspan, TH vs TD
- Responsive Tables
- Meta Tags and Viewport
- `<link>` and `<style>` Tags
- External/Internal CSS
- `<script>` Tag
- CSS vs JS Tags
- Script `defer` and `async`
- Semantic Tags (`<header>`, `<main>`, `<section>`, etc.)
- Form Elements and Attributes
- GET vs POST
- Fieldset, Legend, Label
- Placeholder, Required, Autocomplete
- Select vs Datalist
- Input Types (`text`, `email`, `range`, etc.)
- Pattern Attribute
- Progress and Meter Tags
- Global Attributes (`id`, `class`, `style`, etc.)
- `data-*` and `hidden`
- `disabled` vs `readonly`
- Grouping Radio Buttons
- Enctype Attribute
- `<mark>`, `<abbr>`, `<address>`, `<time>`
- `<pre>` vs `<code>`
- Void Elements
- Character Encoding
- Favicon
- Tabindex and Contenteditable
- Display Types (Block vs Inline)
- Default Display Types of Elements
- Opening Link in New Tab
- HTML Comments

---

## ✅ 31. What is the difference between `<ol>`, `<ul>`, and `<dl>`?

**Answer:**

* `<ol>` → Ordered List (1, 2, 3)
* `<ul>` → Unordered List (•, ○)
* `<dl>` → Description List (term-definition)

Each is used to show lists in different ways.

👉 Example:

```html
<ol><li>First</li><li>Second</li></ol>
<ul><li>Item</li></ul>
<dl><dt>HTML</dt><dd>Markup Language</dd></dl>
```

---

## ✅ 32. How to change list numbering style in `<ol>`?

**Answer:**
Use the `type` attribute:

* `type="A"` → A, B, C
* `type="a"` → a, b, c
* `type="I"` → I, II, III
* `type="i"` → i, ii, iii

👉 Example:

```html
<ol type="A">
  <li>HTML</li>
  <li>CSS</li>
</ol>
```

---

## ✅ 33. Can we create nested lists in HTML?

**Answer:**
Yes. You can place one list inside another.
Useful for sub-topics.

👉 Example:

```html
<ul>
  <li>Fruits
    <ul>
      <li>Apple</li>
      <li>Mango</li>
    </ul>
  </li>
</ul>
```

---

## ✅ 34. What are the basic tags for creating a table?

**Answer:**

* `<table>` → start of table
* `<tr>` → table row
* `<td>` → table data (cell)
* `<th>` → table heading (bold + centered)

👉 Example:

```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Avi</td>
    <td>25</td>
  </tr>
</table>
```

---

## ✅ 35. What is the purpose of `<thead>`, `<tbody>`, and `<tfoot>`?

**Answer:**
They help to divide a table into:

* `<thead>` – table header section
* `<tbody>` – main data rows
* `<tfoot>` – footer of table

👉 This improves accessibility and readability.

---

## ✅ 36. What is `colspan` and `rowspan` in table cells?

**Answer:**
Used to merge cells:

* `colspan` → merge columns (side-by-side)
* `rowspan` → merge rows (top to bottom)

👉 Example:

```html
<td colspan="2">Merged Cell</td>
<td rowspan="2">2 rows merged</td>
```

---

## ✅ 37. What is the difference between `<th>` and `<td>`?

**Answer:**

* `<th>` = table heading → bold, centered text
* `<td>` = table data → normal text

Both are used inside `<tr>` (table row).

---

## ✅ 38. How to create a responsive table?

**Answer:**
Wrap table in a scrollable container:

```html
<div style="overflow-x:auto;">
  <table>
    ...
  </table>
</div>
```

Or use CSS `@media` rules to hide/show columns on smaller screens.

---

## ✅ 39. What are meta tags and why are they important?

**Answer:**
Meta tags give info **about the webpage**. They are written inside `<head>`.

Used for:

* SEO (search engines)
* Page description
* Charset, author info

👉 Example:

```html
<meta charset="UTF-8">
<meta name="description" content="HTML Guide">
```

---

## ✅ 40. What is the viewport meta tag and why should we use it?

**Answer:**
It helps in **responsive design**. Makes the website adjust to screen size.

👉 Required for mobile-friendly sites.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Without this, websites look zoomed-out or broken on mobile devices.

---

## ✅ 41. What is the purpose of the `<link>` tag in HTML?

**Answer:**
The `<link>` tag is used in the `<head>` to connect external resources.
Mostly used for **CSS** stylesheets.

👉 Example:

```html
<link rel="stylesheet" href="styles.css">
```
rel means it describe the type of relationship.

---

## ✅ 42. How to connect internal CSS and external CSS in HTML?

**Answer:**

* Internal CSS: write in `<style>` inside `<head>`
* External CSS: use `<link>` tag with CSS file path

👉 Internal:

```html
<style>
p { color: blue; }
</style>
```

👉 External:

```html
<link rel="stylesheet" href="style.css">
```

---

## ✅ 43. What is the `<style>` tag used for?

**Answer:**
It is used to write **internal CSS** in HTML. You can define styles directly in the page.

👉 Example:

```html
<style>
h1 { color: red; }
</style>
```

---

## ✅ 44. What is the purpose of the `<script>` tag?

**Answer:**
Used to write or load **JavaScript** code inside HTML.

👉 Example:

```html
<script>
  alert("Hello from JS");
</script>
```

You can also use `src` to link external `.js` file.

---

## ✅ 45. Difference between `<style>` and `<script>`?

**Answer:**

* `<style>` → used for CSS (styling)
* `<script>` → used for JavaScript (logic/interaction)

Both are placed in `<head>` or `<body>`.

---

## ✅ 46. How to include an external JavaScript file?

**Answer:**
Use `<script>` tag with `src` attribute:

```html
<script src="main.js"></script>
```

Best to place it before closing `</body>` tag for faster loading.

---

## ✅ 47. What is the difference between inline, internal, and external CSS?

**Answer:**

* **Inline**: inside the tag using `style` attribute
* **Internal**: inside `<style>` in HTML head
* **External**: separate `.css` file linked by `<link>`

👉 Inline Example:

```html
<p style="color:red">Hi</p>
```

---

## ✅ 48. What are block and inline elements?

**Answer:**

* **Block**: takes full width (starts on new line)
  → Example: `<div>`, `<p>`, `<h1>`
* **Inline**: takes only needed space
  → Example: `<span>`, `<a>`, `<strong>`

---

## ✅ 49. How to convert block to inline and vice versa?

**Answer:**
Use CSS `display` property:

```css
div { display: inline; }
span { display: block; }
```

This changes how the element behaves.

---

## ✅ 50. What is HTML5 and how is it different from HTML4?

**Answer:**
HTML5 is the **latest version** of HTML. Key differences:

* New semantic tags: `<header>`, `<footer>`, `<nav>`, etc.
* Native support for audio, video, canvas
* Cleaner and simpler code
* Mobile & responsive friendly

👉 You write `<!DOCTYPE html>` at the top for HTML5.

---

## ✅ 51. What are semantic elements in HTML5?

**Answer:**
Semantic elements have clear meaning and describe their purpose.
Examples:

* `<header>`: top part
* `<footer>`: bottom info
* `<article>`: independent content
* `<section>`: logical block

They help screen readers, SEO, and code readability.

---

## ✅ 52. Difference between `<div>` and semantic tags?

**Answer:**

* `<div>` is a non-semantic container (no meaning).
* Semantic tags like `<header>`, `<nav>` tell what content they hold.

Semantic tags are better for structure, SEO, and accessibility.

---

## ✅ 53. What is the use of the `<nav>` tag?

**Answer:**
`<nav>` defines navigation links like menus or tables of contents.

👉 Example:

```html
<nav>
  <a href="/home">Home</a>
  <a href="/about">About</a>
</nav>
```

---

## ✅ 54. What is the purpose of the `<main>` tag?

**Answer:**
It wraps the **main content** of a webpage (excluding header, footer, nav).
Only one `<main>` tag should be used per page.

---

## ✅ 55. What is the use of the `<section>` tag?

**Answer:**
`<section>` is used to group related content.
Useful when content has its own heading.

👉 Example:

```html
<section>
  <h2>About Us</h2>
  <p>We are a tech company...</p>
</section>
```

---

## ✅ 56. Difference between `<section>` and `<div>`?

**Answer:**

* `<section>` is semantic → used for grouped, related content with headings
* `<div>` is generic container → used for layout or styling

Use `<section>` when content has a specific meaning.

---

## ✅ 57. What is the use of `<article>` tag?

**Answer:**
Use `<article>` for **self-contained content** like blog posts, news, etc.
It should make sense even if taken out of the page.

---

## ✅ 58. How to create a form in HTML?

**Answer:**
Use `<form>` with input elements:

```html
<form action="/submit" method="post">
  <input type="text" name="username">
  <input type="submit">
</form>
```

---

## ✅ 59. What is the difference between GET and POST method?

**Answer:**

* **GET** → data in URL, less secure, used for reading
* **POST** → data in body, more secure, used for submitting forms

---

## ✅ 60. What is the use of `action` and `method` in forms?

**Answer:**

* `action`: URL where form data will be sent
* `method`: type of HTTP request (`get` or `post`)

👉 Example:

```html
<form action="/login" method="post">
  ...
</form>
```

---

## ✅ 61. What is the use of the `<label>` tag in forms?

**Answer:**
`<label>` gives a name to an input field and improves accessibility. When you click the label, the input field is focused.

👉 Example:

```html
<label for="email">Email:</label>
<input type="email" id="email">
```

---

## ✅ 62. Difference between `id` and `name` in input fields?

**Answer:**

* `id`: used by JavaScript or label (must be unique)
* `name`: used to send form data to server (not required to be unique)

---

## ✅ 63. What is the purpose of `placeholder` in input fields?

**Answer:**
It shows **hint text** inside the input box to tell users what to type.

👉 Example:

```html
<input type="text" placeholder="Enter your name">
```

---

## ✅ 64. What is the use of the `required` attribute in forms?

**Answer:**
It makes the input field **mandatory**. The form won’t submit unless the field is filled.

👉 Example:

```html
<input type="email" required>
```

---

## ✅ 65. What is the use of `autocomplete` in forms?

**Answer:**
`autocomplete` helps the browser **remember and auto-fill** past values.

* `on`: allow autofill
* `off`: stop autofill

👉 Example:

```html
<form autocomplete="off">
  ...
</form>
```

---

## ✅ 66. What is the use of `<fieldset>` and `<legend>`?

**Answer:**
Used to group related form fields.

* `<fieldset>`: groups the fields with a box
* `<legend>`: adds a title to the box

👉 Example:

```html
<fieldset>
  <legend>Contact Info</legend>
  <input type="text">
</fieldset>
```

---

## ✅ 67. How to create a dropdown in HTML?

**Answer:**
Use `<select>` and `<option>`:

```html
<select>
  <option>India</option>
  <option>USA</option>
</select>
```

---

## ✅ 68. What is the difference between `<select>` and `<datalist>`?

**Answer:**

* `<select>` shows a dropdown with fixed choices
* `<datalist>` allows **free typing + suggestions**

👉 Example with `<datalist>`:

```html
<input list="browsers">
<datalist id="browsers">
  <option value="Chrome">
  <option value="Firefox">
</datalist>
```

---

## ✅ 69. What is the purpose of `<progress>` and `<meter>` tags?

**Answer:**

* `<progress>`: shows task progress (like file upload)
* `<meter>`: shows a value in a range (like battery level)

👉 Example:

```html
<progress value="30" max="100"></progress>
<meter value="0.6">60%</meter>
```

---

## ✅ 70. What are global attributes in HTML?

**Answer:**
These are attributes that **can be used in any HTML tag**.
Examples:

* `id`
* `class`
* `style`
* `title`
* `hidden`
* `data-*`

👉 Example:

```html
<p id="para1" class="info">Hello</p>
```
---

## ✅ 71. What is the use of the `data-*` attribute?

**Answer:**
`data-*` is used to store custom data in any HTML tag. JavaScript can later access or change it.

👉 Example:

```html
<div data-user="Avinash">Hello</div>
```

You can access it in JS: `element.dataset.user`

---

## ✅ 72. What is the use of the `hidden` attribute?

**Answer:**
It hides the element from the page. But it still exists in the HTML DOM and can be shown later using JavaScript.

👉 Example:

```html
<p hidden>This is hidden</p>
```

---

## ✅ 73. What is the difference between `disabled` and `readonly`?

**Answer:**

* `disabled`: user cannot edit or click, and it’s not sent with form
* `readonly`: user cannot edit, but value is sent with form

👉 Example:

```html
<input disabled>
<input readonly>
```

---

## ✅ 74. How to group radio buttons in HTML?

**Answer:**
Give same `name` to all radio inputs so only one can be selected.

👉 Example:

```html
<input type="radio" name="gender" value="male"> Male
<input type="radio" name="gender" value="female"> Female
```

---

## ✅ 75. What is the default method for a form?

**Answer:**
If not written, the default method is `GET`, which sends data in URL.
Use `POST` for sensitive data.

---

## ✅ 76. What is the purpose of `enctype` in a form?

**Answer:**
It defines how the form data is encoded. Required when you upload files.

👉 Common values:

* `application/x-www-form-urlencoded` (default)
* `multipart/form-data` → required for file upload

---

## ✅ 77. What are input types available in HTML5?

**Answer:**
Some important ones:

* `text`, `password`, `email`, `number`
* `checkbox`, `radio`
* `date`, `time`, `color`, `range`
* `file`, `search`, `url`, `tel`

---

## ✅ 78. What is the use of the `pattern` attribute in input fields?

**Answer:**
Used for validation using regular expressions.

👉 Example:

```html
<input type="text" pattern="[A-Za-z]{3}">
```

Only allows exactly 3 letters.

---

## ✅ 79. What is the purpose of the `<noscript>` tag?

**Answer:**
This tag shows message when JavaScript is disabled in the browser.

👉 Example:

```html
<noscript>Please enable JavaScript for full features.</noscript>
```

---

## ✅ 80. How does HTML handle whitespace and line breaks?

**Answer:**
HTML **ignores extra spaces, tabs, or line breaks** by default. Use:

* `&nbsp;` for space
* `<br>` for line break
* `<pre>` tag to preserve formatting

👉 Example:

```html
<p>This&nbsp;&nbsp;has&nbsp;space</p>
<pre>Exact    spacing</pre>
```

---

## ✅ 81. What is the use of the `title` attribute?

**Answer:**
The `title` attribute shows a small tooltip when you hover the mouse.

👉 Example:

```html
<p title="Hello Tip">Hover me</p>
```

---

## ✅ 82. What is the difference between `id` and `class`?

**Answer:**

* `id`: unique name for one element
* `class`: can be shared by many elements

👉 Example:

```html
<p id="main"></p>
<p class="info"></p>
```

---

## ✅ 83. What is the use of `lang` attribute in HTML?

**Answer:**
`lang` tells the browser the language of the content. Helps screen readers and SEO.

👉 Example:

```html
<html lang="en">
```

---

## ✅ 84. What is the difference between `<strong>` and `<b>`?

**Answer:**

* `<strong>`: bold with meaning (important)
* `<b>`: just bold, no meaning

Use `<strong>` for accessibility and semantics.

---

## ✅ 85. Difference between `<em>` and `<i>`?

**Answer:**

* `<em>`: italic + semantic (emphasis)
* `<i>`: only visual italic, no meaning

Prefer `<em>` when emphasis is important.

---

## ✅ 86. What is the use of `<mark>` tag?

**Answer:**
It highlights the text with yellow by default.

👉 Example:

```html
<p>This is <mark>important</mark></p>
```

---

## ✅ 87. What is the purpose of `<abbr>` tag?

**Answer:**
Used to define abbreviation. Shows full form on hover.

👉 Example:

```html
<abbr title="HyperText Markup Language">HTML</abbr>
```

---

## ✅ 88. Use of `<time>` and `<address>` tags?

**Answer:**

* `<time>`: shows date or time with machine-readable format
* `<address>`: shows contact info (usually in footer)

👉 Example:

```html
<time datetime="2025-07-15">15 July 2025</time>
<address>abc@example.com</address>
```

---

## ✅ 89. What is the difference between `<script defer>` and `<script async>`?

**Answer:**

* `defer`: waits for HTML to load, then runs in order
* `async`: runs as soon as it’s downloaded (may break order)

👉 Use `defer` for safe, ordered loading.

---

## ✅ 90. What are accessibility features in HTML?

**Answer:**
Features that help disabled users:

* `alt` for images
* Semantic tags (`<header>`, `<main>`, etc.)
* `aria-*` attributes for screen readers
* `label` for inputs

Helps screen readers, voice tools, and improves usability.

---

## ✅ 91. What is the difference between `<base>` and `<link>` tag?

**Answer:**

* `<base>`: sets base URL for all relative links
* `<link>`: connects external resources (like CSS)

👉 Example:

```html
<base href="https://example.com/">
<link rel="stylesheet" href="style.css">
```

---

## ✅ 92. What is the difference between `<meta>` and `<title>` tag?

**Answer:**

* `<meta>`: gives info about page (SEO, charset, etc.)
* `<title>`: sets tab name (shown in browser tab)

👉 Example:

```html
<meta charset="UTF-8">
<title>My Webpage</title>
```

---

## ✅ 93. What is the use of `<pre>` tag?

**Answer:**
Shows text exactly as written — with spaces and line breaks. Like in code blocks.

👉 Example:

```html
<pre>
  Line 1
    Line 2
</pre>
```

---

## ✅ 94. What is the use of `<code>` tag?

**Answer:**
Used to display small inline code.

👉 Example:

```html
<p>Use <code>console.log()</code> to print in JS.</p>
```

---

## ✅ 95. What is the difference between `<pre>` and `<code>`?

**Answer:**

* `<pre>`: block of preformatted text (preserves spacing)
* `<code>`: used for showing code inline

Often used together: `<pre><code>...</code></pre>`

---

## ✅ 96. What are void elements in HTML?

**Answer:**
Tags that do not have closing tags.
Examples: `<br>`, `<hr>`, `<img>`, `<input>`, `<meta>`, `<link>`

They are self-contained.

---

## ✅ 97. What is character encoding and why is it important?

**Answer:**
Character encoding (like UTF-8) tells browser how to read text symbols.
Without it, text may look broken.

👉 Use:

```html
<meta charset="UTF-8">
```

---

## ✅ 98. What is a favicon and how to add it?

**Answer:**
A small icon shown in the browser tab.

👉 Add using:

```html
<link rel="icon" href="favicon.ico">
```

---

## ✅ 99. What is the default character set of HTML5?

**Answer:**
UTF-8 is the default character set in HTML5. It supports most languages and symbols.

👉 Set using:

```html
<meta charset="UTF-8">
```

---

## ✅ 100. What is the role of `tabindex` attribute?

**Answer:**
It controls keyboard navigation order.

* `tabindex="0"` → normal
* `tabindex="-1"` → not focusable by tab
* `tabindex="1"` → comes first

👉 Example:

```html
<button tabindex="1">First</button>
```

---

## ✅ 101. What is `contenteditable` attribute?

**Answer:**
Makes any element editable in browser like a textbox.

👉 Example:

```html
<p contenteditable="true">You can edit this</p>
```

---

## ✅ 102. What is the difference between inline and block-level elements?

**Answer:**

* **Block**: starts on new line, takes full width (e.g., `<div>`, `<p>`, `<section>`)
* **Inline**: stays in line, only takes needed space (e.g., `<span>`, `<a>`, `<strong>`)

---

## ✅ 103. What is the default display type of `<a>`, `<span>`, `<div>`?

**Answer:**

* `<a>` → inline
* `<span>` → inline
* `<div>` → block

---

## ✅ 104. How to open a link in new tab using HTML?

**Answer:**
Use `target="_blank"` in anchor tag.

👉 Example:

```html
<a href="https://google.com" target="_blank">Open Google</a>
```

---

## ✅ 105. How to comment in HTML?

**Answer:**
Use:

```html
<!-- This is a comment -->
```

Comments are not shown on the webpage.

---
