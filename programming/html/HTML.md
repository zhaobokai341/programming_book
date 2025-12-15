# HTML Cheat Sheet: Elements (Tags), Attributes (Label & Value), and Functions

This document summarizes **HTML elements (tags)**, their **common attributes (label = attribute name, value = attribute value)**, and their **functions (what they do)**.

---

## 1. Document Structure

| Element           | Function                 | Common Attributes (label="value")                                                    |
| ----------------- | ------------------------ | ------------------------------------------------------------------------------------ |
| `<!DOCTYPE html>` | Declares HTML5 document  | —                                                                                    |
| `<html>`          | Root element             | `lang="en"`                                                                          |
| `<head>`          | Metadata container       | —                                                                                    |
| `<title>`         | Page title (browser tab) | —                                                                                    |
| `<meta>`          | Metadata                 | `charset="UTF-8"`, `name="viewport" content="width=device-width, initial-scale=1.0"` |
| `<link>`          | External resource        | `rel="stylesheet"`, `href="style.css"`                                               |
| `<style>`         | Internal CSS             | `type="text/css"`                                                                    |
| `<script>`        | JavaScript               | `src="app.js"`, `defer`, `async`                                                     |
| `<body>`          | Visible content          | —                                                                                    |

---

## 2. Text & Content

| Element        | Function                 | Common Attributes |
| -------------- | ------------------------ | ----------------- |
| `<h1>`–`<h6>`  | Headings                 | `class`, `id`     |
| `<p>`          | Paragraph                | `class`, `id`     |
| `<br>`         | Line break               | —                 |
| `<hr>`         | Horizontal rule          | —                 |
| `<strong>`     | Strong importance (bold) | —                 |
| `<em>`         | Emphasis (italic)        | —                 |
| `<span>`       | Inline container         | `class`, `style`  |
| `<div>`        | Block container          | `class`, `id`     |
| `<pre>`        | Preformatted text        | —                 |
| `<code>`       | Code text                | —                 |
| `<blockquote>` | Quotation block          | `cite="url"`      |

---

## 3. Links & Media

| Element    | Function      | Common Attributes                                |
| ---------- | ------------- | ------------------------------------------------ |
| `<a>`      | Hyperlink     | `href="url"`, `target="_blank"`                  |
| `<img>`    | Image         | `src="img.png"`, `alt="text"`, `width`, `height` |
| `<audio>`  | Audio player  | `src`, `controls`, `autoplay`, `loop`            |
| `<video>`  | Video player  | `src`, `controls`, `width`, `height`             |
| `<source>` | Media source  | `src`, `type`                                    |
| `<iframe>` | Embedded page | `src`, `width`, `height`                         |

---

## 4. Lists

| Element | Function         | Common Attributes       |
| ------- | ---------------- | ----------------------- |
| `<ul>`  | Unordered list   | —                       |
| `<ol>`  | Ordered list     | `type="1"`, `start="3"` |
| `<li>`  | List item        | —                       |
| `<dl>`  | Description list | —                       |
| `<dt>`  | Term             | —                       |
| `<dd>`  | Description      | —                       |

---

## 5. Tables

| Element     | Function           | Common Attributes    |
| ----------- | ------------------ | -------------------- |
| `<table>`   | Table container    | `border`, `class`    |
| `<caption>` | Table title        | —                    |
| `<tr>`      | Table row          | —                    |
| `<th>`      | Header cell        | `scope="col"`        |
| `<td>`      | Data cell          | `colspan`, `rowspan` |
| `<thead>`   | Table header group | —                    |
| `<tbody>`   | Table body group   | —                    |
| `<tfoot>`   | Table footer group | —                    |

---

## 6. Forms & Input

| Element      | Function           | Common Attributes                                  |
| ------------ | ------------------ | -------------------------------------------------- |
| `<form>`     | Form container     | `action="url"`, `method="post"`                    |
| `<label>`    | Input label        | `for="id"`                                         |
| `<input>`    | User input         | `type`, `name`, `value`, `placeholder`, `required` |
| `<textarea>` | Multi-line input   | `rows`, `cols`, `placeholder`                      |
| `<button>`   | Button             | `type="submit"`                                    |
| `<select>`   | Dropdown           | `name`, `multiple`                                 |
| `<option>`   | Dropdown option    | `value`, `selected`                                |
| `<fieldset>` | Group inputs       | —                                                  |
| `<legend>`   | Fieldset title     | —                                                  |
| `<datalist>` | Input suggestions  | `id`                                               |
| `<output>`   | Calculation result | `for`, `name`                                      |

### Common `<input type>` values

`text`, `password`, `email`, `number`, `checkbox`, `radio`, `file`, `date`, `time`, `range`, `color`, `submit`, `reset`, `hidden`

---

## 7. Semantic HTML

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

## 8. Interactive & Misc

| Element      | Function             | Common Attributes |
| ------------ | -------------------- | ----------------- |
| `<details>`  | Collapsible section  | `open`            |
| `<summary>`  | Details heading      | —                 |
| `<dialog>`   | Dialog/modal         | `open`            |
| `<template>` | Hidden HTML template | —                 |
| `<canvas>`   | Drawing area         | `width`, `height` |
| `<svg>`      | Vector graphics      | `width`, `height` |

---

## 9. Global Attributes (Apply to Almost All Elements)

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

---

## 10. Event Attributes (HTML Functions via JavaScript)

| Attribute     | Function              |
| ------------- | --------------------- |
| `onclick`     | Mouse click           |
| `ondblclick`  | Double click          |
| `oninput`     | Input change          |
| `onchange`    | Value change          |
| `onsubmit`    | Form submit           |
| `onload`      | Page or resource load |
| `onmouseover` | Mouse over            |
| `onkeydown`   | Key press             |

Example:

```html
<button onclick="alert('Hello')">Click</button>
```

---

## 11. ARIA (Accessibility)

| Attribute       | Function                | Example                 |
| --------------- | ----------------------- | ----------------------- |
| `role`          | Element role            | `role="button"`         |
| `aria-label`    | Screen reader label     | `aria-label="Close"`    |
| `aria-hidden`   | Hide from screen reader | `aria-hidden="true"`    |
| `aria-expanded` | Toggle state            | `aria-expanded="false"` |

