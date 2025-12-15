Below is a **JavaScript (JS) local cheat sheet** — **no document / no canvas**, just plain Markdown here.

---

## 1. Basics

```js
// comment
let x = 10;      // mutable
const y = 20;    // immutable
var z = 30;      // function-scoped (avoid)
```

| Keyword | Function                 |
| ------- | ------------------------ |
| `let`   | Block-scoped variable    |
| `const` | Block-scoped constant    |
| `var`   | Function-scoped (legacy) |

---

## 2. Data Types

| Type      | Example        |
| --------- | -------------- |
| Number    | `42`, `3.14`   |
| String    | `"hi"`         |
| Boolean   | `true`         |
| Undefined | `let a;`       |
| Null      | `null`         |
| Object    | `{}`           |
| Array     | `[]`           |
| Function  | `function(){}` |
| Symbol    | `Symbol('id')` |
| BigInt    | `123n`         |

```js
typeof 123      // "number"
Array.isArray([]) // true
```

---

## 3. Operators

| Operator    | Function           |   |    |
| ----------- | ------------------ | - | -- |
| `+ - * / %` | Math               |   |    |
| `**`        | Power              |   |    |
| `=`         | Assign             |   |    |
| `==`        | Loose compare      |   |    |
| `===`       | Strict compare     |   |    |
| `&&`        | AND                |   |    |
| `           |                    | ` | OR |
| `!`         | NOT                |   |    |
| `??`        | Nullish coalescing |   |    |
| `?.`        | Optional chaining  |   |    |

```js
a ?? b        // if a is null/undefined
obj?.user?.id
```

---

## 4. Control Flow

```js
if (a > 10) {}
else {}

switch(x) {
  case 1: break;
  default: break;
}

for (let i = 0; i < 3; i++) {}
while (x > 0) {}
do {} while (x > 0)
```

---

## 5. Functions

```js
function add(a, b) {
  return a + b
}

const sub = (a, b) => a - b
```

| Concept        | Meaning                     |
| -------------- | --------------------------- |
| Arrow function | Short syntax                |
| Callback       | Function passed as argument |
| IIFE           | Runs immediately            |

```js
(() => console.log("run"))()
```

---

## 6. Scope & Hoisting

| Concept  | Explanation                    |
| -------- | ------------------------------ |
| Scope    | Variable visibility            |
| Hoisting | `var` & functions moved up     |
| Closure  | Function remembers outer scope |

```js
function outer() {
  let x = 5
  return () => x
}
```

---

## 7. Arrays

```js
const arr = [1,2,3]
```

| Method     | Function     |
| ---------- | ------------ |
| `push`     | Add end      |
| `pop`      | Remove end   |
| `shift`    | Remove start |
| `unshift`  | Add start    |
| `map`      | Transform    |
| `filter`   | Select       |
| `reduce`   | Accumulate   |
| `find`     | First match  |
| `includes` | Contains     |

```js
arr.map(x => x * 2)
```

---

## 8. Objects

```js
const user = {
  name: "A",
  age: 20
}
```

| Operation | Example               |
| --------- | --------------------- |
| Access    | `user.name`           |
| Add       | `user.id = 1`         |
| Delete    | `delete user.age`     |
| Keys      | `Object.keys(user)`   |
| Values    | `Object.values(user)` |

---

## 9. Destructuring

```js
const [a, b] = [1, 2]
const {name} = user
```

---

## 10. Spread & Rest

```js
const a = [1,2]
const b = [...a, 3]

function sum(...nums) {}
```

---

## 11. Strings

| Method          | Function      |
| --------------- | ------------- |
| `length`        | Size          |
| `toUpperCase()` | Uppercase     |
| `includes()`    | Contains      |
| `slice()`       | Cut           |
| `replace()`     | Replace       |
| `split()`       | To array      |
| `trim()`        | Remove spaces |

```
```
