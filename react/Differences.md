# ReactJS - Frequently Asked "Difference Between" Questions

## 1. Difference between Class Component and Functional Component

**Class Component:**

- Uses ES6 classes.
- Can use lifecycle methods directly.
- Uses `this` keyword.
- State is managed via `this.state`.

**Functional Component:**

- Uses plain JavaScript functions.
- Hooks (like `useState`, `useEffect`) are used for side effects and state.
- No `this` keyword.
- Simpler and preferred in modern React.

---

## 2. Difference between State and Props

**Props:**

- Passed from parent to child.
- Immutable (read-only).
- Used for component configuration.

**State:**

- Managed within the component.
- Mutable (can be updated using `setState` or `useState`).
- Used to store local data and manage behavior.

---

## 3. Difference between useEffect and componentDidMount

**componentDidMount (Class):**

- Lifecycle method that runs once after the component mounts.

**useEffect (Hook):**

- Can replicate multiple lifecycle behaviors (mount, update, unmount).
- Can run on every render or just once, depending on the dependency array.

---

## 4. Difference between Controlled and Uncontrolled Components

**Controlled Component:**

- Form data is handled by React state.
- `value` and `onChange` props are required.

**Uncontrolled Component:**

- Form data is handled by the DOM.
- Uses refs to access form values.

---

## 5. Difference between useState and useRef

**useState:**

- Triggers re-render when state changes.
- Used for reactive data.

**useRef:**

- Stores mutable value without causing re-render.
- Useful for accessing DOM elements or persistent values.

---

## 6️⃣ Difference Between Virtual DOM and Real DOM

> The Virtual DOM acts as a performance optimization layer that minimizes direct manipulation of the Real DOM, making UI updates faster and smoother.

| Feature              | Real DOM                                         | Virtual DOM                            |
| -------------------- | ------------------------------------------------ | -------------------------------------- |
| 🚀 Performance       | Slower due to direct updates                     | Faster with optimized batch updates    |
| 🧠 Structure         | Actual browser DOM                               | In-memory abstraction of the real DOM  |
| 🔄 Update Mechanism  | Updates entire UI on changes                     | Uses diffing to find minimal changes   |
| 🛠️ Manipulation      | Direct DOM API (e.g., `document.getElementById`) | Managed by React internally            |
| 🔁 Re-render Trigger | Manual or via native DOM triggers                | Triggered by React state/props changes |
| 🌐 Used By           | All web pages                                    | Mostly in frameworks like React        |

---

## 7. Difference between React and React Native

**React:**

- Used for building web applications.
- Renders to the browser DOM.

**React Native:**

- Used for building mobile applications (iOS, Android).
- Renders to native mobile UI components.

---

## 8. Difference between React Fragment and a Div Wrapper

**React Fragment (`<></>` or `<React.Fragment>`):**

- Doesn’t create extra DOM nodes.
- Useful for grouping children without adding extra markup.

**Div Wrapper (`<div>`):**

- Adds an actual node to the DOM.
- Can affect layout/styles unintentionally.

---

## 9. Difference between useEffect and useLayoutEffect

**useEffect:**

- Runs after paint (non-blocking).
- Good for data fetching, event listeners, etc.

**useLayoutEffect:**

- Runs synchronously **before** the browser paints.
- Used when you need to measure DOM before display.

---

## 10. Difference between key and ref in React

**Key:**

- Used in lists to identify elements uniquely.
- Helps React optimize re-rendering.

**Ref:**

- Provides direct access to a DOM element or component instance.
- Used for focus, text selection, or triggering animations.

---

## 11. Difference between setState and forceUpdate

**setState:**

- Updates state and re-renders the component.
- Asynchronous.
- Should be used in normal scenarios to change state.

**forceUpdate:**

- Forces a re-render without changing the state.
- Rarely used and considered an anti-pattern.

---

## 12. Difference between Mounting and Updating Phase

**Mounting:**

- Component is being created and inserted into the DOM.
- Lifecycle: `constructor` → `render` → `componentDidMount`.

**Updating:**

- Component is being re-rendered due to prop/state changes.
- Lifecycle: `shouldComponentUpdate` → `render` → `componentDidUpdate`.

---

## 13. Difference between Presentational and Container Components

**Presentational Components:**

- Focus on how things look (UI).
- Receive data via props.
- Typically functional components.

**Container Components:**

- Focus on how things work (logic, state).
- May use state and lifecycle methods.
- Often class components or use hooks.

---

## 14. Difference between React Context and Redux

**React Context:**

- Built-in way to pass data deeply without prop drilling.
- Good for global themes, language, user info.

**Redux:**

- State management library.
- Better for large-scale applications with complex state logic.

---

## 15. Difference between Inline Styling and CSS Modules

**Inline Styling:**

- Defined directly in component using style objects.
- No scope — global by default.

**CSS Modules:**

- Scoped locally by default.
- Helps avoid class name collisions.

---

## 16. Difference between useCallback and useMemo

**useCallback:**

- Memoizes a **function**.
- Prevents unnecessary re-creations of functions.

**useMemo:**

- Memoizes the **result of a function**.
- Prevents unnecessary recalculations.

---

## 17. Difference between React.memo and useMemo

**React.memo:**

- Higher Order Component to memoize entire functional components.
- Prevents re-render if props haven't changed.

**useMemo:**

- Hook to memoize values (not components).
- Used inside functional components.

---

## 18. Difference between BrowserRouter and HashRouter

**BrowserRouter:**

- Uses HTML5 history API.
- Cleaner URLs (e.g., `/home`).

**HashRouter:**

- Uses hash in URL (e.g., `/#/home`).
- Useful for static file hosting (GitHub Pages).

---

## 19. Difference between Context API and Props

**Context API:**

- Provides a way to share values globally without props drilling.
- Good for theming, localization, auth, etc.

**Props:**

- Passed from parent to child only.
- Best for one-way, explicit data flow.

---

## 20. Difference between JavaScript and JSX

**JavaScript:**

- Standard programming language.

**JSX:**

- Syntax extension that looks like HTML inside JavaScript.
- Gets compiled to `React.createElement`.

---
