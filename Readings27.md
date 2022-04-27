# `useState()` Hook:

- Why Hooks?
  -  Hooks let us organize the logic inside a component into reusable isolated units
  -  Hooks apply the React philosophy (explicit data flow and composition) inside a component, rather than just between the components
  -  Unlike patterns like render props or higher-order components, Hooks don’t introduce unnecessary nesting into your component tree

- What Are Hooks?
  - A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components
  - Hooks let you use React features (like state) from a function — by doing a single function call. React provides a few built-in Hooks exposing the “building blocks” of React: state, lifecycle, and context
  - Hooks are regular JavaScript functions, you can combine built-in Hooks provided by React into your own “custom Hooks”
    - This lets you turn complex problems into one-liners and share them across your application.

- How does React differ from vanilla JS/HTML/CSS?
  - Plain JS apps usually start with the initial UI created on the server (as HTML), whereas React apps start with a blank HTML page, and dynamically create the initial state in JavaScript. React requires you to break your UI into components, but plain JS apps can be structured in any way you see fit. [SRC: Framer](https://www.framer.com/blog/posts/react-vs-vanilla-js/)
 
- What is the primary difference between a function component and a class component?
  - A functional component is just a plain JavaScript function that accepts props as an argument and returns a React element. A class component requires you to extend from React. Component and create a render function which returns a React element. There is no render method used in functional components. [SRC: GeeksForGeek](https://www.geeksforgeeks.org/differences-between-functional-components-and-class-components-in-react/#:~:text=A%20functional%20component%20is%20just,method%20used%20in%20functional%20components.) 

| Terminology | Definition |
| ----------- | ---------- |
| Functional Components | A Functional component is a function that takes props and returns JSX. They do not have state or lifecycle methods. Functional components are easier to read, debug, and test. They offer performance benefits, decreased coupling, and greater reusability. [SRC: ProgrammingWithMosh](https://programmingwithmosh.com/react/react-functional-components/#:~:text=A%20Functional%20component%20is%20a,decreased%20coupling%2C%20and%20greater%20reusability.) |
| Children/ Child Components | Children allow you to pass components as data to other components, just like any other prop you use. The special thing about children is that React provides support through its ReactElement API and JSX [SRC: BuildwithReact](https://buildwithreact.com/article/component-children) |
