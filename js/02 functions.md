# Functions

## 1️⃣ What Are First-Class Functions?

In JavaScript, **functions are first-class citizens**, which means:

- They can be **assigned to variables**.
- They can be **passed as arguments** to other functions.
- They can be **returned from other functions**.

📌 Example:

```javascript
function greet(name) {
  return `Hello, ${name}`;
}

const sayHello = greet; // assigning function to a variable
console.log(sayHello("Alice")); // Output: Hello, Alice
```

---

## 2️⃣ Function Declaration vs. Function Expression

### 🔹 Function Declaration:

- Defined using the `function` keyword.
- Hoisted: available before its definition in code.

```javascript
function greet() {
  console.log("Hello!");
}
```

### 🔹 Function Expression:

- Assigned to a variable.
- Not hoisted: available only after the assignment.

```javascript
const greet = function () {
  console.log("Hello!");
};
```

📌 Difference:
| Aspect | Declaration | Expression |
|---------------------|------------------------|------------------------|
| Hoisting | ✅ Yes | ❌ No |
| Syntax | Named function | Can be anonymous |
| Usage flexibility | Slightly more limited | Very flexible |

---

## 3️⃣ What Is an Anonymous Function?

An **anonymous function** is a function **without a name**.

📌 Commonly used as function expressions or passed directly as arguments:

```javascript
setTimeout(function () {
  console.log("Executed after delay");
}, 1000);
```

✅ They're great for inline, temporary logic.

---

## 4️⃣ What Is an Arrow Function? How Is It Different?

Introduced in ES6, an **arrow function** uses the `=>` syntax.

### 🔹 Syntax:

```javascript
const greet = (name) => `Hello, ${name}`;
```

### 🔸 Key Differences:

| Feature        | Regular Function            | Arrow Function                       |
| -------------- | --------------------------- | ------------------------------------ |
| `this` binding | Dynamic (depends on caller) | Lexical (inherits from parent scope) |
| Syntax         | Verbose                     | Concise                              |
| Constructor    | Can be used with `new`      | ❌ Cannot be used as constructor     |

⚠️ Arrow functions are not ideal for object methods or callbacks that rely on `this`.

---

## 5️⃣ What Is a Callback Function?

A **callback** is a function passed into another function as an argument, to be **executed later**.

📌 Common in asynchronous operations like API calls, timers, or event handling.

```javascript
function fetchData(callback) {
  setTimeout(() => {
    callback("Data loaded");
  }, 1000);
}

fetchData(function (msg) {
  console.log(msg); // Output: Data loaded
});
```

---

## 6️⃣ What Is IIFE (Immediately Invoked Function Expression)?

An **IIFE** runs **immediately after it's defined**.

### 🔹 Syntax:

```javascript
(function () {
  console.log("IIFE running!");
})();
```

✅ Useful for:

- Avoiding polluting the global scope.
- Creating private scopes.

---

## 7️⃣ Difference Between Synchronous and Asynchronous Functions

### 🔹 Synchronous:

- Executes line by line.
- Blocks further execution until complete.

```javascript
console.log("Step 1");
console.log("Step 2");
```

### 🔹 Asynchronous:

- Allows other code to run while waiting (e.g., API calls, timers).
- Commonly uses **callbacks**, **Promises**, or **async/await**.

```javascript
console.log("Start");
setTimeout(() => {
  console.log("Inside timeout");
}, 1000);
console.log("End");
// Output: Start → End → Inside timeout
```

📌 Async functions enhance performance in I/O-heavy tasks.

---
