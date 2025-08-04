# 🚦 React Router

---

## 1️⃣ What Is React Router?

**React Router** is a library that enables navigation between different components in a React application without refreshing the page.

🔍 Why it's useful:

- Creates **single-page applications (SPAs)**
- Enables dynamic routing and **URL-based navigation**
- Avoids full page reloads for smoother UX

It handles client-side routing by mapping URL paths to React components.

---

## 2️⃣ How Do You Implement Routing in a React App?

Here’s the basic setup using **React Router v6+**:

### 🧪 Steps to Implement Routing:

#### 🔹 Step 1: Install React Router

```bash
npm install react-router-dom
```

#### 🔹 Step 2: Import Required Components

```jsx
import { BrowserRouter, Routes, Route } from "react-router-dom";
```

#### 🔹 Step 3: Define Routes

```jsx
function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </BrowserRouter>
  );
}
```

Each `Route` matches a URL path to a component. `BrowserRouter` wraps the app to enable routing capabilities.

---

## 3️⃣ Bonus: Navigation Links

Use `Link` to navigate without page reloads:

```jsx
import { Link } from "react-router-dom";

function Navbar() {
  return (
    <nav>
      <Link to="/">Home</Link> |<Link to="/about">About</Link> |
      <Link to="/contact">Contact</Link>
    </nav>
  );
}
```
