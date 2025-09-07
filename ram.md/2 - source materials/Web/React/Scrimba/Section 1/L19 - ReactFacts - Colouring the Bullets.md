02-08-2025 14:29:44

Status :

Tags :

# Colouring the Bullets

This lesson focuses on styling the bullet points of the unordered list in the main content section of the ReactFacts page to match the design.

## The Challenge of Customizing List Bullets

Traditionally, customizing list bullets in CSS to change their color, size, and position precisely can be tricky. Common methods involve:

  * Removing default bullets (`list-style: none;`).
  * Using `::before` pseudo-elements to create custom shapes and then styling and positioning them.

While effective, this approach can be quite "nitty-gritty" and might be overkill for a React course's primary focus.

## Solution: Using the `::marker` Pseudo-Element

For simpler customizations like changing color and size, CSS offers the `::marker` pseudo-element, which is specifically designed for styling list item markers (bullets or numbers).

  * The `::marker` pseudo-element allows you to target and style the actual bullet point (or number) of a list item directly.
  * It supports a limited set of CSS properties, primarily related to text and color (e.g., `color`, `font-size`, `content`, `white-space`).

**Applying `::marker` to the ReactFacts List Items:**

1.  **Target the list items (`<li>`) within your facts list.**
2.  **Use the `::marker` pseudo-element.**
3.  **Apply `color` and `font-size` properties.**

**Example CSS:**

```css
/* index.css */

.facts-list > li::marker { /* Target the marker of list items within .facts-list */
    color: #61DAFB; /* Set color to React blue (same as Navbar title) */
    font-size: 1.5rem; /* Set font size to make bullets larger */
    /* Note: Going too large with font-size on ::marker can cause
             misalignment with the list item text in some browsers.
             1.5rem is chosen here as a good balance for alignment. */
}
```

**Why `1.5rem` for `font-size`?**

  * While the design might suggest a larger bullet size (e.g., equivalent to `2rem`), increasing the `font-size` on `::marker` too much can lead to visual misalignment between the bullet and the text of the list item.
  * `1.5rem` provides a noticeable increase in size while maintaining good alignment. For pixel-perfect alignment in more complex scenarios, the `::before` pseudo-element method might still be necessary.

This technique provides a quick and clean way to style list bullets without resorting to more complex CSS hacks.
## References


