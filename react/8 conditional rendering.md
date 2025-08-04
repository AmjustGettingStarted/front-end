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
---
Here’s a detailed explanation of **conditional vs. unconditional rendering in React**, formatted in Markdown for clarity:

---

# 🌗 Conditional vs. Unconditional Rendering in React

## 🔀 Conditional Rendering

Conditional rendering means displaying different UI elements **based on a condition**—like user authentication, data availability, or application state.

### ✅ Common Techniques

```jsx
// 1. If Statement
function Greeting({ isLoggedIn }) {
  if (isLoggedIn) {
    return <h1>Welcome back!</h1>;
  }
  return <h1>Please sign in.</h1>;
}

// 2. Ternary Operator
function Greeting({ isLoggedIn }) {
  return <h1>{isLoggedIn ? "Welcome back!" : "Please sign in."}</h1>;
}

// 3. Logical AND (&&)
function Notification({ hasNotifications }) {
  return <div>{hasNotifications && <p>You have new notifications!</p>}</div>;
}

// 4. Switch Case
function StatusMessage({ status }) {
  switch (status) {
    case 'loading': return <p>Loading...</p>;
    case 'success': return <p>Data loaded!</p>;
    case 'error': return <p>Error occurred.</p>;
    default: return <p>Unknown status</p>;
  }
}
```

> 📌 Conditional rendering is dynamic and adapts the UI based on logic or state.

---

## 🚦 Unconditional Rendering

Unconditional rendering means rendering components or elements **without any condition**. The component always renders the same output regardless of props or state.

### 🧱 Example

```jsx
function WelcomeMessage() {
  return <h1>Welcome to our site!</h1>;
}
```

This component will always render the same message—no logic, no branching.

---

## ⚖️ Comparison Table

| Feature                  | Conditional Rendering                          | Unconditional Rendering                      |
|--------------------------|------------------------------------------------|----------------------------------------------|
| 🔄 Behavior              | Varies based on props/state                    | Always renders the same output               |
| 🧠 Logic Required        | Yes (if, ternary, switch, etc.)                | No logic required                            |
| 🔧 Use Case              | Dynamic UIs, user feedback, data-driven views | Static content, headers, footers, branding   |
| 💡 Example               | `isLoggedIn ? <Welcome /> : <Login />`        | `<h1>Welcome to our site!</h1>`              |

---
