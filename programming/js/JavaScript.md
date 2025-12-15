# **Ultimate JavaScript Cheat Sheet – Local Functions, Classes, Values, and Returns**

---

## **1. Global / Built-in Functions (Local Use)**

| Function                  | Purpose               | Returns   |
| ------------------------- | --------------------- | --------- |
| `isNaN(value)`            | Check if value is NaN | `boolean` |
| `isFinite(value)`         | Check finite number   | `boolean` |
| `parseInt(str, radix)`    | String → integer      | `number`  |
| `parseFloat(str)`         | String → float        | `number`  |
| `encodeURI(uri)`          | Encode URI            | `string`  |
| `decodeURI(uri)`          | Decode URI            | `string`  |
| `encodeURIComponent(str)` | Encode URI component  | `string`  |
| `decodeURIComponent(str)` | Decode URI component  | `string`  |
| `Number(value)`           | Convert to number     | `number`  |
| `String(value)`           | Convert to string     | `string`  |
| `Boolean(value)`          | Convert to boolean    | `boolean` |
| `Object(value)`           | Convert to object     | `object`  |

---

## **2. Console Functions**

| Function            | Purpose                    | Returns     |
| ------------------- | -------------------------- | ----------- |
| `console.log()`     | Print output               | `undefined` |
| `console.error()`   | Print error                | `undefined` |
| `console.warn()`    | Print warning              | `undefined` |
| `console.table()`   | Table display              | `undefined` |
| `console.time()`    | Start timer                | `undefined` |
| `console.timeEnd()` | End timer & print duration | `undefined` |
| `console.clear()`   | Clear console              | `undefined` |

---

## **3. Number Methods & Values**

### Static (`Number.`)

| Method / Value             | Purpose             | Returns   |
| -------------------------- | ------------------- | --------- |
| `Number.isNaN(value)`      | Strict NaN check    | `boolean` |
| `Number.isInteger(value)`  | Check integer       | `boolean` |
| `Number.parseInt()`        | Parse integer       | `number`  |
| `Number.parseFloat()`      | Parse float         | `number`  |
| `Number.MAX_VALUE`         | Max finite number   | `number`  |
| `Number.MIN_VALUE`         | Min positive number | `number`  |
| `Number.POSITIVE_INFINITY` | +Infinity           | `number`  |
| `Number.NEGATIVE_INFINITY` | -Infinity           | `number`  |

### Instance (`number.`)

| Method            | Purpose                               | Returns  |
| ----------------- | ------------------------------------- | -------- |
| `toFixed(n)`      | Fixed decimals                        | `string` |
| `toString(radix)` | Convert to string with optional radix | `string` |
| `toPrecision(n)`  | Round to significant digits           | `string` |
| `valueOf()`       | Primitive number value                | `number` |

---

## **4. Math Object**

| Method / Value                      | Purpose         | Returns  |
| ----------------------------------- | --------------- | -------- |
| `Math.abs(x)`                       | Absolute value  | `number` |
| `Math.ceil(x)`                      | Round up        | `number` |
| `Math.floor(x)`                     | Round down      | `number` |
| `Math.round(x)`                     | Nearest integer | `number` |
| `Math.max(a,b,...)`                 | Maximum         | `number` |
| `Math.min(a,b,...)`                 | Minimum         | `number` |
| `Math.random()`                     | Random 0–1      | `number` |
| `Math.pow(a,b)`                     | Power           | `number` |
| `Math.sqrt(x)`                      | Square root     | `number` |
| `Math.PI`                           | π constant      | `number` |
| `Math.sin(x)` / `cos(x)` / `tan(x)` | Trig functions  | `number` |

---

## **5. String Methods**

| Method                | Purpose                  | Returns   |
| --------------------- | ------------------------ | --------- |
| `length`              | String length            | `number`  |
| `charAt(i)`           | Character at index       | `string`  |
| `includes(str)`       | Substring check          | `boolean` |
| `startsWith(str)`     | Starts with substring    | `boolean` |
| `endsWith(str)`       | Ends with substring      | `boolean` |
| `indexOf(str)`        | First index of substring | `number`  |
| `lastIndexOf(str)`    | Last index of substring  | `number`  |
| `slice(a,b)`          | Extract substring        | `string`  |
| `substring(a,b)`      | Extract substring        | `string`  |
| `substr(a,length)`    | Extract substring        | `string`  |
| `replace(a,b)`        | Replace first occurrence | `string`  |
| `replaceAll(a,b)`     | Replace all occurrences  | `string`  |
| `split(sep)`          | Convert to array         | `Array`   |
| `toUpperCase()`       | Uppercase                | `string`  |
| `toLowerCase()`       | Lowercase                | `string`  |
| `trim()`              | Remove whitespace        | `string`  |
| `padStart(len, char)` | Left pad                 | `string`  |
| `padEnd(len, char)`   | Right pad                | `string`  |

---

## **6. Array Methods**

| Method                         | Purpose                 | Returns               |
| ------------------------------ | ----------------------- | --------------------- |
| `push(x)`                      | Add to end              | `number` (new length) |
| `pop()`                        | Remove last             | element               |
| `shift()`                      | Remove first            | element               |
| `unshift(x)`                   | Add to start            | `number` (new length) |
| `map(fn)`                      | Transform each element  | `Array`               |
| `filter(fn)`                   | Filter elements         | `Array`               |
| `reduce(fn, init)`             | Reduce to value         | any                   |
| `find(fn)`                     | First match             | element / `undefined` |
| `findIndex(fn)`                | Index of first match    | `number`              |
| `includes(x)`                  | Check element existence | `boolean`             |
| `some(fn)`                     | Any element true        | `boolean`             |
| `every(fn)`                    | All elements true       | `boolean`             |
| `concat(arr)`                  | Merge arrays            | `Array`               |
| `slice(a,b)`                   | Copy portion            | `Array`               |
| `splice(start, del, items...)` | Modify array            | `Array`               |
| `indexOf(x)`                   | First index             | `number`              |
| `lastIndexOf(x)`               | Last index              | `number`              |
| `reverse()`                    | Reverse array           | `Array`               |
| `sort(fn?)`                    | Sort array              | `Array`               |
| `flat(depth)`                  | Flatten array           | `Array`               |

---

## **7. Object Methods**

| Method / Function        | Purpose                  | Returns              |
| ------------------------ | ------------------------ | -------------------- |
| `Object.keys(obj)`       | Array of keys            | `Array<string>`      |
| `Object.values(obj)`     | Array of values          | `Array<any>`         |
| `Object.entries(obj)`    | Key-value pairs          | `Array<[key,value]>` |
| `Object.assign(a,b)`     | Merge objects            | `Object`             |
| `Object.freeze(obj)`     | Make immutable           | `Object`             |
| `Object.seal(obj)`       | Prevent add/remove props | `Object`             |
| `Object.hasOwn(obj,key)` | Own property check       | `boolean`            |
| `delete obj.prop`        | Delete property          | `boolean`            |

---

## **8. Date Methods**

| Method             | Purpose           | Returns  |
| ------------------ | ----------------- | -------- |
| `new Date()`       | Current date      | `Date`   |
| `getFullYear()`    | Year              | `number` |
| `getMonth()`       | Month (0–11)      | `number` |
| `getDate()`        | Day of month      | `number` |
| `getDay()`         | Day of week (0–6) | `number` |
| `getHours()`       | Hours             | `number` |
| `getMinutes()`     | Minutes           | `number` |
| `getSeconds()`     | Seconds           | `number` |
| `getTime()`        | Timestamp ms      | `number` |
| `toISOString()`    | ISO string        | `string` |
| `toLocaleString()` | Local format      | `string` |

---

## **9. JSON**

| Method                | Purpose              | Returns  |
| --------------------- | -------------------- | -------- |
| `JSON.stringify(obj)` | Object → JSON string | `string` |
| `JSON.parse(str)`     | JSON string → Object | `Object` |

---

## **10. Functions & Return Values**

```js
function example() {
  return 5;
}
```

| Case                        | Return Value |
| --------------------------- | ------------ |
| `return x`                  | `x`          |
| `return`                    | `undefined`  |
| No return statement         | `undefined`  |
| Arrow functions: `() => x`  | `x`          |
| Arrow functions: `() => {}` | `undefined`  |

---

## **11. Classes**

```js
class User {
  constructor(name) {
    this.name = name;
  }

  greet() {
    return `Hello ${this.name}`;
  }
}
```

| Part              | Purpose             | Returns  |
| ----------------- | ------------------- | -------- |
| `constructor()`   | Initialize instance | object   |
| `method()`        | Class function      | any      |
| `static method()` | Static class method | any      |
| `new Class()`     | Create object       | instance |

---

## **12. Promises & Async**

| Function / Keyword | Purpose             | Returns        |
| ------------------ | ------------------- | -------------- |
| `new Promise(fn)`  | Async wrapper       | `Promise`      |
| `then(fn)`         | Success callback    | `Promise`      |
| `catch(fn)`        | Error callback      | `Promise`      |
| `finally(fn)`      | Cleanup             | `Promise`      |
| `async function`   | Async function      | `Promise`      |
| `await promise`    | Wait resolved value | resolved value |

---

## **13. Error Handling**

| Method / Keyword       | Purpose      | Returns |
| ---------------------- | ------------ | ------- |
| `try { } catch(e){}`   | Catch errors | —       |
| `throw new Error(msg)` | Throw error  | never   |
| `Error(msg)`           | Error object | `Error` |

---

## **14. Type & Value Checks**

| Expression           | Returns                                                                      |
| -------------------- | ---------------------------------------------------------------------------- |
| `typeof x`           | `"string"`, `"number"`, `"boolean"`, `"object"`, `"function"`, `"undefined"` |
| `x instanceof Class` | `boolean`                                                                    |
| `Array.isArray(x)`   | `boolean`                                                                    |
| `Boolean(x)`         | `boolean`                                                                    |
| `String(x)`          | `string`                                                                     |
| `Number(x)`          | `number`                                                                     |
| `Object(x)`          | `object`                                                                     |
| `x === null`         | `boolean`                                                                    |
