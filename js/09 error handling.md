# 8️⃣ Error Handling in JavaScript

### 1. How Does JavaScript Handle Errors?

💥 JavaScript uses **exceptions** to handle runtime errors. When an error occurs, it "throws" an exception which can be "caught" using `try...catch`. If uncaught, the error halts script execution and may log a stack trace in the console.

> This mechanism helps handle unpredictable failures like missing data, failed network requests, or incorrect inputs.

---

### 2. Difference Between `try`, `catch`, and `finally`

| Block     | Purpose                                     | Runs When?                       |
| --------- | ------------------------------------------- | -------------------------------- |
| `try`     | Contains code that might throw an error     | Always                           |
| `catch`   | Handles any error that occurs in `try`      | Only if error is thrown in `try` |
| `finally` | Executes cleanup code, regardless of errors | Always (error or no error)       |

📌 Example:

```javascript
try {
  let result = riskyOperation();
} catch (err) {
  console.error("Oops!", err.message);
} finally {
  console.log("Cleaning up...");
}
```

---

### 3. Common JavaScript Errors

| Error Type       | Description                                      |
| ---------------- | ------------------------------------------------ |
| `ReferenceError` | Accessing a variable that doesn't exist          |
| `TypeError`      | Wrong data type used (e.g. calling non-function) |
| `SyntaxError`    | Invalid JavaScript syntax                        |
| `RangeError`     | A value outside the allowed range                |
| `EvalError`      | Issues with `eval()` function                    |
| `URIError`       | Incorrect usage of URI handling functions        |

> Most common ones are `ReferenceError` and `TypeError` in development.

---

### 4. How to Throw Custom Errors

Use the `throw` keyword to create your own errors:

```javascript
function checkAge(age) {
  if (age < 18) {
    throw new Error("Must be 18 or older");
  }
  return true;
}
```

🎯 You can also create custom error classes:

```javascript
class ValidationError extends Error {
  constructor(message) {
    super(message);
    this.name = "ValidationError";
  }
}
throw new ValidationError("Invalid input!");
```

---
