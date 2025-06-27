24-06-2025 14:53:11

Status :

Tags :

# React's Composability and Declarative Nature

One of React's core strengths lies in its composable and declarative nature.
## `createElement()`

Before JSX became the standard, React applications were built using `React.createElement()`. This function is fundamental to how React internally represents UI elements.

**Key Points:**

- `React.createElement()` is a function exported by React.
- **Do not confuse it with `document.createElement()`** (which is a browser API). While conceptually similar in creating elements, `React.createElement()` operates within React's virtual DOM.
- It takes three main parameters:
    1. **Type of element:** A string representing the HTML tag (e.g., `'h1'`, `'div'`, `'p'`).
    2. **Props (properties):** An object containing attributes for the element (e.g., `className`, `id`). For simple elements without attributes, `null` can be passed initially.
    3. **Children:** The content or nested elements within the current element. This can be a string, another `React.createElement()` call, or an array of elements.

**Example Usage:**

```javascript
import { createElement } from 'react
// Creating a simple H1 element with text content
const reactElement = createElement(
    "h1",
    null, // No props for now
    "Hello from create element"
);

// To render this element using ReactDOM (not covered in this segment, but for context)
// ReactDOM.render(reactElement, document.getElementById("root"));

// Logging the returned value to the console
console.log(reactElement);
```

> This gets harder to comprehend when you start to nest components

**What `createElement()` Returns:**

- When you call `React.createElement()`, it does **not** directly return a DOM node.
- Instead, it returns a **plain JavaScript object**.
- This object has a specific structure that React understands, containing information about the element's type, props, and children.
- React uses this object to construct its **Virtual DOM**, which is an in-memory representation of the actual DOM.

**Output of `console.log(reactElement)`:**

```json
Object { "$$typeof": Symbol("react.transitional.element"), type: "h1", key: null, props: {…}, _owner: null, _store: {…}, … }
"$$typeof": Symbol("react.transitional.element")
_debugInfo: null
_debugStack: Error: react-stack-top-frame
_debugTask: null
_owner: null
_store: Object { … }
key: null
props: Object { children: "hellow from the create element" }
ref: null
type: "h1"
<prototype>: Object { … }
```

- **Takeaway:** This JavaScript object is crucial because it's what React uses to efficiently manage and update the user interface. This fundamental understanding is key when moving to JSX.

## References


