# 6️⃣ ES6+ JavaScript Features

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

Thanks! Here's a clean and properly formatted version of your content in **Markdown**, combining clarity with structure:

---

## 🔹 7. What Are Promises?

Promises represent the **future completion or failure** of asynchronous operations.

### ✅ Example

```javascript
fetch("/data")
  .then((response) => response.json())
  .then((data) => console.log(data))
  .catch((error) => console.error(error));
```

### 🔄 Promise States

- **Pending**: Initial state, operation not yet completed.
- **Fulfilled**: Operation completed successfully.
- **Rejected**: Operation failed.

> Use `.then()` for success, `.catch()` for errors, and `.finally()` for cleanup.

---

## 🔹 What Is a Promise?

A **Promise** is a JavaScript object that represents the eventual result of an asynchronous operation.

It allows you to write cleaner, more readable async code without deeply nested callbacks.

### 📌 Summary

- Promises simplify async flow.
- They help avoid "callback hell."
- They support chaining and error handling.

---

Let me know if you'd like this turned into a visual cheat sheet or expanded into a full tutorial!

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

---
