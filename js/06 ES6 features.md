````markdown
## 6️⃣ ES6+ JavaScript Features

### 1. Difference between `let`, `const`, and `var`

| Keyword | Scope    | Reassignment | Hoisting Behavior           |
| ------- | -------- | ------------ | --------------------------- |
| `var`   | Function | ✅ Yes       | Hoisted with **undefined**  |
| `let`   | Block    | ✅ Yes       | Hoisted but not initialized |
| `const` | Block    | ❌ No        | Hoisted but not initialized |

📌 Use `let` for variables that change, `const` for fixed values, and avoid `var` unless you need function scope.

---

### 2. Arrow Functions vs Regular Functions

```javascript
const greet = (name) => `Hello, ${name}`;
```
````

| Feature        | Arrow Function           | Regular Function               |
| -------------- | ------------------------ | ------------------------------ |
| `this` Binding | Lexical (inherits)       | Dynamic (depends on call site) |
| Syntax         | Short and clean          | More verbose                   |
| Suited for     | Callbacks, concise logic | Object methods, constructors   |

---

### 3. What are Template Literals?

Use backticks `` ` `` for string interpolation and multiline strings:

```javascript
const name = "Leo";
const greeting = `Hello, ${name}!`;
```

> Replace tricky concatenation with readable, embedded expressions.

---

### 4. Rest `...` and Spread `...` Operators

- **Rest** collects remaining items into an array:
  ```javascript
  function sum(...nums) {
    return nums.reduce((a, b) => a + b);
  }
  ```
- **Spread** expands items from an array or object:
  ```javascript
  const arr = [1, 2, 3];
  const copy = [...arr]; // [1, 2, 3]
  ```

> Handy for flexible functions and immutably copying data.

---

### 5. What are Default Parameters?

Set fallback values in function definitions:

```javascript
function greet(name = "Guest") {
  return `Hello, ${name}`;
}
```

No need for manual checks like `name = name || 'Guest'`

---

### 6. Destructuring in JavaScript

Extract values from arrays or objects:

```javascript
const [a, b] = [1, 2]; // Array
const { name, age } = { name: "Zoe", age: 28 }; // Object
```

> Makes code cleaner and avoids repetitive dot access.

---

### 7. What Are Promises?

Promises represent **future completion** of async operations:

```javascript
fetch("/data")
  .then((response) => response.json())
  .then((data) => console.log(data))
  .catch((error) => console.error(error));
```

States: **pending → fulfilled → rejected**

> Use `.then()`, `.catch()`, and `.finally()` for control.

---

### 8. What Is `async/await`?

Syntactic sugar over promises for cleaner async code:

```javascript
async function loadData() {
  try {
    const response = await fetch("/data");
    const data = await response.json();
    console.log(data);
  } catch (err) {
    console.error(err);
  }
}
```

> No more callback pyramids — reads like synchronous code!

```

Ready to level up with modules, generators, or tackle the event loop next? Let’s keep your JavaScript journey rolling 🔄🧠
```
