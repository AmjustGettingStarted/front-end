# 🔹 **CSS**

### 1. **What is CSS?**

**Answer:** CSS (Cascading Style Sheets) is used to **style and layout** HTML elements, including colors, fonts, spacing, and positioning.

---

### 2. **What are the different types of CSS?**

**Answer:**

1. **Inline CSS** – style written directly in the HTML element using `style=""`.
2. **Internal CSS** – style written inside a `<style>` tag within the `<head>`.
3. **External CSS** – style written in a separate `.css` file and linked using `<link>`.

---

### 3. **What is the difference between `id` and `class` in CSS?**

**Answer:**

- `id` is **unique**, used once per page (`#id`).
- `class` is **reusable**, used on multiple elements (`.class`).

---

### 4. **What is the box model in CSS?**

**Answer:** The box model describes the layout of HTML elements:

```
[ Margin ]
[ Border ]
[ Padding ]
[ Content ]
```

---

### 5. **What are pseudo-classes in CSS?**

**Answer:** They define the special state of an element. Examples:

- `:hover` – when a user hovers over an element.
- `:first-child`, `:last-child`, `:nth-child()`.

---

### 6. **What is the difference between `relative`, `absolute`, and `fixed` positioning?**

**Answer:**

- `relative`: Moves relative to its normal position.
- `absolute`: Positioned relative to the nearest positioned ancestor.
- `fixed`: Stays in the same place relative to the viewport.

---

### 7. **What is specificity in CSS?**

**Answer:** Specificity determines which CSS rule is applied when multiple rules target the same element.
Hierarchy:

```
Inline styles > IDs > Classes/Pseudo-classes > Elements
```

---

### 8. **How do you link an external CSS file to an HTML document?**

**Answer:**

```html
<link rel="stylesheet" href="style.css" />
```

---

### 9. **What is the difference between `em`, `rem`, and `px`?**

**Answer:**

- `px`: Fixed pixel size.
- `em`: Relative to the font size of the parent.
- `rem`: Relative to the font size of the root element (`<html>`).

---

### 10. **What is the difference between `visibility: hidden` and `display: none`?**

**Answer:**

- `visibility: hidden` hides the element **but takes up space**.
- `display: none` **removes** the element from the layout flow.

---

## 🔹 **Intermediate CSS Questions**

### 11. **What is Flexbox in CSS?**

**Answer:** A layout module that makes it easy to design flexible, responsive layout structures.

---

### 12. **What is the difference between `max-width` and `min-width`?**

**Answer:**

- `max-width`: Sets the **maximum** width an element can be.
- `min-width`: Sets the **minimum** width.

---

### 13. **What is the use of `z-index` in CSS?**

**Answer:** It controls the **stacking order** of overlapping elements. Higher `z-index` means it will appear on top.

---

### 14. **How do you apply the same style to multiple elements?**

**Answer:**

```css
h1,
h2,
p {
  color: blue;
}
```

---

### 15. **What is a media query in CSS?**

**Answer:** Media queries allow CSS to be applied conditionally based on screen size, resolution, etc.

```css
@media (max-width: 768px) {
  body {
    font-size: 14px;
  }
}
```

---

### 16. **What are pseudo-elements in CSS?**

**Answer:** They let you style parts of an element.
Examples:

- `::before`, `::after`

```css
p::before {
  content: "→ ";
}
```

---

### 17. **How do you center a div horizontally and vertically?**

**Answer:**
Using Flexbox:

```css
.parent {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---

### 18. **What is the difference between `static` and `relative` position in CSS?**

**Answer:**

- `static` is the default position (no offset applied).
- `relative` allows the element to move relative to its normal position.

---

### 19. **What is a CSS preprocessor?**

**Answer:** A tool (like **SASS** or **LESS**) that extends CSS with variables, mixins, nesting, etc., and compiles it into standard CSS.

---

### 20. **What is the difference between inline, block, and inline-block elements?**

| Property     | Inline         | Block      | Inline-block |
| ------------ | -------------- | ---------- | ------------ |
| Width/Height | Not applicable | Can be set | Can be set   |
| Layout       | Same line      | New line   | Same line    |

---
