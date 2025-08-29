# JavaScript Coding Questions (With Examples)

### 1️⃣ Reverse a String

#### Q: How do you reverse a string in code?

```javascript
function reverseString(str) {
  return str.split("").reverse().join("");
}
console.log(reverseString("hello"));
// "olleh"
```

Explanation:

> `str.split("")` converts the string into an array of characters.  
> `.reverse()` reverses the array.  
> `.join("")` joins the array back into a string.

---

### 2️⃣ Find the Largest Number in an Array

#### Q: How do you find the largest number in an array in programming?

```javascript
function findMax(arr) {
  return Math.max(...arr);
}
console.log(findMax([1, 5, 3, 9, 2])); // 9
```

> You can also use `reduce()` if you're avoiding spread syntax.

#### Using reduce()

```javascript
function findMax(arr) {
  return arr.reduce((max, current) => Math.max(max, current), -Infinity);
}
console.log(findMax([1, 5, 3, 9, 2])); // 9
```

> `arr.reduce(...): This method iterates through the array, applying a function to accumulate a single result.`

> ` (max, current) => Math.max(max, current): For each element, it compares the current maximum (max) with the current value (current) and keeps the larger one.`

> `Infinity: This is the initial value for max, ensuring that even negative numbers in the array will be considered.`

---

### 3️⃣ Check for Palindrome

#### Q. Write a function to determine whether a given string is a palindrome.

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

#### Q. Print numbers 1–100. If divisible by 3 → “Fizz”, by 5 → “Buzz”, by both → “FizzBuzz”:

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

#### Q. Write a function to calculate the factorial of a non-negative integer n.

```javascript
function factorial(n) {
  if (n <= 1) return 1;
  return n * factorial(n - 1);
}
console.log(factorial(5)); // 120
```

> Base case prevents infinite recursion. Works for small `n`.

> 🔁 Recursive Logic
> The function calls itself with a smaller value each time: factorial(n - 1)

The base case is if(n <= 1), which stops the recursion.

---

### 6. Write a simple functional component that displays a list of names

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

### 7. How would you create a button that toggles text on click?

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

### 8 What will be the output of the following code and why?

```js
var x = 10;
function foo() {
  console.log(x);
  var x = 20;
}
foo();
```

> `Output: undefined due to variable hoisting inside the function scope.`
>
> - Variable declarations with var are hoisted inside functions, giving locals priority over globals, but only declarations, not assignments.
> - So, console.log(x) inside foo logs undefined, not the outer value.`

---

### 9.Explain the output order in this async code:

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

> `Output order: C, A, D, B due to event loop and async await behavior.`

---

### 10. Remove Duplicates from an Array

```js
const arr = [1, 2, 2, 3, 4, 4, 5];
const unique = [...new Set(arr)];
console.log(unique); // [1, 2, 3, 4, 5]
```

---

### 11. Debounce Function

```js
function debounce(fn, delay) {
  let timeout;
  return (...args) => {
    clearTimeout(timeout);
    timeout = setTimeout(() => fn(...args), delay);
  };
}
```

---

### 12 CLone and Object

```js
const obj = { a: 1, b: 2 };
const clone = { ...obj };
console.log(clone); // { a: 1, b: 2 }
```

---

### 13 Shuffle an Array (Fisher-Yates)

```js
function shuffle(array) {
  for (let i = array.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [array[i], array[j]] = [array[j], array[i]];
  }
  return array;
}
```

---
