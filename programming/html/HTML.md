# **Ultimate HTML Cheat Sheet: Elements, Attributes, and Functions**

This cheat sheet summarizes **HTML elements (tags)**, their **common attributes (label="value")**, and their **functions**.

---

## **1. Document Structure**

| Element           | Function                 | Common Attributes (label="value")                                                                                                      |
| ----------------- | ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| `<!DOCTYPE html>` | Declares HTML5 document  | —                                                                                                                                      |
| `<html>`          | Root element             | `lang="en"`, `xmlns="http://www.w3.org/1999/xhtml"`, `dir="ltr"`                                                                       |
| `<head>`          | Metadata container       | —                                                                                                                                      |
| `<title>`         | Page title (browser tab) | —                                                                                                                                      |
| `<meta>`          | Metadata                 | `charset="UTF-8"`, `name="viewport" content="width=device-width, initial-scale=1.0"`, `http-equiv="X-UA-Compatible" content="IE=edge"` |
| `<link>`          | External resource        | `rel="stylesheet"`, `rel="icon"`, `href="style.css"`, `rel="preload"`                                                                  |
| `<style>`         | Internal CSS             | `type="text/css"`                                                                                                                      |
| `<script>`        | JavaScript               | `src="app.js"`, `defer`, `async`, `type="module"`                                                                                      |
| `<body>`          | Visible content          | —                                                                                                                                      |
| `<!-- -->`        | Comment                  | —                                                                                                                                      |

---

## **2. Text & Content**

| Element           | Function                 | Common Attributes    |
| ----------------- | ------------------------ | -------------------- |
| `<h1>`–`<h6>`     | Headings                 | `class`, `id`        |
| `<p>`             | Paragraph                | `class`, `id`, `dir` |
| `<br>`            | Line break               | —                    |
| `<hr>`            | Horizontal rule          | —                    |
| `<strong>`        | Strong importance (bold) | —                    |
| `<b>`             | Bold text (stylistic)    | —                    |
| `<em>`            | Emphasis (italic)        | —                    |
| `<i>`             | Italic text (stylistic)  | —                    |
| `<mark>`          | Highlight text           | —                    |
| `<small>`         | Smaller text             | —                    |
| `<del>`           | Deleted text             | `cite`, `datetime`   |
| `<ins>`           | Inserted text            | `cite`, `datetime`   |
| `<sub>` / `<sup>` | Subscript / Superscript  | —                    |
| `<abbr>`          | Abbreviation             | `title="full term"`  |
| `<cite>`          | Citation                 | —                    |
| `<span>`          | Inline container         | `class`, `style`     |
| `<div>`           | Block container          | `class`, `id`        |
| `<pre>`           | Preformatted text        | —                    |
| `<code>`          | Code text                | —                    |
| `<blockquote>`    | Quotation block          | `cite="url"`         |

---

## **3. Links & Media**

| Element     | Function           | Common Attributes                                                        |
| ----------- | ------------------ | ------------------------------------------------------------------------ |
| `<a>`       | Hyperlink          | `href="url"`, `target="_blank"`, `rel="noopener noreferrer"`             |
| `<img>`     | Image              | `src="img.png"`, `alt="text"`, `width`, `height`                         |
| `<picture>` | Responsive image   | `<source srcset="..." type="...">`, `<img src="..." alt="...">`          |
| `<audio>`   | Audio player       | `src`, `controls`, `autoplay`, `loop`, `muted`                           |
| `<video>`   | Video player       | `src`, `controls`, `width`, `height`, `autoplay`, `muted`, `playsinline` |
| `<source>`  | Media source       | `src`, `type`                                                            |
| `<track>`   | Subtitles/captions | `src`, `kind="subtitles"`, `srclang="en"`, `label="English"`             |
| `<iframe>`  | Embedded page      | `src`, `width`, `height`, `title`                                        |

---

## **4. Lists**

| Element | Function         | Common Attributes                   |
| ------- | ---------------- | ----------------------------------- |
| `<ul>`  | Unordered list   | —                                   |
| `<ol>`  | Ordered list     | `type="1"`, `start="3"`, `reversed` |
| `<li>`  | List item        | `value`                             |
| `<dl>`  | Description list | —                                   |
| `<dt>`  | Term             | —                                   |
| `<dd>`  | Description      | —                                   |

---

## **5. Tables**

| Element                | Function           | Common Attributes            |
| ---------------------- | ------------------ | ---------------------------- |
| `<table>`              | Table container    | `border`, `class`            |
| `<caption>`            | Table title        | —                            |
| `<tr>`                 | Table row          | —                            |
| `<th>`                 | Header cell        | `scope="col"`, `scope="row"` |
| `<td>`                 | Data cell          | `colspan`, `rowspan`         |
| `<thead>`              | Table header group | —                            |
| `<tbody>`              | Table body group   | —                            |
| `<tfoot>`              | Table footer group | —                            |
| `<col>` / `<colgroup>` | Table column/group | `span`, `width`              |

---

## **6. Forms & Input**

| Element      | Function           | Common Attributes                                                                                               |
| ------------ | ------------------ | --------------------------------------------------------------------------------------------------------------- |
| `<form>`     | Form container     | `action="url"`, `method="post"`, `novalidate`                                                                   |
| `<label>`    | Input label        | `for="id"`                                                                                                      |
| `<input>`    | User input         | `type`, `name`, `value`, `placeholder`, `required`, `autocomplete`, `pattern`, `min`, `max`, `step`, `multiple` |
| `<textarea>` | Multi-line input   | `rows`, `cols`, `placeholder`, `maxlength`, `wrap`                                                              |
| `<button>`   | Button             | `type="submit"`, `name`, `value`                                                                                |
| `<select>`   | Dropdown           | `name`, `multiple`                                                                                              |
| `<option>`   | Dropdown option    | `value`, `selected`                                                                                             |
| `<fieldset>` | Group inputs       | —                                                                                                               |
| `<legend>`   | Fieldset title     | —                                                                                                               |
| `<datalist>` | Input suggestions  | `id`                                                                                                            |
| `<output>`   | Calculation result | `for`, `name`                                                                                                   |
| `<meter>`    | Measurement bar    | `value`, `min`, `max`, `low`, `high`, `optimum`                                                                 |
| `<progress>` | Progress bar       | `value`, `max`                                                                                                  |

**Common `<input type>` values:**
`text`, `password`, `email`, `number`, `checkbox`, `radio`, `file`, `date`, `time`, `range`, `color`, `submit`, `reset`, `hidden`

---

## **7. Semantic HTML**

| Element        | Function            | Common Attributes |
| -------------- | ------------------- | ----------------- |
| `<header>`     | Page/section header | —                 |
| `<nav>`        | Navigation          | —                 |
| `<main>`       | Main content        | —                 |
| `<section>`    | Section             | —                 |
| `<article>`    | Independent content | —                 |
| `<aside>`      | Sidebar content     | —                 |
| `<footer>`     | Footer              | —                 |
| `<figure>`     | Media container     | —                 |
| `<figcaption>` | Media caption       | —                 |
| `<address>`    | Contact info        | —                 |

---

## **8. Interactive & Misc**

| Element      | Function             | Common Attributes                |
| ------------ | -------------------- | -------------------------------- |
| `<details>`  | Collapsible section  | `open`                           |
| `<summary>`  | Details heading      | —                                |
| `<dialog>`   | Dialog/modal         | `open`                           |
| `<template>` | Hidden HTML template | —                                |
| `<canvas>`   | Drawing area         | `width`, `height`                |
| `<svg>`      | Vector graphics      | `width`, `height`                |
| `<map>`      | Image map            | `name`                           |
| `<area>`     | Map area             | `shape`, `coords`, `href`, `alt` |

---

## **9. Global Attributes (Apply to Most Elements)**

| Attribute (Label) | Function          | Example Value            |
| ----------------- | ----------------- | ------------------------ |
| `id`              | Unique identifier | `id="main"`              |
| `class`           | CSS class         | `class="container"`      |
| `style`           | Inline CSS        | `style="color:red"`      |
| `title`           | Tooltip text      | `title="info"`           |
| `hidden`          | Hide element      | `hidden`                 |
| `tabindex`        | Keyboard order    | `tabindex="0"`           |
| `contenteditable` | Editable content  | `contenteditable="true"` |
| `draggable`       | Drag support      | `draggable="true"`       |
| `data-*`          | Custom data       | `data-id="123"`          |
| `lang`            | Language code     | `lang="en"`              |
| `spellcheck`      | Spell checking    | `spellcheck="true"`      |
| `translate`       | Allow translation | `translate="no"`         |
| `dir`             | Text direction    | `dir="ltr"`              |

---

## **10. Event Attributes (JavaScript)**

| Attribute     | Function              |
| ------------- | --------------------- |
| `onclick`     | Mouse click           |
| `ondblclick`  | Double click          |
| `onmousedown` | Mouse down            |
| `onmouseup`   | Mouse up              |
| `onmouseover` | Mouse over            |
| `onmouseout`  | Mouse out             |
| `onmousemove` | Mouse move            |
| `onkeydown`   | Key press down        |
| `onkeypress`  | Key press             |
| `onkeyup`     | Key release           |
| `oninput`     | Input value change    |
| `onchange`    | Value change          |
| `onsubmit`    | Form submit           |
| `onfocus`     | Element gains focus   |
| `onblur`      | Element loses focus   |
| `onload`      | Page or resource load |
| `onscroll`    | Scroll event          |
| `onresize`    | Window resize         |

---

## **11. ARIA (Accessibility)**

| Attribute          | Function                          | Example                   |
| ------------------ | --------------------------------- | ------------------------- |
| `role`             | Element role                      | `role="button"`           |
| `aria-label`       | Screen reader label               | `aria-label="Close"`      |
| `aria-hidden`      | Hide from screen reader           | `aria-hidden="true"`      |
| `aria-expanded`    | Toggle state                      | `aria-expanded="false"`   |
| `aria-checked`     | Checkbox/radio state              | `aria-checked="true"`     |
| `aria-selected`    | Selected item                     | `aria-selected="true"`    |
| `aria-labelledby`  | Reference another element by id   | `aria-labelledby="title"` |
| `aria-describedby` | Describe element using another id | `aria-describedby="desc"` |
