# React Hooks — Functional Components

---

## 1️⃣ What are React hooks?

**Answer:**  
React Hooks are special functions that let you “hook into” React features like state and lifecycle from **functional components** without needing to write class components.

🎯 They allow developers to:

- Add state
- Use side effects
- Access context
- Handle performance optimizations  
  ...all in a cleaner, more modular way.

Introduced in React 16.8, Hooks revolutionized functional component development.

---

## 2️⃣ What is the `useState` hook?

**Answer:**  
`useState` enables you to add state variables to functional components.

🧠 Syntax:

```jsx
const [count, setCount] = useState(0);
```

- `count` is the state value.
- `setCount` is the updater function.
- `0` is the initial value.

🔄 Updating state:

```jsx
setCount(count + 1);
```

---

## 3️⃣ What is the `useEffect` hook?

**Answer:**  
`useEffect` lets you perform **side effects** — like fetching data, timers, or directly manipulating the DOM — after render.

🎯 Basic usage:

```jsx
useEffect(() => {
  document.title = `You clicked ${count} times`;
}, [count]); // Runs only when `count` changes
```

📌 If the dependency array is empty (`[]`), the effect runs once on mount.

---

## 4️⃣ Can you use state in functional components? How?

**Answer:**  
Yes! That’s the beauty of Hooks.

✅ You use the `useState` hook like this:

```jsx
const [user, setUser] = useState(null);
```

🛠️ You can have multiple independent state values in one component:

```jsx
const [name, setName] = useState("");
const [age, setAge] = useState(0);
```

---

## 5️⃣ What are the rules of hooks?

**Answer:**  
🔒 Hooks have some important rules to ensure predictable behavior:

1. **Only call hooks at the top level** — Don’t use them inside loops, conditions, or nested functions.
2. **Only call hooks from React functions** — They work in functional components and custom hooks, not regular JS functions or classes.
3. **Use the correct naming convention** — Custom hooks should start with `use` (e.g., `useAuth`).
4. **Dependency array discipline** — Ensure you list all required dependencies in `useEffect`, `useCallback`, etc.

🔍 React has a built-in [lint plugin](https://reactjs.org/docs/hooks-rules.html) to catch violations of these rules.

---
