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

## 6. Difference between Virtual DOM and Real DOM

**Real DOM:**

- Updates are slow.
- Directly updates the UI.

**Virtual DOM:**

- React’s in-memory representation of the UI.
- Compares old vs new (diffing) and updates real DOM efficiently.

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
