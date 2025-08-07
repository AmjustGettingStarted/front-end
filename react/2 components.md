# React Components

## 1️⃣ What are components in React?

**Answer:**  
Components are independent, reusable bits of UI in React. They work like JavaScript functions — receiving inputs (called `props`) and returning UI elements using JSX. Every React application is built by combining components.

---

## 2️⃣ What is the difference between functional and class components?

| Feature            | Functional Component        | Class Component                         |
| ------------------ | --------------------------- | --------------------------------------- |
| Syntax             | JavaScript function         | Uses `class` keyword                    |
| State Management   | `useState` hook             | `this.state` object                     |
| Lifecycle Handling | `useEffect` hook            | Traditional lifecycle methods           |
| Boilerplate        | Minimal                     | More verbose                            |
| Performance        | More optimized (with hooks) | Slightly heavier                        |
| Example Syntax     | `function Comp() {}`        | `class Comp extends React.Component {}` |

---

## 3️⃣ How do you create a functional component in React?

**Answer:**  
You can define a functional component using either traditional or arrow syntax:

```jsx
// Traditional syntax
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

// Arrow function syntax
const Greeting = ({ name }) => <h1>Hello, {name}!</h1>;
```

Functional components are concise and support hooks for state and side effects.

---

## 4️⃣ What is a pure component?

**Answer:**  
A **Pure Component** is a React class component that avoids unnecessary re-renders by comparing previous props and state with current ones using shallow comparison. React offers `React.PureComponent` to implement this automatically.

For functional components, you can use `React.memo()`:

```jsx
const MyComponent = React.memo(function MyComponent(props) {
  return <div>{props.value}</div>;
});
```

This ensures the component only re-renders if its props change.

---
