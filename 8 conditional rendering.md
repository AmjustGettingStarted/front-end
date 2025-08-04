# 🌗 Conditional Rendering in React

## 💡1. How Do You Implement Conditional Rendering?

**Conditional rendering** means displaying components or elements based on certain conditions. React handles this by letting you use standard JavaScript logic (like `if`, ternary operators, logical `&&`, or switch statements) inside JSX.

---

## 🧰 2. Different Ways to Conditionally Render in React

Here are the most common methods:

### 1️⃣ `if` Statement (Outside JSX)

```jsx
function Greeting({ isLoggedIn }) {
  if (isLoggedIn) {
    return <h1>Welcome back!</h1>;
  }
  return <h1>Please sign in.</h1>;
}
```
