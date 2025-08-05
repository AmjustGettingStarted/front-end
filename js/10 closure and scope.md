````markdown
## 9️⃣ Closures & Scope in JavaScript

### 1. What is a Closure?

🔒 A **closure** is formed when a function retains access to variables from its **outer scope**, even after that outer function has finished executing.

📌 Example:

```javascript
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}
const counter = outer();
counter(); // 1
counter(); // 2
```
````

> Here, `inner()` is a closure that remembers `count` from `outer()`'s scope!

---

### 2. What is Lexical Scope?

📦 **Lexical scope** means a function’s scope is determined by its position in the source code.

Each inner function has access to variables from:

- Its own scope
- The scope of its parent
- The global scope

📌 Example:

```javascript
const x = 10;
function foo() {
  const y = 20;
  function bar() {
    console.log(x + y); // Accesses both outer scopes
  }
  bar();
}
```

> Scope is resolved **at the time of writing**, not at runtime.

---

### 3. Use Cases for Closures

✅ **Closures shine** in:

- **Encapsulation**: Preserve state in functional constructs
- **Callbacks**: Pass functions with internal memory
- **Event handlers**: Capture variables in UI logic
- **Partial application/currying**: Fix part of a function’s parameters

📌 Example: Counter Generator

```javascript
function makeCounter() {
  let count = 0;
  return () => ++count;
}
const counter = makeCounter();
console.log(counter()); // 1
console.log(counter()); // 2
```

---

### 4. How Do Closures Help with Data Privacy?

🔐 Closures allow data to remain **hidden** and **protected**, simulating private variables.

📌 Example:

```javascript
function secretHolder() {
  let secret = "hidden!";
  return {
    get: () => secret,
    set: (value) => (secret = value),
  };
}
const safe = secretHolder();
console.log(safe.get()); // "hidden!"
safe.set("new secret");
console.log(safe.get()); // "new secret"
```

> `secret` is inaccessible directly—only through exposed methods.

---

Closures are the stealth ninjas of JavaScript—quietly powerful and everywhere. Want to venture into currying or peek into the prototype chain next? Let’s level up 🧙‍♂️✨

```

```
