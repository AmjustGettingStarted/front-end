# React Lifecycle Methods (Class Components)

---

## 1️⃣ What are React lifecycle methods?

**Answer:**  
React lifecycle methods are special functions that get triggered at different phases of a component’s existence. They help developers hook into and manage rendering behavior, side effects, data fetching, DOM updates, and cleanup actions in **class components**.

The lifecycle has three primary phases:

- **Mounting** – Component is being added to the DOM.
- **Updating** – Component re-renders due to state/prop changes.
- **Unmounting** – Component is being removed from the DOM.

---

## 2️⃣ What is the purpose of `componentDidMount()`?

**Answer:**  
`componentDidMount()` is invoked **once**, immediately after the component is mounted (inserted into the DOM).

🛠️ It’s commonly used for:

- Fetching data from APIs
- Setting up subscriptions or timers
- Triggering animations or DOM manipulations

```jsx
componentDidMount() {
  fetchData().then(data => this.setState({ data }));
}
```

---

## 3️⃣ What is the difference between `componentDidUpdate()` and `shouldComponentUpdate()`?

| Feature               | `shouldComponentUpdate()`      | `componentDidUpdate()`                |
| --------------------- | ------------------------------ | ------------------------------------- |
| Timing                | Before re-rendering            | After re-rendering                    |
| Purpose               | Prevent unnecessary re-renders | Act on changes (e.g., fetch new data) |
| Return Value          | `true` or `false`              | No return value                       |
| Access to Props/State | Yes (next props/state)         | Yes (prev props/state)                |
| Use Case              | Performance optimization       | Side effects after DOM update         |

---

Here’s a comprehensive breakdown of the **React component lifecycle** in both **class** and **functional components**, formatted in Markdown for clarity and structure:

---

# 🧬 React Component Lifecycle

React components go through a series of phases during their existence. These phases are:

- **Mounting**: Component is created and inserted into the DOM.
- **Updating**: Component re-renders due to changes in props or state.
- **Unmounting**: Component is removed from the DOM.

---

## 🏛️ Class Components Lifecycle

Class components use **lifecycle methods** to hook into these phases.

 ### 1. Mounting Phase

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
    console.log("Constructor called");
  }

  static getDerivedStateFromProps(props, state) {
    // Sync state with props
    return props.value !== state.value ? { value: props.value } : null;
  }

  componentDidMount() {
    console.log("Component mounted");
    // Fetch data or set up subscriptions
  }

  render() {
    return <h1>Hello, React Lifecycle!</h1>;
  }
}
```

 ### 2. Updating Phase

```jsx
shouldComponentUpdate(nextProps, nextState) {
  // Optimize performance
  return nextProps.value !== this.props.value;
}

getSnapshotBeforeUpdate(prevProps, prevState) {
  // Capture DOM info before update
  return null;
}

componentDidUpdate(prevProps, prevState, snapshot) {
  console.log("Component updated");
  // Perform side effects
}
```

 ### 3. Unmounting Phase

```jsx
componentWillUnmount() {
  console.log("Component will unmount");
  // Clean up timers, subscriptions
}
```

> 📘 Class lifecycle methods offer fine-grained control over rendering and side effects.

---

## ⚛️ Functional Components Lifecycle (with Hooks)

Functional components use **React Hooks** to manage lifecycle behavior.

### ### 1. Mounting Phase

```jsx
import React, { useState, useEffect } from "react";

function MyComponent() {
  const [data, setData] = useState(null);

  useEffect(() => {
    console.log("Component mounted");
    fetch("/api/data")
      .then(res => res.json())
      .then(setData);
  }, []); // Empty array = run once on mount

  return <h1>{data}</h1>;
}
```

 ### 2. Updating Phase

```jsx
useEffect(() => {
  console.log("Component updated due to 'data' change");
  // Perform side effects on update
}, [data]); // Runs when 'data' changes
```

### 3. Unmounting Phase

```jsx
useEffect(() => {
  const timer = setInterval(() => console.log("Tick"), 1000);

  return () => {
    clearInterval(timer);
    console.log("Component will unmount");
  };
}, []);
```

> 🧠 Functional components are simpler and more concise, and Hooks like `useEffect` and `useState` allow lifecycle control without classes.

---

## 🔍 Comparison Table

| Phase       | Class Component Method         | Functional Component Hook         |
|-------------|-------------------------------|-----------------------------------|
| Mounting    | `componentDidMount()`         | `useEffect(() => {}, [])`         |
| Updating    | `componentDidUpdate()`        | `useEffect(() => {}, [deps])`     |
| Unmounting  | `componentWillUnmount()`      | `useEffect(() => { return () => {} }, [])` |

---


