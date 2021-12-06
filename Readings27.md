# `useState()` Hook:

- How does React differ from vanilla JS/HTML/CSS?
  - Plain JS apps usually start with the initial UI created on the server (as HTML), whereas React apps start with a blank HTML page, and dynamically create the initial state in JavaScript. React requires you to break your UI into components, but plain JS apps can be structured in any way you see fit. [SRC: Framer](https://www.framer.com/blog/posts/react-vs-vanilla-js/)
- What is the primary difference between a function component and a class component?
  - A functional component is just a plain JavaScript function that accepts props as an argument and returns a React element. A class component requires you to extend from React. Component and create a render function which returns a React element. There is no render method used in functional components. [SRC: GeeksForGeek](https://www.geeksforgeeks.org/differences-between-functional-components-and-class-components-in-react/#:~:text=A%20functional%20component%20is%20just,method%20used%20in%20functional%20components.) 

| Terminology | Definition |
| ----------- | ---------- |
| Functional Components | A Functional component is a function that takes props and returns JSX. They do not have state or lifecycle methods. Functional components are easier to read, debug, and test. They offer performance benefits, decreased coupling, and greater reusability. [SRC: ProgrammingWithMosh](https://programmingwithmosh.com/react/react-functional-components/#:~:text=A%20Functional%20component%20is%20a,decreased%20coupling%2C%20and%20greater%20reusability.) |
| Children/ Child Components | Children allow you to pass components as data to other components, just like any other prop you use. The special thing about children is that React provides support through its ReactElement API and JSX [SRC: BuildwithReact](https://buildwithreact.com/article/component-children) |
