16-06-2025 16:57:56

Status :

Tags :

## 1. Why you should care about React

### The Core Idea: Letting React Control the DOM
- **Traditional Approach:** You manually write HTML markup (e.g., `<h1>Hello World</h1>`) in an `.html` file to make content appear in the browser.
- **React Approach:** You write JavaScript code, and React takes responsibility for creating and adding the corresponding HTML markup to the page for you.
- To make this work, you need a placeholder element in your HTML file. This is typically a `<div>` with an ID, commonly `id="root"`. React uses this "root" element as the main container to inject all the content it generates.
### Your First React App: The Bare Essentials
To create a basic React application, you need to perform two main steps in your JavaScript file (often with a `.jsx` extension):
1. **Create a "root":** Tell React which DOM element it should manage.
2. **Render content to the root:** Tell React _what_ to display inside that element.

### The Code
The fundamental code to achieve this involves importing `createRoot` from the `react-dom/client` library.

```jsx
// 1. Import the necessary function
import { createRoot } from 'react-dom/client';

// 2. Select the DOM node where the app will be mounted
const domNode = document.getElementById('root');

// 3. Create a root for that DOM node
const root = createRoot(domNode);

// 4. Render your React element (which looks like HTML) into the root
root.render(<h1>Hello, React!</h1>);
```

### Alternative Syntaxes
- You can chain the methods for a more concise version:
  
```jsx
import { createRoot } from 'react-dom/client';

createRoot(document.getElementById('root')).render(<h1>Hello, React!</h1>);
```
- You can also use other DOM selectors, like `document.querySelector('#root')`.

### Writing with JSX

- The syntax that looks like HTML but is written inside a JavaScript file is called **JSX (JavaScript XML)**.
- It allows you to write UI components in a familiar, declarative way.
- You can nest elements just like in HTML, making it intuitive to build complex UIs.

**Example with a list:**

```jsx
root.render(
  <ul>
    <li>It's a popular library.</li>
    <li>It will make me more employable.</li>
  </ul>
);
```

### Learning Environment: Scrimba vs. Local Setup

- **Scrimba:** The learning platform handles all the complex setup (bundling, dependencies) behind the scenes, allowing you to focus purely on writing React code from day one.
- **Local Machine:** Setting up a React project locally involves more tooling and configuration (which will be covered later). This is how you'll build real-world projects, but it can be a distraction when you're just starting to learn the core concepts of React itself.
- **Recommendation:** The instructor suggests focusing on learning React's syntax and philosophy first, without getting bogged down by the setup process.

### The Importance of Practice
- The lesson emphasizes the value of **repetition and muscle memory**.
- You are encouraged to actively participate in challenges, even if it means re-watching previous sections or looking up information.
- This active discovery process is more beneficial for long-term learning than passively watching the solution.

## References


