# Event Handling

## 1️⃣ How do you handle events in React?

**Answer:**  
React handles events similarly to DOM events in HTML, but with some key differences in syntax and approach.

🧪 Example of handling a click event in a functional component:

```jsx
function MyButton() {
  const handleClick = () => {
    alert("Button clicked!");
  };

  return <button onClick={handleClick}>Click Me</button>;
}
```

✅ Key points:

- Use **camelCase** for event names (e.g., `onClick`, `onChange`)
- Pass **function references**, not strings (no quotes like `"handleClick()"`)
- Events are objects of type `SyntheticEvent`, which normalize behavior across browsers

---

## 2️⃣ What is the difference between handling events in HTML vs. React?

| Feature         | HTML                               | React                                                |
| --------------- | ---------------------------------- | ---------------------------------------------------- |
| Event Syntax    | `<button onclick="doSomething()">` | `<button onClick={doSomething}>`                     |
| Code Location   | Inline JavaScript string           | JS function inside component                         |
| Event Object    | Native DOM Event                   | SyntheticEvent wrapper                               |
| Prevent Default | `event.preventDefault()`           | Same, but applied to SyntheticEvent                  |
| Binding Context | Not automatic                      | Arrow functions or `bind()` may be needed for `this` |

> 📌 Summary:
> React event handling uses **JavaScript functions directly**, not string handlers. It also ensures consistent cross-browser behavior through its **SyntheticEvent system**.

---
