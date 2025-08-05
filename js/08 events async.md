# 1. What is the Event Loop?

🔁 The **event loop** is the engine that drives asynchronous behavior in JavaScript. It continuously checks the **call stack** and the **task queue**, allowing non-blocking operations like timers, network calls, and user input to execute efficiently.

> Think of it as a traffic controller—executing synchronous code and scheduling asynchronous tasks.

---

### 2. What is the Call Stack?

📚 The **call stack** is a LIFO (Last In, First Out) data structure that tracks function calls:

```javascript
function greet() {
  console.log("Hello");
}
greet(); // pushed to stack → executed → popped off
```

Each time a function is invoked, it’s added to the stack. Once completed, it’s removed.

> If the stack gets too deep (e.g., infinite recursion), you’ll hit a “stack overflow”!

---

### 3. Difference between `setTimeout`, `setInterval`, and `clearInterval`

| Method            | Purpose                  | Behavior                           |
| ----------------- | ------------------------ | ---------------------------------- |
| `setTimeout()`    | Delay execution once     | Executes after specified time      |
| `setInterval()`   | Repeated execution       | Executes continuously per interval |
| `clearInterval()` | Stops a running interval | Requires interval ID               |

📌 Example:

```javascript
const id = setInterval(() => console.log("Tick"), 1000);
clearInterval(id); // stops the ticking
```

---

### 4. Microtasks vs Macrotasks

| Task Type  | Examples                           | Execution Priority |
| ---------- | ---------------------------------- | ------------------ |
| Microtasks | `Promise.then`, `MutationObserver` | ✅ Higher priority |
| Macrotasks | `setTimeout`, `setInterval`, I/O   | ❌ Lower priority  |

> Microtasks run right **after** the current operation and **before** the next render. They’re queued in the **microtask queue** and starve macrotasks if overloaded!

---

### 5. What is a Promise? `.then()`, `.catch()`, `.finally()`

💬 A **Promise** represents an asynchronous result—either **resolved** or **rejected**.

```javascript
fetch("data.json")
  .then((res) => res.json()) // on success
  .catch((err) => console.error(err)) // on error
  .finally(() => console.log("Done")); // always runs
```

| Method       | Role                       |
| ------------ | -------------------------- |
| `.then()`    | Handles successful outcome |
| `.catch()`   | Handles errors             |
| `.finally()` | Runs regardless of result  |

---

### 6. What are `async/await` and how do they work?

✨ `async/await` is a syntax sugar over promises for writing **clean, readable async code**:

```javascript
async function fetchData() {
  try {
    const res = await fetch("data.json");
    const data = await res.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}
```

- `await` **pauses** until the Promise resolves.
- Must be used **inside an `async` function.**

> It makes asynchronous flows look synchronous—no more nesting `.then()` chains!

---
