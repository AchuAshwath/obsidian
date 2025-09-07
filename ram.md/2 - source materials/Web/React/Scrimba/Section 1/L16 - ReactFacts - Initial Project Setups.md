02-08-2025 14:25:57

Status :

Tags :

# Initial Project Setup

This lesson establishes the foundational file structure and component hierarchy that is a common convention in modern React applications. It moves away from the single `index.jsx` file to a more organized, scalable structure.

## Challenge: The Bare Bones Setup

**Goal:** Create the basic file and component structure for the ReactFacts project.

**Specific Tasks:**

1.  **Create `app.jsx`:**
      * Create a new file in the project root called `App.jsx`.
      * Inside, define a component called `App` and export it (`export default`).
      * For now, have it return a simple `<h1>` with text like "App component here."
2.  **Create `components` folder:**
      * Create a new folder in the project root called `components`.
3.  **Create `Navbar.jsx` and `Main.jsx`:**
      * Inside the `components` folder, create `Navbar.jsx` and `Main.jsx`.
      * In each file, define and export a component with the same name (`Navbar` and `Main`).
      * Have them return a simple `<h1>` with text indicating their purpose (e.g., "Navbar goes here," "Main component goes here").
4.  **Connect the components:**
      * In `App.jsx`, import `Navbar` and `Main` from their respective files.
      * Have the `App` component return `<Navbar />` and `<Main />` (wrapped in a Fragment or `div`).
5.  **Render `App`:**
      * In `index.jsx`, remove all existing components and import the new `App` component.
      * Call `root.render(<App />);`.
6.  **Add Google Fonts:**
      * Find the "Inter" font on [Google Fonts](https://fonts.google.com/specimen/Inter).
      * Get the `400`, `600`, and `700` weights.
      * Copy the `<link>` tags and paste them into the `<head>` of your `index.html` file, before the link to your stylesheet.

**`App.jsx`:**

```javascript
import Navbar from './components/Navbar';
import Main from './components/Main';
import React from 'react'; // React needs to be in scope for JSX

export default function App() {
    return (
        // Fragment is a good choice here to group the two components
        // without adding an extra DOM node
        <>
            <Navbar />
            <Main />
        </>
    );
}
```

**`components/Navbar.jsx`:**

```javascript
import React from 'react'; // React needs to be in scope for JSX

export default function Navbar() {
    return (
        <h1>Navbar goes here</h1>
    );
}
```

**`components/Main.jsx`:**

```javascript
import React from 'react'; // React needs to be in scope for JSX

export default function Main() {
    return (
        <h1>Main component goes here</h1>
    );
}
```

**`index.jsx`:**

```javascript

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
    <React.StrictMode>
        <App />
    </React.StrictMode>
);
```

**`index.html` (`<head>` section):**

```html
<head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!-- Google Fonts Links -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="index.css">

    <title>ReactFacts</title>
</head>
```

## Key Takeaways

1.  **Standard React File Structure:** This hierarchical approach is a common and highly effective pattern:

      * `index.jsx`: The "entry point" of the application, responsible for mounting the top-level component (`<App />`) into the DOM. It typically contains no application logic.
      * `App.jsx`: The top-level component that acts as the container for the entire application. It defines the main layout and renders the major sections (e.g., `Navbar`, `Main`, `Footer`).
      * `components/`: A folder to store all other reusable UI components. This keeps the project organized and prevents clutter.

2.  **`import` Pathing:**

      * `import App from './App.jsx'`: The `./` indicates that the `App.jsx` file is in the same directory as `index.jsx`.
      * `import Navbar from './components/Navbar.jsx'`: The `./components/` indicates that the `Navbar.jsx` file is inside the `components` folder, which is in the same directory.
      * Some bundlers and configurations may allow you to omit the `.jsx` extension, but including it is often safer and more explicit.

3.  **Fonts and Styling:**

      * Pre-loading fonts in the `<head>` of `index.html` is a best practice for performance, as it ensures the font is available before the page renders, preventing a "flash of unstyled text" (FOUT).
      * You've now set up the foundation to apply these fonts via CSS in a later step.

This setup is the standard starting point for most React projects and is crucial for maintaining a clean, scalable, and manageable codebase.
## References


