# 5️⃣ DOM Manipulation in JavaScript

### 1. What is the DOM?

🌳 The **DOM (Document Object Model)** is a programming interface for HTML and XML documents. It represents the page so that programs can manipulate the structure, style, and content.

> Think of it as a **tree-like structure** where each node is an element, attribute, or text.

---

### 2. How do you select elements in the DOM?

| Method                   | Description                              | Example                                   |
| ------------------------ | ---------------------------------------- | ----------------------------------------- |
| `getElementById`         | Selects by ID (unique)                   | `document.getElementById("header")`       |
| `getElementsByClassName` | Selects elements with class name         | `document.getElementsByClassName("menu")` |
| `getElementsByTagName`   | Selects elements by tag                  | `document.getElementsByTagName("div")`    |
| `querySelector`          | Selects **first** match via CSS selector | `document.querySelector(".btn")`          |
| `querySelectorAll`       | Selects **all** matches via CSS selector | `document.querySelectorAll("p.note")`     |

---

### 3. How do you create and append elements dynamically?

```javascript
const newDiv = document.createElement("div");
newDiv.textContent = "Hello World";
document.body.appendChild(newDiv);
```

> You can also set attributes using `setAttribute()` or style with `.style`.

---

### 4. How do you handle events in JavaScript?

Use `addEventListener` to attach event handlers:

```javascript
const button = document.querySelector(".click-me");
button.addEventListener("click", () => {
  alert("Button clicked!");
});
```

🎯 Supports many events like `click`, `mouseover`, `keydown`, etc.

---

### 5. What is Event Delegation?

Event delegation means attaching a **single event listener** to a parent element instead of multiple children. The listener checks the `event.target` to determine which child triggered the event.

```javascript
document.querySelector("#list").addEventListener("click", (e) => {
  if (e.target.tagName === "LI") {
    console.log("Clicked item:", e.target.textContent);
  }
});
```

> Efficient for dynamic content and fewer listeners!

---

### 6. Difference between `innerHTML`, `textContent`, and `innerText`

| Property      | What It Does                          | HTML Aware | Style Aware |
| ------------- | ------------------------------------- | ---------- | ----------- |
| `innerHTML`   | Gets/sets **HTML content**            | ✅ Yes     | ❌ No       |
| `textContent` | Gets/sets **text without formatting** | ❌ No      | ❌ No       |
| `innerText`   | Gets/sets **visible text only**       | ❌ No      | ✅ Yes      |

📌 Example:

```javascript
element.innerHTML = "<strong>Hello</strong>"; // bold HTML
element.textContent = "<strong>Hello</strong>"; // raw text
element.innerText = "<strong>Hello</strong>"; // depends on visibility
```

---
