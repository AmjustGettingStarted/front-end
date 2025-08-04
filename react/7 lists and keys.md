# Lists and Keys

---

## 1️⃣ How do you render a list of items in React?

**Answer:**  
To render a list in React, use JavaScript’s `map()` function to iterate through an array and return a component or JSX element for each item.

🧪 Example:

```jsx
const fruits = ["Apple", "Banana", "Cherry"];

function FruitList() {
  return (
    <ul>
      {fruits.map((fruit, index) => (
        <li key={index}>{fruit}</li>
      ))}
    </ul>
  );
}
```

📌 Each item is rendered as a `<li>`, and React expects a unique `key` for each child in a list.

---

## 2️⃣ Why are keys important in React lists?

**Answer:**  
**Keys** help React identify which items have changed, been added, or removed. This allows React to:

- ✅ Efficiently update the DOM
- ⚡ Avoid unnecessary re-renders
- 🧠 Maintain UI performance and consistency

🛑 Without proper keys, React may re-render entire sections or misplace elements during updates.

💡 Ideal keys:

- Use **unique and stable identifiers** (e.g., item ID from a database)
- Avoid using indexes as keys unless list order won’t change

🧪 Example of a better key:

```jsx
{
  users.map((user) => <li key={user.id}>{user.name}</li>);
}
```

---

## 🔹 What is a List in JavaScript?

In JavaScript, a list usually refers to an **array**—a collection of items stored in a single variable.

🧪 Example:

```js
const fruits = ["apple", "banana", "cherry"];
```

You can loop through this array using `.map()`, `.forEach()`, or a `for` loop to access or manipulate each item.

---

## 🔹 What is a List in React?

In React, a list is often rendered using `.map()` to dynamically create components from an array of data.

🧪 Example:

```jsx
const fruits = ["apple", "banana", "cherry"];

function FruitList() {
  return (
    <ul>
      {fruits.map((fruit, index) => (
        <li key={index}>{fruit}</li>
      ))}
    </ul>
  );
}
```

Each `<li>` is generated from the array. React needs a **`key`** for each item to optimize rendering.

---

## 🔸 What is a Key in React?

**Keys** are special attributes used by React to identify elements in a list. They help React track changes and update the DOM efficiently.

### ✅ Why are Keys Important?

- They allow React to **know which items changed**
- They help prevent **unnecessary re-renders**
- They maintain **UI stability and performance**

🧪 Good Practice:

```jsx
const users = [
  { id: 101, name: "Alice" },
  { id: 102, name: "Bob" },
];

{
  users.map((user) => <li key={user.id}>{user.name}</li>);
}
```

---
