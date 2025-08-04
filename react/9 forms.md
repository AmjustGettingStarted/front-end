## 🧮 React Forms

---

### 1️⃣ How Do You Handle Forms in React?

React forms are controlled via component state using hooks like `useState()`. You track input values and handle events like `onChange` and `onSubmit`.

```jsx
function ContactForm() {
  const [name, setName] = useState("");

  function handleSubmit(e) {
    e.preventDefault();
    console.log("Submitted name:", name);
  }

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        value={name}
        onChange={(e) => setName(e.target.value)}
      />
      <button type="submit">Send</button>
    </form>
  );
}
```

---

### 2️⃣ What Is a Controlled Component?

A **controlled component** keeps its input value in **React state**, making it easy to validate and manipulate.

```jsx
<input type="text" value={name} onChange={(e) => setName(e.target.value)} />
```

- Value is driven by React state (`useState`)
- Ideal for handling validations, conditionals, and user flow

---

### 3️⃣ What Is an Uncontrolled Component?

An **uncontrolled component** uses the native DOM directly via **`ref`**, instead of syncing with React state.

```jsx
const nameRef = useRef();

function handleSubmit(e) {
  e.preventDefault();
  console.log("Name:", nameRef.current.value);
}

<form onSubmit={handleSubmit}>
  <input type="text" ref={nameRef} />
  <button type="submit">Send</button>
</form>;
```

- Simpler but harder to validate and test
- Not ideal for complex forms or dynamic updates

---

### 4️⃣ Controlled vs Uncontrolled — Quick Comparison

| 🧩 Feature      | Controlled Component    | Uncontrolled Component |
| --------------- | ----------------------- | ---------------------- |
| State Source    | React (`useState`)      | Native DOM (`ref`)     |
| Validation Ease | High                    | Low                    |
| Recommended For | Dynamic, reactive forms | Simple or legacy cases |
| Debugging       | Easier                  | Tougher                |

---
