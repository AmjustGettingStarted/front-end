# Props and State

---

## 1️⃣ What are props in React?

**Answer:**  
Props (short for "properties") are **read-only inputs** that allow data to be passed from **parent components to child components**. They help customize and configure components, making them reusable.

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

---

## 2️⃣ How do props differ from state?

| Feature    | Props                         | State                        |
| ---------- | ----------------------------- | ---------------------------- |
| Ownership  | Passed from parent            | Managed within component     |
| Mutability | Immutable (read-only)         | Mutable (can be updated)     |
| Purpose    | Configuration/input data      | Internal data management     |
| Access     | `this.props` or function args | `useState()` or `this.state` |

Props define **how a component behaves externally**, while state tracks **internal changes** and interactions.

---

## 3️⃣ What is state in React?

**Answer:**  
State is a built-in React object used to store **dynamic data** that affects how a component renders or behaves. It's **mutable** and typically changes due to user actions, API calls, or internal logic.

```jsx
const [count, setCount] = useState(0);
```

In class components:

```jsx
this.state = { count: 0 };
```

---

## 4️⃣ How do you update state in a React component?

**Answer:**  
In **functional components**, use the `useState` hook:

```jsx
const [count, setCount] = useState(0);
setCount(count + 1);
```

In **class components**, use `setState()`:

```jsx
this.setState({ count: this.state.count + 1 });
```

React re-renders the component automatically when state updates.

---

## 5️⃣ Can you modify props directly? Why or why not?

**Answer:**  
❌ No — you **should never modify props directly**.

Props are **immutable** by design. They're controlled by the **parent component**, ensuring a one-way data flow. Changing props inside a child breaks React’s data integrity and may cause bugs or rendering issues.

Instead, to affect parent state, use **callback functions** passed as props:

```jsx
<ChildComponent onUpdate={handleChange} />
```

---

## 6️⃣ How Does React Handle Re-renders?

React efficiently manages re-renders using a mix of smart comparisons, virtual DOM techniques, and component-level optimizations.

---

## ⚙️ Core Re-rendering Process

1. **Trigger**

   - A component re-renders when:
     - Its `state` changes
     - Its `props` change
     - Its parent re-renders

2. **Virtual DOM Update**

   - React creates a new virtual DOM snapshot to compare with the previous one.

3. **Diffing Algorithm**

   - React compares the new and old virtual DOMs using its **reconciliation** process.
   - Only the changed parts of the UI are updated — not the whole page.

4. **Efficient Real DOM Update**
   - After detecting differences, React updates the **actual DOM** selectively, improving performance.

---

## 📦 Optimization Techniques

- **`React.memo()`**  
  Prevents unnecessary re-renders of functional components by memoizing them.

- **`PureComponent`**  
  In class components, `React.PureComponent` automatically handles shallow comparison of `props` and `state`.

- **Key Prop in Lists**  
  Ensures stable identity for list items to prevent unnecessary re-renders.

---
