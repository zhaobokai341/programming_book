# **Ultimate JavaScript DOM Cheat Sheet**

---

## **1. Document Object**

| API                        | Function         | Returns           |
| -------------------------- | ---------------- | ----------------- |
| `document`                 | Root DOM object  | `Document`        |
| `document.documentElement` | `<html>` element | `HTMLElement`     |
| `document.body`            | `<body>` element | `HTMLBodyElement` |
| `document.head`            | `<head>` element | `HTMLHeadElement` |
| `document.title`           | Page title       | `string`          |
| `document.URL`             | Current URL      | `string`          |
| `document.referrer`        | Referring URL    | `string`          |
| `document.characterSet`    | Document charset | `string`          |

---

## **2. Element Selection**

| Method                         | Function                  | Returns           |
| ------------------------------ | ------------------------- | ----------------- |
| `getElementById(id)`           | Select by ID              | `Element \| null` |
| `getElementsByClassName(name)` | Select by class           | `HTMLCollection`  |
| `getElementsByTagName(tag)`    | Select by tag name        | `HTMLCollection`  |
| `querySelector(css)`           | First match CSS selector  | `Element \| null` |
| `querySelectorAll(css)`        | All matches CSS selector  | `NodeList`        |
| `closest(selector)`            | Nearest ancestor matching | `Element \| null` |
| `matches(selector)`            | Check if element matches  | `boolean`         |

---

## **3. Traversing the DOM**

| Property                 | Function           | Returns           |
| ------------------------ | ------------------ | ----------------- |
| `parentNode`             | Parent node        | `Node`            |
| `parentElement`          | Parent element     | `Element \| null` |
| `children`               | Child elements     | `HTMLCollection`  |
| `childNodes`             | All child nodes    | `NodeList`        |
| `firstChild`             | First node         | `Node`            |
| `firstElementChild`      | First element      | `Element`         |
| `lastChild`              | Last node          | `Node`            |
| `lastElementChild`       | Last element       | `Element`         |
| `nextSibling`            | Next node          | `Node`            |
| `nextElementSibling`     | Next element       | `Element`         |
| `previousSibling`        | Previous node      | `Node`            |
| `previousElementSibling` | Previous element   | `Element`         |
| `childElementCount`      | Number of children | `number`          |
| `hasChildNodes()`        | Any children?      | `boolean`         |

---

## **4. Creating & Removing Nodes**

| Method                              | Function                | Returns            |
| ----------------------------------- | ----------------------- | ------------------ |
| `document.createElement(tag)`       | Create element          | `HTMLElement`      |
| `document.createTextNode(text)`     | Create text node        | `Text`             |
| `document.createDocumentFragment()` | Lightweight container   | `DocumentFragment` |
| `appendChild(node)`                 | Append child            | `Node`             |
| `append(...nodes)`                  | Append multiple nodes   | `undefined`        |
| `prepend(...nodes)`                 | Prepend multiple nodes  | `undefined`        |
| `insertBefore(newNode, refNode)`    | Insert before reference | `Node`             |
| `replaceChild(newNode, oldNode)`    | Replace child node      | `Node`             |
| `removeChild(node)`                 | Remove child            | `Node`             |
| `remove()`                          | Remove element          | `undefined`        |
| `cloneNode(deep)`                   | Clone element           | `Node`             |

---

## **5. Content Manipulation**

| Property / Method                     | Function              | Returns     |
| ------------------------------------- | --------------------- | ----------- |
| `innerHTML`                           | HTML content          | `string`    |
| `outerHTML`                           | Element + HTML        | `string`    |
| `textContent`                         | All text content      | `string`    |
| `innerText`                           | Rendered visible text | `string`    |
| `insertAdjacentHTML(position, html)`  | Insert HTML           | `undefined` |
| `insertAdjacentElement(position, el)` | Insert element        | `Element`   |
| `insertAdjacentText(position, text)`  | Insert text           | `undefined` |

*Positions:* `"beforebegin"`, `"afterbegin"`, `"beforeend"`, `"afterend"`

---

## **6. Attributes**

| Method / Property           | Function                   | Returns          |
| --------------------------- | -------------------------- | ---------------- |
| `getAttribute(name)`        | Get attribute value        | `string \| null` |
| `setAttribute(name, value)` | Set attribute              | `undefined`      |
| `removeAttribute(name)`     | Remove attribute           | `undefined`      |
| `hasAttribute(name)`        | Check attribute exists     | `boolean`        |
| `attributes`                | List of attributes         | `NamedNodeMap`   |
| `dataset`                   | Access `data-*` attributes | `DOMStringMap`   |
| `element.dataset.key`       | Get/set specific `data-*`  | `string`         |

---

## **7. Classes (`classList`)**

| Method                                  | Function              | Returns     |
| --------------------------------------- | --------------------- | ----------- |
| `classList.add(...classes)`             | Add class(es)         | `undefined` |
| `classList.remove(...classes)`          | Remove class(es)      | `undefined` |
| `classList.toggle(class, force?)`       | Toggle class          | `boolean`   |
| `classList.contains(class)`             | Check class existence | `boolean`   |
| `classList.replace(oldClass, newClass)` | Replace class         | `boolean`   |

---

## **8. Styles**

| API                                                 | Function          | Returns               |
| --------------------------------------------------- | ----------------- | --------------------- |
| `element.style.property`                            | Inline style      | `string`              |
| `element.style.cssText`                             | All inline styles | `string`              |
| `getComputedStyle(element)`                         | Computed styles   | `CSSStyleDeclaration` |
| `element.className`                                 | Class string      | `string`              |
| `element.style.setProperty(name, value, priority?)` | Set style         | `undefined`           |

---

## **9. Events**

### Event Registration

| Method                                | Function        | Returns     |
| ------------------------------------- | --------------- | ----------- |
| `addEventListener(type, fn, options)` | Register event  | `undefined` |
| `removeEventListener(type, fn)`       | Remove event    | `undefined` |
| `onclick / oninput / ...`             | Inline property | `function`  |

### Common Events

| Event                      | Trigger         |
| -------------------------- | --------------- |
| `click`                    | Mouse click     |
| `dblclick`                 | Double click    |
| `mouseover` / `mouseenter` | Mouse hover     |
| `mouseout` / `mouseleave`  | Mouse leave     |
| `input`                    | Input change    |
| `change`                   | Value commit    |
| `submit`                   | Form submit     |
| `keydown` / `keyup`        | Keyboard input  |
| `load`                     | Resource loaded |
| `DOMContentLoaded`         | DOM ready       |
| `scroll`                   | Scroll event    |
| `resize`                   | Window resize   |

---

## **10. Event Object**

| Property / Method                  | Function               | Returns     |
| ---------------------------------- | ---------------------- | ----------- |
| `event.target`                     | Source element         | `Element`   |
| `event.currentTarget`              | Bound element          | `Element`   |
| `event.type`                       | Event name             | `string`    |
| `event.preventDefault()`           | Prevent default action | `undefined` |
| `event.stopPropagation()`          | Stop bubbling          | `undefined` |
| `event.stopImmediatePropagation()` | Stop all listeners     | `undefined` |
| `event.defaultPrevented`           | Default prevented?     | `boolean`   |
| `event.bubbles`                    | Bubbles?               | `boolean`   |
| `event.cancelable`                 | Cancelable?            | `boolean`   |

---

## **11. Forms & Inputs**

| API                    | Function                 | Returns                      |
| ---------------------- | ------------------------ | ---------------------------- |
| `form.submit()`        | Submit form              | `undefined`                  |
| `form.reset()`         | Reset form               | `undefined`                  |
| `input.value`          | Get/set value            | `string`                     |
| `input.checked`        | Checkbox/radio state     | `boolean`                    |
| `input.disabled`       | Disabled state           | `boolean`                    |
| `select.value`         | Selected option          | `string`                     |
| `select.selectedIndex` | Index of selected option | `number`                     |
| `option.selected`      | Option selected?         | `boolean`                    |
| `form.elements`        | Form controls collection | `HTMLFormControlsCollection` |

---

## **12. DOM Geometry**

| API                            | Function                                  | Returns   |
| ------------------------------ | ----------------------------------------- | --------- |
| `getBoundingClientRect()`      | Element size & position                   | `DOMRect` |
| `offsetWidth`                  | Layout width                              | `number`  |
| `offsetHeight`                 | Layout height                             | `number`  |
| `offsetTop / offsetLeft`       | Element position relative to offsetParent | `number`  |
| `clientWidth` / `clientHeight` | Inner width/height                        | `number`  |
| `scrollWidth` / `scrollHeight` | Full content size                         | `number`  |
| `scrollTop` / `scrollLeft`     | Scroll offset                             | `number`  |

---

## **13. Scrolling**

| API                                | Function                 | Returns     |
| ---------------------------------- | ------------------------ | ----------- |
| `window.scrollTo(x,y)`             | Scroll page              | `undefined` |
| `window.scrollBy(x,y)`             | Scroll relative          | `undefined` |
| `element.scrollIntoView(options?)` | Scroll element into view | `undefined` |
| `element.scrollTo(x,y)`            | Scroll element           | `undefined` |
| `element.scrollBy(x,y)`            | Scroll element relative  | `undefined` |

---

## **14. Node Info**

| Property        | Function         | Returns          |
| --------------- | ---------------- | ---------------- |
| `nodeType`      | Node type ID     | `number`         |
| `nodeName`      | Node name        | `string`         |
| `nodeValue`     | Node value       | `string \| null` |
| `isConnected`   | Attached to DOM? | `boolean`        |
| `ownerDocument` | Parent document  | `Document`       |

---

## **15. Shadow DOM & Slots**

| API                            | Function                  | Returns           |
| ------------------------------ | ------------------------- | ----------------- |
| `element.attachShadow({mode})` | Create shadow root        | `ShadowRoot`      |
| `shadowRoot.innerHTML`         | Shadow HTML               | `string`          |
| `shadowRoot.querySelector()`   | Select in shadow DOM      | `Element \| null` |
| `<slot>`                       | Placeholder in shadow DOM | `HTMLSlotElement` |
| `slot.assignedNodes()`         | Assigned nodes            | `Array<Node>`     |

---

## **16. Focus & Selection**

| API                      | Function                  | Returns     |
| ------------------------ | ------------------------- | ----------- |
| `element.focus()`        | Focus element             | `undefined` |
| `element.blur()`         | Remove focus              | `undefined` |
| `document.activeElement` | Currently focused element | `Element`   |
| `document.hasFocus()`    | Document focused?         | `boolean`   |

---

## **17. Mutation Observer**

| API                             | Function            | Returns            |
| ------------------------------- | ------------------- | ------------------ |
| `new MutationObserver(fn)`      | Observe DOM changes | `MutationObserver` |
| `observer.observe(el, options)` | Start observing     | `undefined`        |
| `observer.disconnect()`         | Stop observing      | `undefined`        |
| `observer.takeRecords()`        | Pending records     | `MutationRecord[]` |

---

## **18. Element Visibility**

| API                                           | Function                 | Returns                |
| --------------------------------------------- | ------------------------ | ---------------------- |
| `element.hidden`                              | Hide/show element        | `boolean`              |
| `IntersectionObserver(callback, options)`     | Observe visibility       | `IntersectionObserver` |
| `observer.observe(el)`                        | Track element visibility | `undefined`            |
| `observer.disconnect()`                       | Stop tracking            | `undefined`            |
| `IntersectionObserverEntry.isIntersecting`    | Currently visible        | `boolean`              |
| `IntersectionObserverEntry.intersectionRatio` | Visible ratio            | `number`               |

---

## **19. Newer & Misc DOM APIs**

| API                             | Function                        | Returns           |
| ------------------------------- | ------------------------------- | ----------------- |
| `element.attachEvent`           | IE old event                    | `undefined`       |
| `document.createRange()`        | Range object                    | `Range`           |
| `range.setStart / setEnd()`     | Set range boundaries            | `undefined`       |
| `document.execCommand()`        | Legacy exec command             | `boolean`         |
| `element.scrollWidth`           | Scrollable width                | `number`          |
| `element.scrollHeight`          | Scrollable height               | `number`          |
| `element.toggleAttribute(name)` | Toggle boolean attribute        | `boolean`         |
| `adoptedStyleSheets`            | For CSSStyleSheet in Shadow DOM | `CSSStyleSheet[]` |


Do you want me to do that?
