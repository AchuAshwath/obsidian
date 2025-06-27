25-06-2025 12:55:30

Status :

Tags :

# Random Housekeeping & Project Setup

This section covers essential setup details and common considerations when starting a new React project, particularly with Vite.

## Challenge: Setup New React App from Scratch

This challenge reinforces the basic steps of setting up a React application.

**Goal:** Create a new React app that renders a simple `<h1>` element.

**Hints:**

- Import `createRoot` from `react-dom/client`.
- Grab the DOM node with `id="root"`.
- Call `root.render()` with your JSX.

&lt;details>

&lt;summary>Click to reveal Solution&lt;/summary>

JavaScript

```
// index.jsx (or index.js, but .jsx is preferred for JSX content)

// 1. Import createRoot from react-dom/client
import { createRoot } from 'react-dom/client';

// 2. Get the DOM node where React will mount the app
const container = document.getElementById('root');

// 3. Create a root instance
const root = createRoot(container);

// 4. Render your React element into the root
root.render(<h1>This is React</h1>);
```

HTML (index.html) Requirement:

Ensure your index.html file has a div with the ID root:

HTML

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React App</title>
</head>
<body>
    <div id="root"></div>
    <script type="module" src="/index.jsx"></script> </body>
</html>
```

&lt;/details>

---

## Housekeeping Point 1: File Extensions (`.jsx` vs. `.js`)

When using JSX in your React files, it's a best practice to use the `.jsx` file extension.

- **Vite Recommendation:** Vite's documentation recommends using `.jsx` for any JavaScript file that contains JSX syntax.
- **Performance & Smoothness:** This helps Vite bundle your code more efficiently and ensures smooth operation.
- **Backward Compatibility:** If you were using the older `React.createElement()` API without JSX, a `.js` extension would suffice. However, with modern React and JSX, `.jsx` is preferred.

## Housekeeping Point 2: Handling Static Images

Dealing with static images (images not coming from a CDN or database) in React projects, especially with build tools like Vite, can be slightly different from traditional HTML.

- **Traditional HTML:** You typically use a relative path directly in the `src` attribute.
    
    HTML
    
    ```
    <img src="./react-logo.png" alt="React Logo" />
    ```
    
- **Vite Behavior & Potential Issues:**
    
    - While a relative path _might_ work in a Scrimba environment (due to how it handles file paths), it can often fail in a locally set up Vite project.
    - Vite's build process might change paths or expect specific import mechanisms.
- **Temporary Workaround (for non-Scrimba environments if relative paths fail):**
    
    - Use an **absolute path from your project root**. This often involves a leading `/` (e.g., `/src/assets/react-logo.png`) if your assets are in a specific folder.
    
    <!-- end list -->
    
    JavaScript
    
    ```
    // In React JSX:
    // (This is just a temporary solution for certain Vite setups)
    <img src="/src/assets/react-logo.png" alt="React Logo" />
    ```
    
- **Future (Better) Solution:** There's a more "React-accepted" way to handle static images (often involving `import` statements or Vite's asset handling) that will be covered in a later section.
    

## Housekeeping Point 3: Rendering Multiple Elements (The "One Parent Element" Rule)

A crucial rule in React rendering: **JSX expressions must have one parent element.**

- You **cannot** render multiple top-level JSX elements side-by-side without wrapping them.
    
    JavaScript
    
    ```
    // ❌ INCORRECT - Will cause an error
    root.render(
        <img src="./logo.png" alt="Logo" />
        <h1>This is another element</h1>
    );
    ```
    
    - **Reasoning:** This limitation stems from how JSX is transpiled to `React.createElement()`. You can't call two `React.createElement()` functions directly as arguments to `root.render()` in this manner. It's like trying to return two separate values from a function where only one is expected.
- **Solution: Wrap in a Single Parent Element**
    
    - To render multiple elements, wrap them within a single parent HTML element (e.g., `div`, `main`, `section`, `article`).
    
    <!-- end list -->
    
    JavaScript
    
    ```
    // ✅ CORRECT - Wrapped in a <div>
    root.render(
        <div>
            <img src="./logo.png" alt="Logo" />
            <h1>This is another element</h1>
        </div>
    );
    ```
    
- **Choosing the Right Parent Element (Semantic HTML):**
    
    - While `div` works, it's often better to use **semantically correct HTML5 elements** (`<main>`, `<section>`, `<article>`, etc.) if they accurately describe the content.
    - Consult MDN Web Docs for semantic HTML elements to choose the most appropriate container for accessibility and meaning.
- **Analogy to `React.createElement()`:**
    
    - Wrapping elements in a parent is conceptually similar to nesting `React.createElement()` calls as children of a parent `React.createElement()` call:
    
    <!-- end list -->
    
    JavaScript
    
    ```
    // Conceptual equivalent to the correct JSX above
    React.createElement(
        "div", // Parent element
        null,  // No props for the parent div
        React.createElement("img", { src: "./logo.png", alt: "Logo" }), // Child 1
        React.createElement("h1", null, "This is another element") // Child 2
    );
    ```
    

---

With these housekeeping items covered, you are now ready to start building the "React Facts" project!

## References


