# CSS Cheat Sheet: Selectors, Properties (Label), Values, and Functions

This document summarizes **CSS selectors**, **properties (labels)**, **values**, and their **functions (what they do)** in Markdown format.

---

## 1. CSS Syntax

```css
selector {
  property: value;
}
```

* **Selector** → what element(s) to style
* **Property (label)** → what to change
* **Value** → how to change it

---

## 2. Selectors

| Selector       | Function         | Example              |
| -------------- | ---------------- | -------------------- |
| `*`            | All elements     | `* { margin: 0; }`   |
| `element`      | By tag name      | `p {}`               |
| `.class`       | By class         | `.box {}`            |
| `#id`          | By ID            | `#header {}`         |
| `A B`          | Descendant       | `div p {}`           |
| `A > B`        | Direct child     | `ul > li {}`         |
| `A + B`        | Adjacent sibling | `h1 + p {}`          |
| `A ~ B`        | General sibling  | `h1 ~ p {}`          |
| `[attr]`       | Has attribute    | `[disabled]`         |
| `[attr=value]` | Attribute value  | `input[type="text"]` |
| `:hover`       | Pseudo-class     | `a:hover`            |
| `::before`     | Pseudo-element   | `p::before`          |

---

## 3. Text & Font Properties

| Property          | Function              | Common Values           |
| ----------------- | --------------------- | ----------------------- |
| `color`           | Text color            | `red`, `#333`           |
| `font-size`       | Text size             | `16px`, `1rem`          |
| `font-family`     | Font type             | `Arial, sans-serif`     |
| `font-weight`     | Font thickness        | `normal`, `bold`, `700` |
| `font-style`      | Italic/normal         | `normal`, `italic`      |
| `line-height`     | Line spacing          | `1.5`, `24px`           |
| `text-align`      | Alignment             | `left`, `center`        |
| `text-decoration` | Underline etc.        | `none`, `underline`     |
| `text-transform`  | Case change           | `uppercase`             |
| `letter-spacing`  | Space between letters | `1px`                   |

---

## 4. Box Model

| Property     | Function         | Example Value      |
| ------------ | ---------------- | ------------------ |
| `width`      | Element width    | `300px`            |
| `height`     | Element height   | `100px`            |
| `padding`    | Inner spacing    | `10px`             |
| `margin`     | Outer spacing    | `20px`             |
| `border`     | Border style     | `1px solid black`  |
| `box-sizing` | Box calculation  | `border-box`       |
| `overflow`   | Overflow control | `hidden`, `scroll` |

---

## 5. Display & Position

| Property                | Function        | Values                                              |
| ----------------------- | --------------- | --------------------------------------------------- |
| `display`               | Layout type     | `block`, `inline`, `flex`, `grid`, `none`           |
| `visibility`            | Visibility      | `visible`, `hidden`                                 |
| `position`              | Position type   | `static`, `relative`, `absolute`, `fixed`, `sticky` |
| `top/right/bottom/left` | Position offset | `10px`                                              |
| `z-index`               | Stack order     | `1`, `999`                                          |

---

## 6. Flexbox

| Property          | Function            | Common Values             |
| ----------------- | ------------------- | ------------------------- |
| `display`         | Enable flex         | `flex`                    |
| `flex-direction`  | Main axis           | `row`, `column`           |
| `justify-content` | Main alignment      | `center`, `space-between` |
| `align-items`     | Cross alignment     | `center`, `stretch`       |
| `flex-wrap`       | Wrap items          | `wrap`                    |
| `gap`             | Space between items | `10px`                    |
| `flex`            | Item size           | `1`, `0 1 auto`           |

---

## 7. Grid

| Property                | Function    | Example      |
| ----------------------- | ----------- | ------------ |
| `display`               | Enable grid | `grid`       |
| `grid-template-columns` | Columns     | `1fr 1fr`    |
| `grid-template-rows`    | Rows        | `auto 100px` |
| `grid-column`           | Column span | `1 / 3`      |
| `grid-row`              | Row span    | `1 / 2`      |
| `place-items`           | Align items | `center`     |
| `gap`                   | Spacing     | `20px`       |

---

## 8. Background & Border

| Property              | Function         | Example                     |
| --------------------- | ---------------- | --------------------------- |
| `background-color`    | Background color | `#fff`                      |
| `background-image`    | Background image | `url(bg.png)`               |
| `background-size`     | Image size       | `cover`                     |
| `background-position` | Image position   | `center`                    |
| `border-radius`       | Rounded corners  | `8px`                       |
| `box-shadow`          | Shadow           | `0 2px 10px rgba(0,0,0,.2)` |

---

## 9. Effects & Animation

| Property     | Function           | Example            |
| ------------ | ------------------ | ------------------ |
| `opacity`    | Transparency       | `0.5`              |
| `transition` | Smooth change      | `all 0.3s ease`    |
| `transform`  | Transform element  | `scale(1.1)`       |
| `animation`  | Keyframe animation | `fade 2s infinite` |

```css
@keyframes fade {
  from { opacity: 0; }
  to { opacity: 1; }
}
```

---

## 10. Responsive Design

| Feature  | Function        | Example                     |
| -------- | --------------- | --------------------------- |
| `@media` | Media query     | `@media (max-width: 768px)` |
| `%`      | Relative size   | `width: 50%`                |
| `vw/vh`  | Viewport units  | `100vw`                     |
| `rem`    | Root-based size | `1rem`                      |

---

## 11. Common Functions

| Function | Use              | Example                    |
| -------- | ---------------- | -------------------------- |
| `calc()` | Calculate values | `width: calc(100% - 20px)` |
| `var()`  | CSS variable     | `color: var(--main)`       |
| `rgb()`  | Color            | `rgb(255,0,0)`             |
| `rgba()` | Color + alpha    | `rgba(0,0,0,.5)`           |
| `hsl()`  | Color model      | `hsl(200, 50%, 50%)`       |

```css
:root {
  --main: #3498db;
}
```

---

## 12. Global & Reset

| Property      | Function       | Example   |
| ------------- | -------------- | --------- |
| `cursor`      | Mouse cursor   | `pointer` |
| `user-select` | Text selection | `none`    |
| `outline`     | Focus outline  | `none`    |
| `appearance`  | Native style   | `none`    |

---

**If you want:**

* CSS interview questions
* Beginner-only CSS
* Flexbox vs Grid comparison
* CSS + HTML examples
* Printable PDF

Tell me 👍
