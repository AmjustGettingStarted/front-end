# ✅ JavaScript Basics

### 1. What is JavaScript? How is it different from Java?

JavaScript is a lightweight, interpreted scripting language primarily used to add interactive behaviors to web pages. Despite the similar name, **Java** and **JavaScript** are entirely different:

- Java is a statically typed, compiled language used for building large-scale applications.
- JavaScript is dynamically typed and runs in browsers without compilation, making it ideal for client-side scripting.

---

### 2. What are the different data types in JavaScript?

JavaScript has **8** main data types:

- **Primitive**: `String`, `Number`, `BigInt`, `Boolean`, `undefined`, `Symbol`, and `null`.
- **Non-primitive (reference)**: `Object` (includes arrays, functions, etc.)

---

### 3. What is the difference between `var`, `let`, and `const`?

- `var`: Function-scoped, allows redeclaration, hoisted.
- `let`: Block-scoped, no redeclaration, hoisted (but not initialized).
- `const`: Block-scoped, must be initialized at declaration, value cannot be reassigned.

---

### 4. What are primitive and non-primitive data types?

- **Primitive**: Immutable values (e.g., `number`, `string`, `boolean`, etc.). Stored directly.
- **Non-primitive**: Complex data structures (e.g., `object`, `array`, `function`) stored by reference.

---

### 5. How is `==` different from `===`?

- `==` (loose equality): Compares values **after type coercion**.
- `===` (strict equality): Compares both **value and type**. Safer and more predictable.

Example:

```javascript
"5" == 5; // true
"5" === 5; // false
```

---

### 6. What is hoisting in JavaScript?

Hoisting is JavaScript's behavior of **moving declarations to the top** of their scope before code execution.

- `var` and `function` declarations are hoisted.
- `let` and `const` are hoisted but not initialized—accessing them before declaration throws a ReferenceError.

Sure! Here’s a crisp and precise explanation of **hoisting in JavaScript**:

### 🚀 What Is Hoisting?

**Hoisting** is JavaScript's default behavior of **moving declarations (not initializations)** to the top of the current scope—**before the code runs**.

---

### 🔍 Breakdown by Type

- **`var`**: Declaration is hoisted. Initialized as `undefined`.  
  → You can access it before it's declared, but you'll get `undefined`.

- **`let` / `const`**: Declaration is hoisted, but **not initialized**.  
  → Accessing it before declaration throws a `ReferenceError` due to the **Temporal Dead Zone**.

- **Function declarations**: Entire function (name + body) is hoisted.  
  → You can call the function even before it's defined.

- **Function expressions / arrow functions**: Only the variable name is hoisted—not the function logic.  
  → Accessing them before declaration gives an error.

---

> ### ⚠️ Key Rule: Hoisting **does not move code**, it only shifts **declarations** not assignments.

Sure! Here's a precise explanation of **JavaScript hoisting** using clear examples so you can see how each type behaves in action:

---

### 🧪 Example 1: `var` Hoisting

```javascript
console.log(a); // 👉 Output: undefined
var a = 10;
```

**Why?**  
The `var` declaration is hoisted to the top, but the initialization (`= 10`) is not. So it's as if JavaScript rewrites this as:

```javascript
var a;
console.log(a); // undefined
a = 10;
```

---

### 🧪 Example 2: `let` and `const` Hoisting (with TDZ)

```javascript
console.log(b); // ❌ ReferenceError
let b = 20;
```

**Why?**  
`let` is hoisted, but it’s in the **Temporal Dead Zone** until the line `let b = 20;` is reached. Accessing it before that throws an error.

The same happens with `const`:

```javascript
console.log(c); // ❌ ReferenceError
const c = 30;
```

---

### 🧪 Example 3: Function Declaration Hoisting

```javascript
greet(); // 👉 Output: "Hello!"

function greet() {
  console.log("Hello!");
}
```

**Why?**  
Function **declarations** are fully hoisted—including the code block—so you can call them before they appear in code.

---

### 🧪 Example 4: Function Expression Hoisting

```javascript
sayHi(); // ❌ TypeError: sayHi is not a function

var sayHi = function () {
  console.log("Hi!");
};
```

> **Why?**  
> Only the variable `sayHi` is hoisted (initialized as `undefined`). The function isn't yet assigned when it's called.

---

> ### 🎓 Final Insight: Hoisting is like JavaScript doing a **silent pre-processing step**, where it lifts declarations up but leaves assignments and initializations where they are.

---

### 7. Explain the concept of scope (global vs local).

- **Global scope**: Variables declared outside any function or block. Accessible throughout the script.
- **Local scope**: Variables declared inside a block or function. Accessible only within that block or function.

### 8. What are template literals in JavaScript?

Template literals (enclosed with backticks `` ` ``) allow:

- Multiline strings
- String interpolation using `${expression}`

Example:

```javascript
const name = "JavaScript";
console.log(`Hello, ${name}!`);
```

### 9. What are truthy and falsy values?

In JavaScript, values are coerced to boolean in conditional contexts.

- **Falsy values**: `false`, `0`, `""`, `null`, `undefined`, `NaN`
- **Truthy values**: Everything else (including `"0"`, `[]`, `{}`)

### 10. How does `typeof` work in JavaScript?

The `typeof` operator returns a string indicating the type of a value.
Examples:

```javascript
typeof 42; // "number"
typeof "hello"; // "string"
typeof null; // "object"   // (a long-standing JS quirk)
typeof []; // "object"
typeof undefined; // "undefined"
```
