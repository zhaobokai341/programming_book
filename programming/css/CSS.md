# **Ultimate CSS Cheat Sheet: Selectors, Properties, Values, and Functions**

This cheat sheet summarizes **CSS selectors**, **properties (labels)**, **values**, and their **functions**.

---

## **1. CSS Syntax**

```css
selector {
  property: value;
}
```

* **Selector** → what element(s) to style
* **Property (label)** → what to change
* **Value** → how to change it

---

## **2. Selectors**

| Selector         | Function                        | Example              |
| ---------------- | ------------------------------- | -------------------- |
| `*`              | All elements                    | `* { margin: 0; }`   |
| `element`        | Tag name                        | `p {}`               |
| `.class`         | By class                        | `.box {}`            |
| `#id`            | By ID                           | `#header {}`         |
| `A B`            | Descendant                      | `div p {}`           |
| `A > B`          | Direct child                    | `ul > li {}`         |
| `A + B`          | Adjacent sibling                | `h1 + p {}`          |
| `A ~ B`          | General sibling                 | `h1 ~ p {}`          |
| `[attr]`         | Has attribute                   | `[disabled]`         |
| `[attr=value]`   | Attribute value                 | `input[type="text"]` |
| `[attr^=val]`    | Starts with                     | `[class^="btn"]`     |
| `[attr$=val]`    | Ends with                       | `[class$="active"]`  |
| `[attr*=val]`    | Contains                        | `[href*="example"]`  |
| `:hover`         | Pseudo-class (hover)            | `a:hover`            |
| `:active`        | Pseudo-class (active)           | `button:active`      |
| `:focus`         | Pseudo-class (focus)            | `input:focus`        |
| `:first-child`   | First child                     | `li:first-child`     |
| `:last-child`    | Last child                      | `li:last-child`      |
| `:nth-child(n)`  | N-th child                      | `li:nth-child(2)`    |
| `:not(selector)` | Negation                        | `div:not(.active)`   |
| `::before`       | Pseudo-element (before content) | `p::before`          |
| `::after`        | Pseudo-element (after content)  | `p::after`           |
| `::first-letter` | First letter                    | `p::first-letter`    |
| `::first-line`   | First line                      | `p::first-line`      |

---

## **3. Text & Font Properties**

| Property          | Function                        | Common Values                          |
| ----------------- | ------------------------------- | -------------------------------------- |
| `color`           | Text color                      | `red`, `#333`, `rgb(0,0,0)`            |
| `font-size`       | Text size                       | `16px`, `1rem`, `120%`                 |
| `font-family`     | Font type                       | `Arial, sans-serif`                    |
| `font-weight`     | Thickness                       | `normal`, `bold`, `100-900`            |
| `font-style`      | Italic/normal                   | `normal`, `italic`, `oblique`          |
| `line-height`     | Line spacing                    | `1.5`, `24px`, `normal`                |
| `text-align`      | Alignment                       | `left`, `center`, `right`, `justify`   |
| `text-decoration` | Underline/overline/line-through | `none`, `underline`, `line-through`    |
| `text-transform`  | Case change                     | `uppercase`, `lowercase`, `capitalize` |
| `letter-spacing`  | Space between letters           | `1px`, `0.05em`                        |
| `word-spacing`    | Space between words             | `2px`, `0.1em`                         |
| `white-space`     | Text wrapping/spacing           | `normal`, `nowrap`, `pre`, `pre-line`  |
| `text-overflow`   | Overflowing text                | `ellipsis`, `clip`                     |

---

## **4. Box Model**

| Property        | Function          | Example Value               |
| --------------- | ----------------- | --------------------------- |
| `width`         | Element width     | `300px`, `50%`              |
| `height`        | Element height    | `100px`, `auto`             |
| `padding`       | Inner spacing     | `10px`, `1em`               |
| `margin`        | Outer spacing     | `20px`, `auto`              |
| `border`        | Border style      | `1px solid black`           |
| `border-width`  | Border thickness  | `2px`                       |
| `border-style`  | Border line style | `solid`, `dashed`, `none`   |
| `border-color`  | Border color      | `#ccc`, `red`               |
| `border-radius` | Rounded corners   | `8px`, `50%`                |
| `box-sizing`    | Box calculation   | `border-box`, `content-box` |
| `overflow`      | Overflow control  | `hidden`, `scroll`, `auto`  |

---

## **5. Display & Positioning**

| Property                | Function        | Values                                                    |
| ----------------------- | --------------- | --------------------------------------------------------- |
| `display`               | Layout type     | `block`, `inline`, `inline-block`, `flex`, `grid`, `none` |
| `visibility`            | Visibility      | `visible`, `hidden`, `collapse`                           |
| `position`              | Position type   | `static`, `relative`, `absolute`, `fixed`, `sticky`       |
| `top/right/bottom/left` | Position offset | `10px`, `50%`                                             |
| `z-index`               | Stack order     | `1`, `999`                                                |
| `float`                 | Float element   | `left`, `right`, `none`                                   |
| `clear`                 | Clear floats    | `left`, `right`, `both`, `none`                           |

---

## **6. Flexbox**

| Property          | Function             | Common Values                                           |
| ----------------- | -------------------- | ------------------------------------------------------- |
| `display`         | Enable flex          | `flex`, `inline-flex`                                   |
| `flex-direction`  | Main axis            | `row`, `row-reverse`, `column`, `column-reverse`        |
| `justify-content` | Main axis alignment  | `flex-start`, `center`, `space-between`, `space-around` |
| `align-items`     | Cross axis alignment | `flex-start`, `center`, `stretch`, `baseline`           |
| `align-self`      | Item cross alignment | `auto`, `flex-start`, `center`                          |
| `flex-wrap`       | Wrap items           | `nowrap`, `wrap`, `wrap-reverse`                        |
| `gap`             | Space between items  | `10px`, `1rem`                                          |
| `flex`            | Item size shorthand  | `1`, `0 1 auto`, `2 2 50%`                              |

---

## **7. CSS Grid**

| Property                | Function                | Example                      |
| ----------------------- | ----------------------- | ---------------------------- |
| `display`               | Enable grid             | `grid`, `inline-grid`        |
| `grid-template-columns` | Define columns          | `1fr 1fr 1fr`, `100px 2fr`   |
| `grid-template-rows`    | Define rows             | `auto 100px`                 |
| `grid-column`           | Column span/start-end   | `1 / 3`                      |
| `grid-row`              | Row span/start-end      | `1 / 2`                      |
| `place-items`           | Align items (both axes) | `center`, `start`, `stretch` |
| `justify-items`         | Horizontal alignment    | `start`, `center`, `stretch` |
| `align-items`           | Vertical alignment      | `start`, `center`, `stretch` |
| `gap`                   | Grid spacing            | `20px`, `1rem`               |

---

## **8. Backgrounds & Borders**

| Property              | Function                | Example                           |
| --------------------- | ----------------------- | --------------------------------- |
| `background-color`    | Background color        | `#fff`, `rgba(0,0,0,0.5)`         |
| `background-image`    | Background image        | `url(bg.png)`                     |
| `background-size`     | Image size              | `cover`, `contain`, `100% 100%`   |
| `background-position` | Image position          | `center`, `top right`             |
| `background-repeat`   | Repeat behavior         | `repeat`, `no-repeat`, `repeat-x` |
| `background-clip`     | Clip area of background | `border-box`, `padding-box`       |
| `box-shadow`          | Shadow                  | `0 2px 10px rgba(0,0,0,.2)`       |
| `border-image`        | Image border            | `url(border.png) 30 round`        |

---

## **9. Effects & Animation**

| Property                    | Function                | Example                       |
| --------------------------- | ----------------------- | ----------------------------- |
| `opacity`                   | Transparency            | `0.5`                         |
| `transition`                | Smooth property changes | `all 0.3s ease`               |
| `transform`                 | Transform element       | `scale(1.1)`, `rotate(45deg)` |
| `animation`                 | Keyframe animation      | `fade 2s infinite`            |
| `animation-name`            | Animation name          | `fade`                        |
| `animation-duration`        | Duration                | `2s`                          |
| `animation-iteration-count` | Loops                   | `infinite`, `1`               |

```css
@keyframes fade {
  from { opacity: 0; }
  to { opacity: 1; }
}
```

---

## **10. Responsive Design & Units**

| Feature   | Function              | Example                             |
| --------- | --------------------- | ----------------------------------- |
| `@media`  | Media query           | `@media (max-width: 768px) { ... }` |
| `%`       | Relative size         | `width: 50%`                        |
| `vw/vh`   | Viewport width/height | `100vw`, `100vh`                    |
| `rem`     | Root-based unit       | `1rem`                              |
| `em`      | Relative to font size | `2em`                               |
| `clamp()` | Responsive range      | `font-size: clamp(1rem, 2vw, 2rem)` |

---

## **11. Common Functions**

| Function            | Use                 | Example                                |
| ------------------- | ------------------- | -------------------------------------- |
| `calc()`            | Calculate values    | `width: calc(100% - 20px)`             |
| `var()`             | CSS variable        | `color: var(--main)`                   |
| `rgb()`             | Color               | `rgb(255,0,0)`                         |
| `rgba()`            | Color + alpha       | `rgba(0,0,0,.5)`                       |
| `hsl()`             | Color model         | `hsl(200, 50%, 50%)`                   |
| `linear-gradient()` | Gradient background | `linear-gradient(to right, red, blue)` |
| `url()`             | Image URL           | `background-image: url(img.png)`       |

```css
:root {
  --main: #3498db;
  --secondary: #2ecc71;
}
```

---

## **12. Global, Reset & Accessibility**

| Property      | Function              | Example                  |
| ------------- | --------------------- | ------------------------ |
| `cursor`      | Mouse cursor          | `pointer`, `default`     |
| `user-select` | Text selection        | `none`, `auto`           |
| `outline`     | Focus outline         | `none`, `2px solid blue` |
| `appearance`  | Remove native styling | `none`                   |
| `box-sizing`  | Box sizing reset      | `border-box`             |
| `all`         | Reset all properties  | `all: unset`             |
| `visibility`  | Show/hide element     | `visible`, `hidden`      |


Do you want me to do that next?
