# JavaScript – Functions, Classes, Values, and Return Values

---

## 1. Global Functions

| Function               | Purpose                     | Returns      |
| ---------------------- | --------------------------- | ------------ |
| `eval(str)`            | Execute JS code from string | Any          |
| `isNaN(value)`         | Check if value is NaN       | `boolean`    |
| `isFinite(value)`      | Check finite number         | `boolean`    |
| `parseInt(str, radix)` | String → integer            | `number`     |
| `parseFloat(str)`      | String → float              | `number`     |
| `encodeURI(uri)`       | Encode URI                  | `string`     |
| `decodeURI(uri)`       | Decode URI                  | `string`     |
| `setTimeout(fn, ms)`   | Delay execution             | `timeoutID`  |
| `setInterval(fn, ms)`  | Repeat execution            | `intervalID` |
| `clearTimeout(id)`     | Cancel timeout              | `undefined`  |
| `clearInterval(id)`    | Cancel interval             | `undefined`  |

---

## 2. Console Functions

| Function            | Purpose       | Returns     |
| ------------------- | ------------- | ----------- |
| `console.log()`     | Print output  | `undefined` |
| `console.error()`   | Print error   | `undefined` |
| `console.warn()`    | Print warning | `undefined` |
| `console.table()`   | Table display | `undefined` |
| `console.time()`    | Start timer   | `undefined` |
| `console.timeEnd()` | End timer     | `undefined` |

---

## 3. Number Functions & Values

### Static (`Number.`)

| Function / Value           | Purpose           | Returns   |
| -------------------------- | ----------------- | --------- |
| `Number()`                 | Convert to number | `number`  |
| `Number.isNaN()`           | Strict NaN check  | `boolean` |
| `Number.isInteger()`       | Integer check     | `boolean` |
| `Number.parseInt()`        | Parse integer     | `number`  |
| `Number.MAX_VALUE`         | Max number        | `number`  |
| `Number.MIN_VALUE`         | Min number        | `number`  |
| `Number.POSITIVE_INFINITY` | +∞                | `number`  |

### Instance (`number.`)

| Function     | Purpose           | Returns  |
| ------------ | ----------------- | -------- |
| `toFixed(n)` | Fixed decimals    | `string` |
| `toString()` | Convert to string | `string` |

---

## 4. Math Object

| Function / Value | Purpose         | Returns  |
| ---------------- | --------------- | -------- |
| `Math.abs(x)`    | Absolute value  | `number` |
| `Math.ceil(x)`   | Round up        | `number` |
| `Math.floor(x)`  | Round down      | `number` |
| `Math.round(x)`  | Nearest integer | `number` |
| `Math.max(a,b)`  | Max value       | `number` |
| `Math.min(a,b)`  | Min value       | `number` |
| `Math.random()`  | Random 0–1      | `number` |
| `Math.pow(a,b)`  | Power           | `number` |
| `Math.sqrt(x)`   | Square root     | `number` |
| `Math.PI`        | π value         | `number` |

---

## 5. String Functions

| Function          | Purpose            | Returns   |
| ----------------- | ------------------ | --------- |
| `length`          | String length      | `number`  |
| `charAt(i)`       | Char at index      | `string`  |
| `includes(str)`   | Contains substring | `boolean` |
| `indexOf(str)`    | First index        | `number`  |
| `slice(a,b)`      | Extract substring  | `string`  |
| `substring(a,b)`  | Extract substring  | `string`  |
| `replace(a,b)`    | Replace text       | `string`  |
| `replaceAll(a,b)` | Replace all        | `string`  |
| `split(sep)`      | Split to array     | `Array`   |
| `toUpperCase()`   | Uppercase          | `string`  |
| `toLowerCase()`   | Lowercase          | `string`  |
| `trim()`          | Remove spaces      | `string`  |

---

## 6. Array Functions

| Function           | Purpose      | Returns               |
| ------------------ | ------------ | --------------------- |
| `push(x)`          | Add end      | `number` (new length) |
| `pop()`            | Remove end   | `any`                 |
| `shift()`          | Remove start | `any`                 |
| `unshift(x)`       | Add start    | `number`              |
| `map(fn)`          | Transform    | `Array`               |
| `filter(fn)`       | Filter       | `Array`               |
| `reduce(fn, init)` | Reduce       | `any`                 |
| `find(fn)`         | First match  | `any`                 |
| `findIndex(fn)`    | Match index  | `number`              |
| `includes(x)`      | Contains     | `boolean`             |
| `some(fn)`         | Any true     | `boolean`             |
| `every(fn)`        | All true     | `boolean`             |
| `concat(arr)`      | Merge arrays | `Array`               |
| `slice(a,b)`       | Copy portion | `Array`               |
| `splice()`         | Modify array | `Array`               |

---

## 7. Object Functions

| Function              | Purpose            | Returns         |
| --------------------- | ------------------ | --------------- |
| `Object.keys(obj)`    | Keys               | `Array<string>` |
| `Object.values(obj)`  | Values             | `Array<any>`    |
| `Object.entries(obj)` | Key-value pairs    | `Array`         |
| `Object.assign(a,b)`  | Merge objects      | `Object`        |
| `Object.freeze(obj)`  | Make immutable     | `Object`        |
| `Object.seal(obj)`    | Prevent add/remove | `Object`        |
| `hasOwn(obj,key)`     | Own property check | `boolean`       |

---

## 8. Date Class

| Function           | Purpose      | Returns  |
| ------------------ | ------------ | -------- |
| `new Date()`       | Current date | `Date`   |
| `getFullYear()`    | Year         | `number` |
| `getMonth()`       | Month (0–11) | `number` |
| `getDate()`        | Day          | `number` |
| `getTime()`        | Timestamp    | `number` |
| `toISOString()`    | ISO string   | `string` |
| `toLocaleString()` | Local format | `string` |

---

## 9. JSON

| Function              | Purpose       | Returns  |
| --------------------- | ------------- | -------- |
| `JSON.stringify(obj)` | Object → JSON | `string` |
| `JSON.parse(str)`     | JSON → Object | `Object` |

---

## 10. Functions & Return Rules

```js
function f() {
  return 5
}
```

| Case       | Return Value |
| ---------- | ------------ |
| `return x` | `x`          |
| `return`   | `undefined`  |
| no return  | `undefined`  |

---

## 11. Classes

```js
class User {
  constructor(name) {
    this.name = name
  }

  greet() {
    return "Hello " + this.name
  }
}
```

| Part            | Purpose        | Returns  |
| --------------- | -------------- | -------- |
| `constructor()` | Initialize     | instance |
| `method()`      | Class function | any      |
| `new Class()`   | Create object  | instance |

---

## 12. Promises & Async

| Function          | Purpose         | Returns        |
| ----------------- | --------------- | -------------- |
| `new Promise(fn)` | Async wrapper   | `Promise`      |
| `then(fn)`        | Success handler | `Promise`      |
| `catch(fn)`       | Error handler   | `Promise`      |
| `finally(fn)`     | Cleanup         | `Promise`      |
| `async function`  | Async function  | `Promise`      |
| `await promise`   | Wait result     | resolved value |

---

## 13. Error Handling

| Function / Class    | Purpose      | Returns |
| ------------------- | ------------ | ------- |
| `try/catch`         | Catch errors | —       |
| `throw new Error()` | Throw error  | never   |
| `Error(message)`    | Error object | `Error` |

---

## 14. Type & Value Checks

| Expression           | Returns   |
| -------------------- | --------- |
| `typeof x`           | `string`  |
| `x instanceof Class` | `boolean` |
| `Array.isArray(x)`   | `boolean` |
| `Boolean(x)`         | `boolean` |
| `String(x)`          | `string`  |
| `Number(x)`          | `number`  |


Just say 👍
