# LLM Code Generation Context: Modern Vanilla JS/Alpine

**Core Philosophy:** Generate readable, simple, maintainable, and modern front-end code. Prioritize native browser features and Vanilla JavaScript. Use Alpine.js *only* when it significantly simplifies state management or complex UI interactions that would be verbose in Vanilla JS. Assume code is primarily for personal use unless specified otherwise (focus on modern browsers, less emphasis on extreme polyfills/compatibility).

**Technology Stack & Priorities:**

1.  **HTML:**
    *   **Semantic & Modern:** Use HTML5 elements correctly (e.g., `<article>`, `<nav>`, `<aside>`). Embrace modern elements like `<details>`, `<dialog>`, `<template>`.
    *   **Accessibility (Basic):** Use ARIA attributes (`aria-label`, `role`, etc.) where appropriate, especially for custom components or non-obvious interactions. Ensure keyboard navigability.
    *   **Structure:** Keep HTML clean and well-structured. Minimize "divitis".

2.  **CSS:**
    *   **Tailwind CSS:** This is the **primary** styling method. Apply utility classes directly in the HTML.
    *   **Design is directed by a separate context file**

3.  **JavaScript:**
    *   **Vanilla JS First:** **Strong preference for modern Vanilla JavaScript (ES6+).** Use features like `const`/`let`, arrow functions, template literals, Promises, `async`/`await`, destructuring, optional chaining (`?.`), nullish coalescing (`??`).
    *   **Alpine.js (Conditional):** Use Alpine.js **sparingly** for declarative, component-level state management and UI interactions (e.g., dropdowns, modals, tabs). Define logic directly in `x-data`, `x-init`, `@event`, `x-show`, `x-bind`, `x-for`, etc. **Do not** use Alpine for simple DOM manipulations or tasks easily done with a few lines of Vanilla JS.
    *   **Modularity:** Use **ES Modules** (`import`/`export`) to organize code into logical, reusable units. Place `<script type="module">` typically at the end of `<body>` or use `defer`.
    *   **DOM Interaction:**
        *   Prefer efficient selectors (`getElementById`, `querySelector`, `querySelectorAll`).
        *   Use event delegation where practical (attach listener to parent).
        *   Manipulate the DOM efficiently; use `<template>` elements for cloning complex structures. Minimize reflows/repaints, especially in loops.
        *   Use `textContent` instead of `innerHTML` when inserting non-HTML text to prevent XSS vulnerabilities.
    *   **Readability & Maintainability:**
        *   Use clear, descriptive variable and function names (camelCase).
        *   Keep functions small and focused (Single Responsibility Principle).
        *   Add comments only for *why*, not *what*, or for complex logic.
        *   Format code consistently (like Prettier defaults).
    *   **Asynchronous Operations:** Use `async`/`await` for managing Promises.
    *   **Error Handling:** Implement basic `try...catch` blocks for operations that might fail (e.g., API calls, `JSON.parse`).
    *   **Performance:** Consider debouncing/throttling event listeners for high-frequency events (scroll, resize, input).

4.  **State & Persistence:**
    *   **`localStorage`:** Use for simple key-value persistence across browser sessions. **Always** use `JSON.stringify()` when saving objects/arrays and `JSON.parse()` (within a `try...catch`) when retrieving. Be mindful of storage limits and its synchronous nature. Do not store sensitive information.
    *   **`sessionStorage`:** Consider if persistence is only needed for the duration of the browser tab/session.
    *   **In-Memory State:** For component-level, non-persistent state, use Vanilla JS variables/objects or Alpine.js `x-data`.

5.  **Provided UI Context:**
    *   A UI context file (e.g., `ui_context.js` or similar containing reusable UI functions/constants) will often be provided. **Always** utilize functions/constants from this context where applicable instead of redefining similar logic.

**Exclusions (Unless explicitly requested):**

*   **Frameworks:** No React, Vue, Angular, Svelte, etc. (Alpine.js is the *only* exception, used minimally).
*   **Libraries:** No jQuery or other large utility libraries unless specifically required for a unique task not easily solvable otherwise.
*   **Build Tools:** Assume no complex build steps (Webpack, Vite, Parcel) unless specified. Code should run directly in modern browsers.
*   **CSS Preprocessors:** No Sass, Less, Stylus.

**Goal:** Generate code that is immediately understandable, follows modern web standards, leverages the specified stack effectively, and integrates seamlessly with the provided UI context. Prioritize simplicity and directness.