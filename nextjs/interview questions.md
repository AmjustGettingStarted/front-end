### ✅ **Next.js Interview Questions**

#### 1. **What is Next.js?**

- Explain what it is, and how it's built on top of React.
- Why it's considered a full-stack framework.

#### 2. **What are the main features of Next.js?**

- Server-side rendering (SSR)
- Static site generation (SSG)
- API routes
- Image optimization
- File-system-based routing
- Incremental static regeneration (ISR)

#### 3. **What is the difference between SSR, SSG, and CSR in Next.js?**

- When to use each and how they're implemented in Next.js.

#### 4. **How does routing work in Next.js?**

- File-based routing system using the `pages/` directory.
- Dynamic routes using brackets (e.g., `[id].js`).

#### 5. **What is the difference between `getStaticProps`, `getServerSideProps`, and `getInitialProps`?**

- Usage and lifecycle of each.
- Which are called at build time or runtime.

#### 6. **What is API routing in Next.js?**

- Creating serverless functions in the `pages/api/` directory.
- Use cases (e.g., form handling, data fetching).

#### 7. **How to do dynamic routing in Next.js?**

- Using `[param].js` and `useRouter()` hook.

#### 8. **How is navigation handled in Next.js?**

- Using `<Link>` component from `next/link`.
- Prefetching routes automatically.

#### 9. **What is Image Optimization in Next.js?**

- Using the `next/image` component.
- Benefits like lazy loading, automatic resizing, and WebP support.

#### 10. **What is `getStaticPaths` used for?**

- Used with `getStaticProps` for dynamic static generation.

---

### ⚙️ Technical & Practical Questions

#### 11. **How do you fetch data in Next.js?**

- Client-side: `fetch`, `axios`, `useEffect`
- Server-side: `getServerSideProps`, `getStaticProps`

#### 12. **What are the differences between Next.js and CRA (Create React App)?**

- SSR and SSG support in Next.js
- Better SEO, performance, routing

#### 13. **What is Incremental Static Regeneration (ISR)?**

- Rebuilding static pages on-demand using `revalidate` key in `getStaticProps`.

#### 14. **How do you deploy a Next.js app?**

- Platforms like Vercel (official), Netlify, or custom servers.

#### 15. **How do you handle environment variables in Next.js?**

- Using `.env.local`, `.env.production`, etc.
- Accessing with `process.env.NEXT_PUBLIC_`

---

### 🔍 Basic React Knowledge (Expected for Next.js)

- **JSX, Components, Props, and State**
- **Hooks like `useState`, `useEffect`, `useRouter`**
- **Event handling and form submission**
- **Understanding of ES6+ JavaScript features**

---

Absolutely! Here's a continuation of **Next.js interview questions for freshers**, diving a bit deeper into real-world scenarios, performance optimization, and understanding of the framework’s features.

---

## 🧠 More Next.js Interview Questions for Freshers

---

### 📁 **Routing & Pages**

#### 16. **How do you create nested routes in Next.js?**

- By creating nested folders in the `pages/` directory.

#### 17. **What is a catch-all route in Next.js?**

- Using `[...slug].js` for matching multiple segments in a URL.

#### 18. **What is the difference between a dynamic route and a catch-all route?**

- `[id].js` vs `[...params].js` vs `[[...params]].js` (optional catch-all).

#### 19. **How do you handle 404 or custom error pages?**

- Create a custom `pages/404.js` or `pages/_error.js`.

---

### ⚡ **Performance & Optimization**

#### 20. **What is code splitting in Next.js?**

- Automatic splitting of JavaScript by page to improve performance.

#### 21. **How does Next.js handle lazy loading?**

- Automatically lazy-loads images and code with dynamic imports.

#### 22. **How can you improve performance in a Next.js app?**

- Use SSR/SSG appropriately
- Image optimization
- Minimize third-party scripts
- Use caching and CDN (Vercel does this)

#### 23. **How does Next.js handle caching and CDN?**

- Automatic static optimization and CDN support (especially with Vercel)

---

### 🧩 **API & Backend Integration**

#### 24. **Can you connect to a database in Next.js?**

- Yes, via API routes or in `getServerSideProps`/`getStaticProps`.

#### 25. **What are serverless functions in Next.js?**

- Functions in `pages/api/` that run on demand on the server (lambda functions).

#### 26. **How do you create REST API endpoints in Next.js?**

- Inside `pages/api/` folder, e.g., `pages/api/users.js`.

---

### 🎨 **Styling & Theming**

#### 27. **How do you style components in Next.js?**

- CSS Modules (e.g., `styles.module.css`)
- Global CSS
- Tailwind CSS
- Styled-components or other CSS-in-JS libraries

#### 28. **What are CSS Modules in Next.js?**

- Scoped CSS files that avoid global class name conflicts.

#### 29. **How do you add global styles in Next.js?**

- Import in `pages/_app.js` using `import '../styles/globals.css'`

---

### 🧪 **Advanced but Useful Topics (Light for Freshers)**

#### 30. **What is middleware in Next.js?**

- Runs before a request is completed (e.g., auth, redirects).
- Located in `middleware.ts` or `middleware.js` at root.

#### 31. **What is the `_app.js` file used for?**

- Customize the root component; useful for layout, context providers, etc.

#### 32. **What is `_document.js` used for?**

- Used to customize the HTML document structure (e.g., `<html>`, `<body>`, adding meta tags).

#### 33. **What are Layouts in Next.js and how do you implement them?**

- Custom layout per page using shared components via `_app.js`.

---

### 🧠 Conceptual / Real-World

#### 34. **How do you protect routes in Next.js (authentication)?**

- Client-side: check auth token in components.
- Server-side: check token in `getServerSideProps` or API route.

#### 35. **What are the benefits of using Next.js for SEO?**

- SSR and SSG provide HTML to crawlers, improving indexing.

#### 36. **How would you migrate a CRA app to Next.js?**

- Replace routing logic
- Move pages into `pages/`
- Adjust fetch/data logic
- Handle SSR/SSG needs

---

### 🧑‍💻 Bonus: Coding/Practical Questions

1. **Create a simple blog using SSG with dynamic routes.**
2. **Build a form that submits to an API route.**
3. **Use `getServerSideProps` to fetch data from a public API and display it.**
4. **Use dynamic import to lazy-load a heavy component.**

---

Would you like me to:

- Provide **answers** to any specific question?
- Generate a **PDF mock interview sheet**?
- Create a **project-based assignment** based on these?

Let me know how you'd like to prepare further!
