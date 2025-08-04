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
