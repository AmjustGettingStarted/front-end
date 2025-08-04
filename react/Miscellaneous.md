# 🧠 Miscellaneous React Interview Questions

## 1️⃣ What is the Virtual DOM?

**Answer:**  
The **Virtual DOM (VDOM)** is an in-memory representation of the actual DOM. React uses it to improve performance by minimizing direct manipulation of the browser’s DOM.

🔍 How it works:

- React creates a virtual copy of the DOM whenever your component renders.
- When a change occurs, React compares the new virtual DOM with the previous one (diffing).
- Only the changed parts are updated in the real DOM — saving time and resources.

---

## 2️⃣ How does React update the DOM?

**Answer:**  
React follows this update flow:

1. **Trigger:** When `state` or `props` change, React re-renders the component.
2. **Diffing:** It compares the updated Virtual DOM with the old one.
3. **Reconciliation:** Finds the minimal set of changes.
4. **Batch Update:** Efficiently updates only affected nodes in the actual DOM.

⚡ Result: Smooth performance even for complex UIs.

---

## 3️⃣ What is lifting state up in React?

**Answer:**  
**Lifting state up** means moving shared state to the closest common parent of two or more components that need access to it.

🧪 Use case:
If two sibling components need the same data (like form input or filter settings), you place that state in their parent and pass it down as props.

```jsx
<Parent>
  <ChildA data={sharedData} />
  <ChildB data={sharedData} />
</Parent>
```

🧠 This prevents duplication and keeps state consistent across components.

---

## 4️⃣ What is the purpose of the `key` prop in React?

**Answer:**  
The `key` prop uniquely identifies elements in a list and helps React determine:

- Which items have changed
- Which have been added or removed

✨ Why it's critical:

- Improves rendering speed
- Maintains UI stability
- Prevents bugs in dynamic lists

Always use **unique, stable keys** (like `id`). Avoid using array indices unless list order never changes.

---

## 5️⃣ How do you pass data between components?

**Answer:**  
There are several ways:

- **Parent to Child:** Use props
  ```jsx
  <Child name="Alex" />
  ```
- **Child to Parent:** Use callback functions passed via props
  ```jsx
  <Child onClick={handleChildEvent} />
  ```
- **Between Siblings:** Lift state up to a common parent, then pass via props
- **Across Tree Levels:** Use **React Context API** or **state management tools** like Redux/Zustand

---

## 6️⃣ What is prop drilling? How can it be avoided?

**Answer:**  
**Prop drilling** occurs when you pass data through multiple nested components that don’t need it, just to reach a deeply nested one.

🎯 Problem:
Makes code harder to manage and scale.

🛡️ How to avoid it:

- Use the **Context API**: Share state globally without passing through intermediate components.
- Adopt tools like **Redux**, **Zustand**, or **Recoil** for centralized state.
- Break UI into smaller, logical containers to reduce unnecessary prop chains.

---
