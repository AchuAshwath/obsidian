02-08-2025 14:21:52

Status :

Tags :

# Styling in React: Using Classes

This lesson focuses on how to apply CSS styles to your React components using external stylesheets and class names, highlighting the key difference from vanilla HTML.

## Basic Styling Principles in React

* **External Stylesheets:** Just like in vanilla HTML/CSS, you link your `.css` files in your `index.html`.

```html
<head>
	<link rel="stylesheet" href="index.css">
</head>
```

* **Applying Styles:** You define your CSS rules in your `.css` file and apply them to elements in your React components using class names.

## The `className` Attribute

The primary difference when applying CSS classes in React JSX compared to vanilla HTML is the attribute name:

  * **Vanilla HTML:** `class="my-class"`
  * **React JSX:** `className="my-class"`

**Why `className`?**

  * This is **NOT** because `class` is a reserved keyword in JavaScript for creating classes (`class MyClass {}`).
  * Instead, it's because when React internally transforms your JSX into actual DOM elements (using methods similar to `document.createElement()`), it interacts with the DOM API. In the native DOM API, the property used to set an element's class is `element.className`.
  * React's `className` in JSX directly maps to the `className` property of the underlying DOM element, just like `onClick` maps to `onclick` and `htmlFor` maps to `for` for accessibility labels.

**Example:**

```javascript
// In React JSX
<ul className="nav-list">
    <li>Item 1</li>
    <li>Item 2</li>
</ul>
```

```css
/* In your App.css */
.nav-list {
    list-style: none; /* Example style */
}
/* remove #root
```

## Challenge 1: Style the Navbar with Flexbox

**Goal:** Use Flexbox to align the list items (`<li>`) horizontally within the navigation list and align the logo and the entire navigation horizontally in the header. **Crucially, use class names for all styling (no bare element selectors like `nav` or `ul`).**

**Specific Steps & Hints:**

1.  **Apply `className="nav-list"` to your `<ul>` element within the `Header` component.**
2.  **In `index.css`:**
      * Target `.nav-list`.
      * Set `display: flex;` to align list items horizontally.
      * Remove bullet points using `list-style: none;`.
      * (Optional, but good practice for spacing) Add `margin-left` (e.g., `10px`) to each list item. You'll need to apply a class name (e.g., `nav-list-item`) to each `<li>` and then target `.nav-list-item` in CSS.
3.  **Apply `className="header"` to your `<header>` element within the `Header` component.**
4.  **In `index.css`:**
      * Target `.header`.
      * Set `display: flex;` to align the logo (`<img>`) and the navigation (`<nav>`) horizontally.
      * Use `align-items: center;` to vertically center the items (prevents image stretching).
      * Use `justify-content: space-between;` to push the logo to one side and the navigation to the other.

**`App.jsx` (or `Page.jsx` if not broken into Header component yet):**

```javascript
// Assuming you've already extracted the Header component
function Header() {
    return (
        <header className="header"> {/* Added className="header" */}
            <img src="react-logo.png" width="40px" alt="React Logo" />
            <nav> {/* Assuming nav element wraps the ul */}
                <ul className="nav-list"> {/* Added className="nav-list" */}
                    <li className="nav-list-item">Pricing</li> {/* Added className="nav-list-item" */}
                    <li className="nav-list-item">About</li>   {/* Added className="nav-list-item" */}
                    <li className="nav-list-item">Contact</li> {/* Added className="nav-list-item" */}
                </ul>
            </nav>
        </header>
    );
}
```

**`App.css`:**

```css
/* Styles for the overall header container */
.header {
    display: flex;
    align-items: center; /* Vertically centers children */
    justify-content: space-between; /* Pushes content to edges */
}

/* Styles for the navigation list */
.nav-list {
    list-style: none; /* Removes bullet points */
    display: flex;     /* Makes list items horizontal */
    padding: 0;       /* Remove default padding */
    margin: 0;        /* Remove default margin */
}

/* Styles for individual list items */
.nav-list-item {
    margin-left: 10px; /* Adds space between list items */
    font-size: 1.1rem; /* Optional: adjust font size */
}
```

## Challenge 2: Move Image Width to CSS

**Goal:** Remove the inline `width` attribute from the `<img>` tag in JSX and apply the width using a CSS class instead. Change the width to `55px`.

**Specific Steps:**

1.  **Add a `className` (e.g., `nav-logo`) to the `<img>` tag in your `Header` component.**
2.  **Remove the `width="40px"` attribute from the `<img>` tag in JSX.**
3.  **In `index.css`, create a rule for `.nav-logo` and set `width: 55px;`.**

**`Header.jsx`:**

```javascript
function Header() {
    return (
        <header className="header">
            {/* Removed width="40px", added className="nav-logo" */}
            <img src="react-logo.png" className="nav-logo" alt="React Logo" />
            <nav>
                <ul className="nav-list">
                    <li className="nav-list-item">Pricing</li>
                    <li className="nav-list-item">About</li>
                    <li className="nav-list-item">Contact</li>
                </ul>
            </nav>
        </header>
    );
}
```

**`index.css`:**

```css
/* ... existing CSS ... */

.nav-logo {
    width: 55px; /* New width applied via CSS */
}
```
## Encouragement: Personalize Your Design\!

  * Take 5-10 minutes to add your own styling flair to the page.
  * Experiment with colors, fonts, spacing, background images, etc.
  * You don't have to stick to the dark theme. Make it your own\!
  * **Share your creations\!** Post your design in the Scrimba Discord's `#i-built-this` channel to get feedback and celebrate your progress. This is a great way to interact with the community and feel proud of your learning journey.

## References


