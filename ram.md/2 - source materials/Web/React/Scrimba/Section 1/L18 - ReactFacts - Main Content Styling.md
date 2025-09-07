02-08-2025 14:28:20

Status :

Tags :

# Main Content Section: Styling the Core Page

This lesson focuses on building and styling the main content area of the ReactFacts project, following the Figma design. Like the Navbar, it involves significant CSS work.

## Challenge: Build and Style the Main Content

**Goal:** Create the markup and apply the necessary CSS to the main content section, matching the Figma design.

**Exclusions for this Challenge:**

  * **Colored/Sized Bullets:** Don't worry about styling the bullet points on the list items yet.
  * **Background React Logo:** The large, faded React logo in the background will be a separate challenge.

**Specific Tasks:**

1.  **Markup in `Main.jsx`:**
      * The top-level element should be `<main>` for semantic correctness.
      * Inside `main`, add an `<h1>` for the title "Fun facts about React".
      * Below the `<h1>`, add an unordered list (`<ul>`) with the following five list items (`<li>`):
          * "Was first released in 2013"
          * "Was originally created by Jordan Walke"
          * "Has well over 100K stars on GitHub"
          * "Is maintained by Facebook"
          * "Powers thousands of enterprise apps, including mobile apps"
2.  **Styling in `index.css`:**
      * **Body Background:** Set the overall background color of the `body` to a dark color from the Figma design. This ensures the background covers the entire page.
      * **Main Padding:** Add padding to the `main` element to create space around its content (top/bottom and left/right).
      * **H1 Margin:** Reset the default top margin of the `h1` element within `main` to prevent unwanted pushing of the `main` section.
      * **Text Color:** Set a light `color` (e.g., white) for the text within the `body` to ensure it's visible against the dark background.
      * **H1 Font Size:** Set the font size of the `h1` to match the Figma design (approx. `2.4rem`).
      * **List Styling:**
          * Apply a `className` (e.g., `facts-list`) to the `<ul>`.
          * Add `margin-top` to the `.facts-list` to create space between the `h1` and the list.
          * Add `padding-block` (or `margin-top` on `li` children) to create vertical spacing between the `<li>` items. Using `padding-block` on the `li`s is better to avoid collapsing margins.
          * Optionally, set a `max-width` on the `.facts-list` to prevent lines from becoming too long.
          * Optionally, set `line-height` for better readability.

**`components/Main.jsx`:**

```javascript
import React from 'react';

export default function Main() {
    return (
        // The main element serves as the top-level container for this component
        <main className="main-content"> {/* Added a class for styling */}
            <h1>Fun facts about React</h1>
            <ul className="facts-list"> {/* Added a class for styling the list */}
                <li>Was first released in 2013</li>
                <li>Was originally created by Jordan Walke</li>
                <li>Has well over 100K stars on GitHub</li>
                <li>Is maintained by Facebook</li>
                <li>Powers thousands of enterprise apps, including mobile apps</li>
            </ul>
        </main>
    );
}
```

**`index.css`:**

```css
body{
  margin : 0;
  font-family: Inter;
  background-color: #282D35;
  color: white;
}

header{
  height: 90px;
  background-color: #212121;
  padding: 20px 25px;
}

nav {
  display: flex;
  align-items: center;
  height: 100%;
}

nav > img{
  width: 80px; /* Adjust the width as needed */
  margin-right: 7px;
}

nav > span {
  font-size: 1.4em;
  color: #ffffff;
  margin-left: 7px;
  color: #61DAFB;
  font-weight: 700;
}

main{
  padding: 30px 60px;
}

main > h1 {
  margin: 0;
  font-size: 2.4rem;
}

.facts-list {
  margin-top: 23px;
  max-width: 500px;
}

.facts-list > li {
  padding-block: 5px;
  line-height: 19px;
  font-size: 1.1rem;
}
```

\</details\>

-----

## Key Learnings from Main Content Styling:

1.  **Background Application:** Applying the main background color to the `body` is generally the most straightforward way to ensure it covers the entire viewport and interacts well with other elements like a fixed header.
2.  **Margin Collapse:** Be aware of **margin collapsing** (especially vertical margins). If a parent element has no padding or border between its top margin and its first child's top margin, those margins can collapse, taking on the value of the *larger* margin. Resetting margins on child elements or using `padding` on the parent can resolve this.
3.  **Spacing Strategies:** Using `padding-block` on list items for vertical spacing is often more predictable than `margin-top` or `margin-bottom` on list items, as `padding` doesn't collapse between siblings.
4.  **Rem Units:** Using `rem` (root `em`) units for `font-size` and other measurements tied to text is a good practice for accessibility, as it scales relative to the user's base font size.
5.  **Targeting Elements for CSS:** You can directly target elements within a parent using the child combinator (`>`) or descendant combinator (`     `) in CSS if you're confident in your HTML structure and want to avoid adding excessive class names. However, applying specific class names to your React components remains a robust and scalable method.

This challenge completes the basic content and layout of the main section. The next steps will tackle the more advanced styling details like custom bullet points and the background image.
## References


