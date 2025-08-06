# 🔹 **Basics HTML**

### 1. **What is HTML?**

**Answer:** HTML (HyperText Markup Language) is the standard language for creating and structuring web pages using elements like headings, paragraphs, links, images, etc.

---

### 2. **What are tags in HTML?**

**Answer:** Tags are the building blocks of HTML. They define elements in a document. For example: `<p>`, `<h1>`, `<a>`, `<div>`.

---

### 3. **What is the difference between HTML and HTML5?**

**Answer:**

- HTML5 is the latest version.
- HTML5 supports new elements like `<article>`, `<section>`, `<audio>`, and `<video>`.
- It has better support for multimedia and APIs (like Geolocation, Web Storage).

---

### 4. **What are semantic tags in HTML5?**

**Answer:** Semantic tags clearly define their meaning in a human- and machine-readable way. Examples:

- `<header>`, `<footer>`, `<article>`, `<section>`, `<nav>`

---

### 5. **What is the difference between block-level and inline elements?**

**Answer:**

- **Block-level:** Starts on a new line and takes up full width (e.g., `<div>`, `<p>`, `<h1>`).
- **Inline:** Doesn’t start on a new line, only takes up as much width as needed (e.g., `<span>`, `<a>`, `<strong>`).

---

## 🔹 **Intermediate HTML Questions**

### 6. **What is the purpose of the `<!DOCTYPE html>` declaration?**

**Answer:** It defines the HTML version and helps browsers render the page correctly.

---

### 7. **How do you insert an image in HTML?**

**Answer:** Using the `<img>` tag:

```html
<img src="image.jpg" alt="Description" />
```

---

### 8. **How can you create a hyperlink in HTML?**

**Answer:**

```html
<a href="https://example.com">Visit Example</a>
```

---

### 9. **What is the use of the `alt` attribute in images?**

**Answer:** It provides alternative text for the image if it cannot be displayed and improves accessibility.

---

### 10. **How do you create a table in HTML?**

**Answer:**

```html
<table>
  <tr>
    <th>Heading 1</th>
    <th>Heading 2</th>
  </tr>
  <tr>
    <td>Data 1</td>
    <td>Data 2</td>
  </tr>
</table>
```

---

## 🔹 **Forms & Input**

### 11. **How do you create a form in HTML?**

**Answer:**

```html
<form action="/submit" method="post">
  <input type="text" name="name" />
  <input type="submit" value="Submit" />
</form>
```

---

### 12. **List some common form input types.**

**Answer:** `text`, `password`, `email`, `checkbox`, `radio`, `submit`, `date`, `file`.

---

### 13. **What is the purpose of the `action` and `method` attributes in a form?**

**Answer:**

- `action`: URL where the form data is sent.
- `method`: HTTP method used to send data (`GET` or `POST`).

---

## 🔹 **Miscellaneous Questions**

### 14. **What is the use of the `<meta>` tag?**

**Answer:** It provides metadata about the HTML document (e.g., charset, viewport settings, SEO-related info).

---

### 15. **What is the difference between `<id>` and `<class>` attributes?**

**Answer:**

- `id`: Unique identifier for a single element.
- `class`: Can be used for multiple elements to apply common styles.

---

### 16. **Can a webpage have multiple `<header>` or `<footer>` tags?**

**Answer:** Yes, each section or article can have its own `<header>` or `<footer>`.

---

### 17. **What is the use of the `<iframe>` tag?**

**Answer:** It is used to embed another HTML page within the current page.

---

### 18. **What is the difference between `<ul>`, `<ol>`, and `<dl>`?**

- `<ul>`: Unordered list.
- `<ol>`: Ordered list.
- `<dl>`: Description list.

---

### 19. **How can you make a website mobile-friendly using HTML?**

**Answer:** Use the `<meta name="viewport" content="width=device-width, initial-scale=1.0">` tag.

---

### 20. **What are void (self-closing) elements in HTML?**

**Answer:** Elements that don’t have a closing tag. Examples: `<img>`, `<br>`, `<hr>`, `<input>`.

---

Absolutely! Here are **more HTML interview questions** that are frequently asked, especially for **freshers** who are starting their careers in web development.

---

## 🔹 **Additional Basic & Intermediate HTML Questions**

### 21. **What is the difference between `<div>` and `<span>`?**

**Answer:**

- `<div>` is a **block-level** element used for grouping larger sections.
- `<span>` is an **inline** element used for grouping smaller parts like text within a line.

---

### 22. **What are empty elements in HTML?**

**Answer:** Elements that **do not have any content** or a closing tag.
Examples: `<br>`, `<hr>`, `<img>`, `<input>`

---

### 23. **What is the purpose of the `rel` attribute in the `<link>` tag?**

**Answer:** It defines the **relationship** between the current document and the linked file.
Example:

```html
<link rel="stylesheet" href="styles.css" />
```

---

### 24. **What are global attributes in HTML?**

**Answer:** Attributes that can be used with **any HTML element**.
Examples: `id`, `class`, `style`, `title`, `data-*`, `hidden`, `lang`, `dir`.

---

### 25. **What does the `target="_blank"` attribute do in a link?**

**Answer:** It opens the link in a **new browser tab** or window.

---

### 26. **What is the difference between `GET` and `POST` methods in forms?**

**Answer:**

- `GET`: Appends data to the URL, less secure, used for fetching.
- `POST`: Sends data in the request body, more secure, used for submitting.

---

### 27. **How can you add comments in HTML?**

**Answer:**

```html
<!-- This is a comment -->
```

---

### 28. **How do you embed a video in HTML5?**

**Answer:**

```html
<video controls>
  <source src="video.mp4" type="video/mp4" />
  Your browser does not support the video tag.
</video>
```

---

### 29. **What is the difference between `<strong>` and `<b>` tags?**

**Answer:**

- `<strong>`: Has semantic meaning (importance).
- `<b>`: Only applies bold styling, no semantic meaning.

---

### 30. **What is the difference between `<em>` and `<i>` tags?**

**Answer:**

- `<em>`: Emphasizes text with semantic meaning.
- `<i>`: Italics without meaning, just stylistic.

---

## 🔹 **Accessibility & Best Practices**

### 31. **What is accessibility in HTML?**

**Answer:** Designing HTML content so that it can be used by people with disabilities using screen readers, keyboard navigation, etc.

---

### 32. **What is the role of `aria-*` attributes?**

**Answer:** They improve **accessibility** by helping screen readers interpret elements that are not natively accessible.

---

### 33. **What are the best practices for writing HTML?**

- Use semantic elements.
- Write clean, well-indented code.
- Use `alt` for images.
- Avoid inline styles (use CSS).
- Use lowercase tag names.
- Always close tags.

---

### 34. **What are data attributes in HTML5?**

**Answer:** Custom attributes that start with `data-`. They store extra information.

```html
<div data-user-id="12345"></div>
```

---

### 35. **What is the difference between `localStorage` and `sessionStorage` in HTML5?**

**Answer:**

- `localStorage`: Stores data **permanently** in the browser.
- `sessionStorage`: Stores data for **one session** (until the tab is closed).

---

## 🔹 **Advanced/Tricky HTML Questions (Still Freshers-Friendly)**

### 36. **Can a single HTML document have multiple `<head>` tags?**

**Answer:** No, only **one `<head>`** is allowed per document.

---

### 37. **What happens if you forget to close an HTML tag?**

**Answer:** The browser **tries to fix** the markup by inferring structure, but it may cause **unintended rendering** or layout issues.

---

### 38. **What is the use of `<noscript>` tag?**

**Answer:** Displays alternate content for users whose browsers **do not support JavaScript** or have it disabled.

---

### 39. **How do you embed a Google Map in HTML?**

**Answer:** Use an `<iframe>`:

```html
<iframe src="https://www.google.com/maps/embed?..."></iframe>
```

---

### 40. **How is HTML different from XML?**

| Feature         | HTML               | XML                         |
| --------------- | ------------------ | --------------------------- |
| Purpose         | Displaying content | Storing & transporting data |
| Tags            | Predefined         | Custom                      |
| Error Tolerance | Lenient            | Strict                      |

---
