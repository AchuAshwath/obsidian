25-06-2025 11:23:13

Status :

Tags :

# Why React? (Composable & Declarative)

React is a powerful library for building user interfaces, and its popularity stems from several key advantages. We'll focus on two primary reasons why React is a significant step up from vanilla HTML, CSS, and JavaScript.

## 1. Composability

React's composability means it provides tools to easily create **reusable and interchangeable pieces of the web (components)** that can be combined in various ways to build complex systems.

### Analogy: Michelangelo's David vs. Lego David

- **Michelangelo's David (Imperative/Monolithic):**
    
    - Carved from a single block of marble.
    - A single, solid unit.
    - Cannot be easily reused or repurposed.
    - _Analogy to traditional web development:_ Building a full webpage from scratch, where elements are tightly coupled and hard to isolate or reuse.
- **Lego David (Composable):**
    
    - Built from many individual Lego bricks.
    - Each brick can be reused and repurposed in countless ways.
    - Allows for complex creations from simple, discrete units.
    - _Analogy to React:_ Building UIs from small, independent, and reusable components that can be assembled to form complex interfaces.

### The Problem with Traditional HTML for Reusability

Consider a common UI element like a navigation bar.

- **Traditional Approach (e.g., Bootstrap HTML):**
    
    - A navigation bar might be 30+ lines of complex HTML and CSS.
    - To include it on multiple pages, you would **copy and paste** this entire block of code into each HTML file.
    - **Maintenance Nightmare:** If you need to change anything in the navigation bar, you have to find and update it in _every single file_ where it's copied. This is prone to errors and time-consuming.
    
```HTML
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="#">Navbar</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Link</a>
      </li>
      <li class="nav-item dropdown">
        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
          Dropdown
        </a>
        <div class="dropdown-menu" aria-labelledby="navbarDropdown">
          <a class="dropdown-item" href="#">Action</a>
          <a class="dropdown-item" href="#">Another action</a>
          <div class="dropdown-divider"></div>
          <a class="dropdown-item" href="#">Something else here</a>
        </div>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled" href="#">Disabled</a>
      </li>
    </ul>
    <form class="form-inline my-2 my-lg-0">
      <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
      <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
    </form>
  </div>
</nav>
```


### React's Solution: Custom Components

React introduces the concept of **Custom Components**, which are reusable building blocks for your UI.

```jsx
<body>
	<MyawsomeNavbar />
	<MainContent />
	<MyAwsomeFooter />
</body>
```

- A custom component encapsulates its own logic and UI (JSX).
- You define it once, and then you can "render" instances of it wherever needed in your application.
- **Single Source of Truth:** Changes to a component's definition automatically reflect everywhere that component is used. This drastically simplifies maintenance.

**Example: `MyAwsomeNavbar` Component**

```jsx
function MyAwsomeNavbar() {
  const navBarStyles = {
    backgroundColor: '#333',
    padding: '10px 0',
    color: 'white',
    width: '100%',
    boxSizing: 'border-box',
    // --- Key styles to position it at the very top ---
    position: 'fixed', // Makes it stick to the viewport
    top: 0,            // Positions it at the very top of the viewport
    left: 0,           // Positions it at the very left of the viewport
    zIndex: 1000,      // Ensures it's on top of other content
    // --------------------------------------------------
  };

  const ulStyles = {
    listStyle: 'none',
    padding: 0,
    margin: 0,
    display: 'flex',
    justifyContent: 'center',
    gap: '20px',
  };

  const linkStyles = {
    color: 'white',
    textDecoration: 'none',
    fontWeight: 'bold',
    fontSize: '1.1em',
    padding: '5px 10px',
  };

  return (
    <nav style={navBarStyles}>
      <ul style={ulStyles}>
        <li><a href="/" style={linkStyles}>Home</a></li>
        <li><a href="/about" style={linkStyles}>About</a></li>
        <li><a href="/services" style={linkStyles}>Services</a></li>
        <li><a href="/contact" style={linkStyles}>Contact</a></li>
      </ul>
    </nav>
  );
}
```

### Challenge: Create Your First Custom React Component

**Goal:** Create a new React component called `MainContent` that returns a simple `<h1>` element saying "React is great!". Then, render it in `ReactDOM.render()`.

**Template:** Use the `MyAwesomeNavbar` component as a guide.

**Steps to Solve:**

1. Define a new JavaScript function for your component.
2. Make this function return JSX (your `<h1>` element).
3. Render an instance of your new component in `ReactDOM.render()`.

```jsx
function MainContent(){
  return <h1>React is great!</h1>
}

createRoot(document.getElementById('root')).render(
  <div>
    <MyAwsomeNavbar />
    <MainContent />
  </div>
)
```


 > When rendering a component that doesn't have children (like our `MainContent` component in this example), it must be a **self-closing tag** in JSX: `<MainContent />`. Forgetting the trailing slash (`/`) will result in errors.

## 2. Declarative Programming

Another fundamental reason to use React is its **declarative** nature. This contrasts with **imperative** programming.

|                 |                                                                                                                                                                                                                                           |                                                                                                                                                                                                                    |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Concept**     | **Description**                                                                                                                                                                                                                           | **Analogy**                                                                                                                                                                                                        |
| **Declarative** | **"What should be done?"** You describe the _desired outcome_ or _state_ of your UI, and React (the library) figures out _how_ to achieve it, handling all the underlying manual DOM manipulation.                                        | **Ordering at a Restaurant:** You tell the host, "Table for four, please." You state your desired outcome, and trust the host (the "library") to handle all the steps (finding a table, leading you, seating you). |
| **Imperative**  | **"How should it be done?"** You provide a step-by-step sequence of instructions to directly manipulate the DOM to reach the desired state. This involves manually creating elements, setting attributes, and appending them to the tree. | **Directing a Host:** You tell the host, "Walk 50 steps down the hallway, turn right, walk 35 steps, then seat us at the booth on the left." You give precise, step-by-step instructions.                          |

### Challenge: Imperative DOM Manipulation

**Goal:** Recreate the `<h1>React is great!</h1>` element using vanilla JavaScript (imperative DOM manipulation).

**Requirements:**

- Use `document.createElement()` to create the `<h1>`.
- Set its `textContent` property.
- Give it a `className` of `header`.
- Append it to the `div` with the ID `root` using `appendChild()`.
- **Do NOT use `innerHTML`**.

```jsx
// 1. Create a new H1 element
const h1 = document.createElement("h1")
// 2. Set its text content
h1.textContent= "This is manual imperative coding"; // Or "React is great!" for the challenge
// 3. Give it a class name
h1.className = "header";
// 4. Append the H1 to the root element
document.getElementById("root").appendChild(h1);
```

### Why Declarative is Better in React

- **Simplicity:** You focus on _what_ your UI should look like at any given time, not _how_ to make it look that way. React abstracts away the complex DOM manipulation.
- **Maintainability:** Less manual manipulation code means fewer opportunities for bugs and easier-to-understand code.
- **Efficiency:** React can optimize DOM updates more effectively when it has a declarative description of the desired UI state.
- **Scalability:** As applications grow, managing imperative DOM updates becomes unmanageable. Declarative UIs scale much better.

For even a simple project, like the "React Facts" page, using React's declarative approach (with JSX and components) makes building and managing the UI significantly easier and more enjoyable than manual imperative DOM manipulation.

---
## References


