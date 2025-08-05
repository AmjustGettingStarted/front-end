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

### 3. What is the difference between `var`, `let`, and `const`?

- `var`: Function-scoped, allows redeclaration, hoisted.
- `let`: Block-scoped, no redeclaration, hoisted (but not initialized).
- `const`: Block-scoped, must be initialized at declaration, value cannot be reassigned.

### 4. What are primitive and non-primitive data types?

- **Primitive**: Immutable values (e.g., `number`, `string`, `boolean`, etc.). Stored directly.
- **Non-primitive**: Complex data structures (e.g., `object`, `array`, `function`) stored by reference.

### 5. How is `==` different from `===`?

- `==` (loose equality): Compares values **after type coercion**.
- `===` (strict equality): Compares both **value and type**. Safer and more predictable.

Example:

```javascript
"5" == 5; // true
"5" === 5; // false
```

### 6. What is hoisting in JavaScript?

Hoisting is JavaScript's behavior of **moving declarations to the top** of their scope before code execution.

- `var` and `function` declarations are hoisted.
- `let` and `const` are hoisted but not initialized—accessing them before declaration throws a ReferenceError.

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

```

Would you like this as a printable cheat sheet or turned into flashcards next? I can also help explain advanced concepts!
```
