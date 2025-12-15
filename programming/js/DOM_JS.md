# JavaScript DOM – Complete Cheat Sheet (All DOM APIs)

This document covers **JavaScript DOM (Document Object Model)** only: **selection, traversal, manipulation, events, attributes, styles**, and **return values**.

---

## 1. Document Object

| API                        | Function         | Returns           |
| -------------------------- | ---------------- | ----------------- |
| `document`                 | Root DOM object  | `Document`        |
| `document.documentElement` | `<html>` element | `HTMLElement`     |
| `document.body`            | `<body>`         | `HTMLBodyElement` |
| `document.head`            | `<head>`         | `HTMLHeadElement` |

---

## 2. Element Selection

| Method                         | Function     | Returns           |
| ------------------------------ | ------------ | ----------------- |
| `getElementById(id)`           | Select by ID | `Element \| null` |
| `getElementsByClassName(name)` | By class     | `HTMLCollection`  |
| `getElementsByTagName(tag)`    | By tag       | `HTMLCollection`  |
| `querySelector(css)`           | First match  | `Element \| null` |
| `querySelectorAll(css)`        | All matches  | `NodeList`        |

---

## 3. Traversing the DOM

| Property                 | Function         | Returns           |
| ------------------------ | ---------------- | ----------------- |
| `parentNode`             | Parent node      | `Node`            |
| `parentElement`          | Parent element   | `Element \| null` |
| `children`               | Child elements   | `HTMLCollection`  |
| `childNodes`             | All child nodes  | `NodeList`        |
| `firstChild`             | First node       | `Node`            |
| `firstElementChild`      | First element    | `Element`         |
| `lastChild`              | Last node        | `Node`            |
| `nextSibling`            | Next node        | `Node`            |
| `nextElementSibling`     | Next element     | `Element`         |
| `previousSibling`        | Previous node    | `Node`            |
| `previousElementSibling` | Previous element | `Element`         |

---

## 4. Creating & Removing Nodes

| Method                          | Function       | Returns       |
| ------------------------------- | -------------- | ------------- |
| `document.createElement(tag)`   | Create element | `HTMLElement` |
| `document.createTextNode(text)` | Create text    | `Text`        |
| `appendChild(node)`             | Append child   | `Node`        |
| `append(...nodes)`              | Append nodes   | `undefined`   |
| `prepend(...nodes)`             | Prepend nodes  | `undefined`   |
| `insertBefore(new, ref)`        | Insert before  | `Node`        |
| `removeChild(node)`             | Remove child   | `Node`        |
| `remove()`                      | Remove element | `undefined`   |
| `cloneNode(deep)`               | Clone node     | `Node`        |

---

## 5. Content Manipulation

| Property      | Function       | Returns  |
| ------------- | -------------- | -------- |
| `innerHTML`   | HTML content   | `string` |
| `outerHTML`   | Element + HTML | `string` |
| `textContent` | Text only      | `string` |
| `innerText`   | Visible text   | `string` |

---

## 6. Attributes

| Method / Property           | Function         | Returns          |
| --------------------------- | ---------------- | ---------------- |
| `getAttribute(name)`        | Get attribute    | `string \| null` |
| `setAttribute(name, value)` | Set attribute    | `undefined`      |
| `removeAttribute(name)`     | Remove attribute | `undefined`      |
| `hasAttribute(name)`        | Attribute exists | `boolean`        |
| `attributes`                | Attribute list   | `NamedNodeMap`   |

---

## 7. Classes (`classList`)

| Method                 | Function      | Returns     |
| ---------------------- | ------------- | ----------- |
| `classList.add()`      | Add class     | `undefined` |
| `classList.remove()`   | Remove class  | `undefined` |
| `classList.toggle()`   | Toggle class  | `boolean`   |
| `classList.contains()` | Check class   | `boolean`   |
| `classList.replace()`  | Replace class | `boolean`   |

---

## 8. Styles

| API                    | Function          | Returns               |
| ---------------------- | ----------------- | --------------------- |
| `style.property`       | Inline style      | `string`              |
| `style.cssText`        | All inline styles | `string`              |
| `getComputedStyle(el)` | Final styles      | `CSSStyleDeclaration` |

---

## 9. Events

### Event Registration

| Method                          | Function        | Returns     |
| ------------------------------- | --------------- | ----------- |
| `addEventListener(type, fn)`    | Add listener    | `undefined` |
| `removeEventListener(type, fn)` | Remove listener | `undefined` |

### Common Events

| Event              | Trigger      |
| ------------------ | ------------ |
| `click`            | Mouse click  |
| `dblclick`         | Double click |
| `input`            | Input change |
| `change`           | Value commit |
| `submit`           | Form submit  |
| `keydown`          | Key down     |
| `keyup`            | Key up       |
| `load`             | Loaded       |
| `DOMContentLoaded` | DOM ready    |

---

## 10. Event Object

| Property / Method         | Function       | Returns     |
| ------------------------- | -------------- | ----------- |
| `event.target`            | Source element | `Element`   |
| `event.currentTarget`     | Bound element  | `Element`   |
| `event.type`              | Event name     | `string`    |
| `event.preventDefault()`  | Stop default   | `undefined` |
| `event.stopPropagation()` | Stop bubbling  | `undefined` |

---

## 11. Forms & Inputs

| API              | Function       | Returns     |
| ---------------- | -------------- | ----------- |
| `form.submit()`  | Submit form    | `undefined` |
| `form.reset()`   | Reset form     | `undefined` |
| `input.value`    | Input value    | `string`    |
| `input.checked`  | Checkbox state | `boolean`   |
| `input.disabled` | Disabled state | `boolean`   |

---

## 12. DOM Geometry

| API                       | Function        | Returns   |
| ------------------------- | --------------- | --------- |
| `getBoundingClientRect()` | Size & position | `DOMRect` |
| `offsetWidth`             | Layout width    | `number`  |
| `offsetHeight`            | Layout height   | `number`  |
| `clientWidth`             | Inner width     | `number`  |
| `scrollHeight`            | Scroll height   | `number`  |
| `scrollTop`               | Scroll Y        | `number`  |

---

## 13. Scrolling

| API                        | Function          | Returns     |
| -------------------------- | ----------------- | ----------- |
| `scrollTo(x,y)`            | Scroll page       | `undefined` |
| `scrollBy(x,y)`            | Scroll relative   | `undefined` |
| `element.scrollIntoView()` | Scroll to element | `undefined` |

---

## 14. Node Info

| Property    | Function     | Returns          |
| ----------- | ------------ | ---------------- |
| `nodeType`  | Node type ID | `number`         |
| `nodeName`  | Node name    | `string`         |
| `nodeValue` | Node value   | `string \| null` |

---

## 15. Dataset (`data-*`)

| API               | Function        | Returns        |
| ----------------- | --------------- | -------------- |
| `element.dataset` | Data attributes | `DOMStringMap` |
| `dataset.key`     | Read value      | `string`       |

---

## 16. Focus & Selection

| API                      | Function        | Returns     |
| ------------------------ | --------------- | ----------- |
| `focus()`                | Focus element   | `undefined` |
| `blur()`                 | Remove focus    | `undefined` |
| `document.activeElement` | Focused element | `Element`   |

---

## 17. Mutation Observer

| API                          | Function        | Returns            |
| ---------------------------- | --------------- | ------------------ |
| `new MutationObserver(fn)`   | Observe DOM     | `MutationObserver` |
| `observer.observe(el, opts)` | Start observing | `undefined`        |
| `observer.disconnect()`      | Stop observing  | `undefined`        |

---

## 18. Element Visibility

| API                    | Function            | Returns                |
| ---------------------- | ------------------- | ---------------------- |
| `element.hidden`       | Hide element        | `boolean`              |
| `IntersectionObserver` | Visibility observer | `IntersectionObserver` |

---

**This document contains ALL commonly used DOM APIs.**
