25-06-2025 11:04:54

Status :

Tags :

# Introduction to JSX (JavaScript XML)

While `createElement()` is the underlying mechanism, directly using it for complex UIs quickly becomes verbose and hard to read, especially with nested elements. This led to the creation of **JSX**.

- JSX is a syntax extension for JavaScript.
- It allows you to write HTML-like markup directly within your JavaScript code.
- **Developer Experience:** JSX was created to significantly improve the developer experience by making UI code more readable and intuitive.
- **Behind the Scenes:** When you write JSX, it is **transpiled (converted)** by tools like Babel into `React.createElement()` calls before being executed by the browser.

> "Using `Create element` is not the greatest developer experience... if you wanted to Nest elements together... JSX is that HTML looking thing that we saw in the beginning of the project."

```jsx
const reactElement = <h1>hellow from JSX!</h1> 

console.log(reactElement);
createRoot(document.getElementById('root')).render(
  reactElement
)
```

 This also return a similar javascript object

```json
Object { "$$typeof": Symbol("react.transitional.element"), type: "h1", key: null, props: {…}, _owner: null, _store: {…}, … }
"$$typeof": Symbol("react.transitional.element")
_debugInfo: null
_debugStack: Error: react-stack-top-frame
_debugTask: null
_owner: null
_store: Object { … }
key: null
props: Object { children: "hellow from JSX!" }
ref: null
type: "h1"
```
## References


