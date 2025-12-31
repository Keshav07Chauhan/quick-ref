# HTML Cheat Sheet (HTML5)

HTML is the structure for a web app.

---

## 1. Document Structure

| Element | Purpose |
|-------|--------|
| `<!DOCTYPE html>` | Tells the browser to use HTML5 standards mode |
| `<html>` | Root element wrapping the entire document |
| `<head>` | Holds metadata and resources not shown on the page |
| `<body>` | Contains all visible page content |

---

## 2. Metadata (`<head>`)

| Element | Purpose |
|-------|--------|
| `<title>` | Sets the browser tab title and SEO title |
| `<meta>` | Provides metadata like charset, viewport, description |
| `<link>` | Links external resources (CSS, icons) |
| `<style>` | Embeds CSS directly into the document |
| `<base>` | Defines a base URL for all relative links |

---

## 3. Sectioning & Semantic Layout

| Element | Purpose |
|-------|--------|
| `<header>` | Introductory content for a page or section |
| `<nav>` | Contains primary navigation links |
| `<main>` | Holds the main unique content of the page |
| `<section>` | Groups related content by theme |
| `<article>` | Self-contained content that can stand alone |
| `<aside>` | Tangential or sidebar content |
| `<footer>` | Closing content for a page or section |

---

## 4. Headings

| Element | Purpose |
|-------|--------|
| `<h1>` | Top-level page heading (only one per page) |
| `<h2>` | Major section heading |
| `<h3>`–`<h6>` | Sub-section headings in decreasing importance |

---

## 5. Text Content

| Element | Purpose |
|-------|--------|
| `<p>` | Represents a paragraph of text |
| `<br>` | Forces a line break (use sparingly) |
| `<hr>` | Indicates a thematic content break |
| `<blockquote>` | Quotes a block of external content |
| `<pre>` | Preserves whitespace and formatting |
| `<address>` | Contact or author information |

---

## 6. Inline Text Semantics

| Element | Purpose |
|-------|--------|
| `<strong>` | Marks text as critically important |
| `<em>` | Adds emphasis that changes meaning |
| `<b>` | Bold text with no semantic importance |
| `<i>` | Italic text with no semantic meaning |
| `<mark>` | Highlights text for reference |
| `<small>` | Displays fine print or disclaimers |
| `<sub>` | Subscript text |
| `<sup>` | Superscript text |
| `<abbr>` | Abbreviation with optional expansion |
| `<cite>` | Title of a referenced work |
| `<code>` | Inline code snippet |
| `<kbd>` | User keyboard input |
| `<samp>` | Program output |
| `<var>` | Variable name |
| `<time>` | Machine-readable date or time |
| `<span>` | Generic inline container with no meaning |

---

## 7. Grouping & Containers

| Element | Purpose |
|-------|--------|
| `<div>` | Generic block-level container (last resort) |

---

## 8. Links

| Element | Purpose |
|-------|--------|
| `<a>` | Creates a hyperlink to another resource |

Common attributes:
- `href` → link destination  
- `target` → where to open the link  
- `rel` → relationship/security info  

---

## 9. Lists

| Element | Purpose |
|-------|--------|
| `<ul>` | Unordered (bulleted) list |
| `<ol>` | Ordered (numbered) list |
| `<li>` | List item |
| `<dl>` | Description list |
| `<dt>` | Term being defined |
| `<dd>` | Term description |

---

## 10. Images & Media

| Element | Purpose |
|-------|--------|
| `<img>` | Embeds an image |
| `<audio>` | Embeds audio content |
| `<video>` | Embeds video content |
| `<source>` | Specifies media file source |
| `<track>` | Adds subtitles or captions |
| `<figure>` | Wraps media with context |
| `<figcaption>` | Caption for figure |

---

## 11. Tables

| Element | Purpose |
|-------|--------|
| `<table>` | Table container |
| `<caption>` | Table title |
| `<thead>` | Header row group |
| `<tbody>` | Main data group |
| `<tfoot>` | Footer row group |
| `<tr>` | Table row |
| `<th>` | Header cell |
| `<td>` | Data cell |

---

## 12. Forms

| Element | Purpose |
|-------|--------|
| `<form>` | Collects user input |
| `<label>` | Describes a form control |
| `<input>` | Single-line input field |
| `<textarea>` | Multi-line text input |
| `<select>` | Dropdown menu |
| `<option>` | Selectable item |
| `<button>` | Clickable action button |
| `<fieldset>` | Groups related controls |
| `<legend>` | Title for a fieldset |
| `<datalist>` | Input suggestions |
| `<output>` | Displays calculated result |

---

## 13. Input Types (What They Mean)

| Type | Use |
|----|----|
| `text` | Free-form text |
| `email` | Email address validation |
| `password` | Masked input |
| `number` | Numeric input |
| `checkbox` | Multiple selection |
| `radio` | Single selection |
| `date` | Date picker |
| `file` | File upload |
| `range` | Slider input |
| `submit` | Form submission |

---

## 14. Interactive Elements

| Element | Purpose |
|-------|--------|
| `<details>` | Expandable disclosure widget |
| `<summary>` | Visible label for details |
| `<dialog>` | Modal or popup dialog |

---

## 15. Embedded Content

| Element | Purpose |
|-------|--------|
| `<iframe>` | Embeds another HTML page |
| `<embed>` | Embeds external content |
| `<object>` | Generic embedded resource |
| `<param>` | Parameters for object |

---

## 16. Scripting

| Element | Purpose |
|-------|--------|
| `<script>` | Runs JavaScript |
| `<noscript>` | Fallback when JS is disabled |

---

## 17. Global Attributes (Used Everywhere)

| Attribute | Purpose |
|---------|--------|
| `id` | Unique element identifier |
| `class` | CSS/JS grouping hook |
| `style` | Inline CSS styling |
| `title` | Tooltip text |
| `hidden` | Hides element |
| `tabindex` | Keyboard navigation order |
| `contenteditable` | Makes content editable |
| `draggable` | Enables drag behavior |
| `lang` | Language of content |
| `dir` | Text direction |

---

## 18. Event Attributes

| Attribute | Purpose |
|----------|--------|
| `onclick` | Fires on click |
| `onchange` | Fires on value change |
| `oninput` | Fires on user input |
| `onsubmit` | Fires on form submit |
| `onload` | Fires when loaded |

---

## 19. Deprecated (Do Not Use) ❌

| Element | Reason |
|-------|--------|
| `<font>` | Styling belongs in CSS |
| `<center>` | Obsolete layout control |
| `<marquee>` | Non-standard behavior |
| `<strike>` | Replaced by CSS |

---

## 20. Void Elements (No Closing Tag)

| Element | Purpose |
|-------|--------|
| `<img>` | Image |
| `<br>` | Line break |
| `<hr>` | Section divider |
| `<input>` | Form input |
| `<meta>` | Metadata |
| `<link>` | External resource |

---

## Learn HTML in Depth

This cheat sheet covers the elements and attributes with their purposes in HTML.

To understand HTML properly — including semantics, best practices, accessibility, and standards — refer to the following resources:

- **MDN Web Docs (Official HTML Documentation)**  
  https://developer.mozilla.org/en-US/docs/Web/HTML

- **GeeksforGeeks HTML Cheat Sheet (Quick Reference)**  
  https://www.geeksforgeeks.org/html/html-cheat-sheet/

Use MDN for deep understanding and GeeksforGeeks for quick syntax reference.

---