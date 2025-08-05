````markdown
## 🔟 JavaScript Miscellaneous Concepts

### 1. What is `NaN` and How to Check It?

🔢 `NaN` stands for **Not-a-Number** and appears when a numeric operation fails:

```javascript
const result = "hello" / 2; // NaN
```
````

To check for `NaN`, use:

```javascript
Number.isNaN(value); // ✅ Accurate and strict check
```

> Avoid `isNaN()` (global) as it coerces non-numeric values and may give false positives.

---

### 2. Difference Between `null` and `undefined`

| Value       | Meaning                            | Type        |
| ----------- | ---------------------------------- | ----------- |
| `undefined` | Variable declared but not assigned | `undefined` |
| `null`      | Intentional absence of value       | `object`    |

📌 Example:

```javascript
let a;
console.log(a); // undefined

let b = null;
console.log(b); // null
```

> Use `null` to deliberately clear a value; `undefined` often means “not yet assigned.”

---

### 3. What is the Use of the `this` Keyword?

👤 `this` refers to the **execution context**—the object that owns the function.

Its value depends on **how the function is called**, not where it's defined.

📌 Example:

```javascript
const person = {
  name: "Avi",
  greet() {
    console.log(`Hi, I'm ${this.name}`);
  },
};
person.greet(); // "Hi, I'm Avi"
```

Arrow functions do **not** have their own `this`; they inherit from their enclosing context.

---

### 4. Difference Between `call()`, `apply()`, and `bind()`

All three allow you to explicitly set the `this` value when invoking functions.

| Method    | Executes Immediately?    | Arguments Format   |
| --------- | ------------------------ | ------------------ |
| `call()`  | ✅ Yes                   | Comma-separated    |
| `apply()` | ✅ Yes                   | Array of arguments |
| `bind()`  | ❌ No (returns function) | Comma-separated    |

📌 Example:

```javascript
function intro(language) {
  console.log(`${this.name} codes in ${language}`);
}
const dev = { name: "Tara" };

intro.call(dev, "JavaScript");
intro.apply(dev, ["Python"]);

const boundIntro = intro.bind(dev, "Go");
boundIntro(); // Executes later
```

---

### 5. What are Debounce and Throttle?

Both control how often functions execute—commonly used in **performance optimization**.

| Concept      | Behavior                                    | Use Case                 |
| ------------ | ------------------------------------------- | ------------------------ |
| **Debounce** | Delays function until user stops triggering | Search box, resize event |
| **Throttle** | Limits execution to once per time interval  | Scroll, mouse movement   |

📌 Debounce Example:

```javascript
function debounce(func, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => func.apply(this, args), delay);
  };
}
```

📌 Throttle Example:

```javascript
function throttle(func, limit) {
  let inThrottle;
  return function (...args) {
    if (!inThrottle) {
      func.apply(this, args);
      inThrottle = true;
      setTimeout(() => (inThrottle = false), limit);
    }
  };
}
```

---

JavaScript’s oddities are part of its charm! Want to take these ideas into practical challenges or quiz-style review? I can cook something up 🌟

```

```
