# JavaScript Coding Questions (With Examples)

### 1️⃣ Reverse a String

You can reverse a string by splitting it into an array, reversing it, and joining it back:

```javascript
function reverseString(str) {
  return str.split("").reverse().join("");
}
console.log(reverseString("hello")); // "olleh"
```

---

### 2️⃣ Find the Largest Number in an Array

```javascript
function findMax(arr) {
  return Math.max(...arr);
}
console.log(findMax([1, 5, 3, 9, 2])); // 9
```

> You can also use `reduce()` if you're avoiding spread syntax.

---

### 3️⃣ Check for Palindrome

```javascript
function isPalindrome(str) {
  const reversed = str.split("").reverse().join("");
  return str === reversed;
}
console.log(isPalindrome("madam")); // true
console.log(isPalindrome("hello")); // false
```

> Works best with simple strings. For complex checks, normalize casing and strip non-alphanumerics.

---

### 4️⃣ FizzBuzz

Print numbers 1–100. If divisible by 3 → “Fizz”, by 5 → “Buzz”, by both → “FizzBuzz”:

```javascript
for (let i = 1; i <= 100; i++) {
  let output = "";
  if (i % 3 === 0) output += "Fizz";
  if (i % 5 === 0) output += "Buzz";
  console.log(output || i);
}
```

---

### 5️⃣ Factorial Using Recursion

```javascript
function factorial(n) {
  if (n <= 1) return 1;
  return n * factorial(n - 1);
}
console.log(factorial(5)); // 120
```

> Base case prevents infinite recursion. Works for small `n`.

---

Sure! Here's the **Markdown** version with answers for both:

---

## ✅ 6. Write a simple functional component that displays a list of names

```jsx
import React from "react";

const NameList = () => {
  const names = ["Alice", "Bob", "Charlie", "Diana"];

  return (
    <div>
      <h2>List of Names:</h2>
      <ul>
        {names.map((name, index) => (
          <li key={index}>{name}</li> // Always use a unique key in real projects
        ))}
      </ul>
    </div>
  );
};

export default NameList;
```

---

## ✅ 7. How would you create a button that toggles text on click?

```jsx
import React, { useState } from "react";

const ToggleText = () => {
  const [isVisible, setIsVisible] = useState(true);

  const handleToggle = () => {
    setIsVisible(!isVisible);
  };

  return (
    <div>
      <button onClick={handleToggle}>
        {isVisible ? "Hide Text" : "Show Text"}
      </button>

      {isVisible && <p>This is the toggled text!</p>}
    </div>
  );
};

export default ToggleText;
```

---

## 8 What will be the output of the following code and why?

```js
var x = 10;
function foo() {
  console.log(x);
  var x = 20;
}
foo();
```

> Output: undefined due to variable hoisting inside the function scope.

---

## 9.Explain the output order in this async code:

```js
async function asyncFunc() {
  console.log("A");
  await new Promise((resolve) => setTimeout(resolve, 1000));
  console.log("B");
}
console.log("C");
asyncFunc();
console.log("D");
```

> Output order: C, A, D, B due to event loop and async await behavior.

---
