# `<Login />` & `<Auth />`

- Why is the Context API useful?
  - Context is a good way to share values between our components without using props every time, but these criteria should not be only one. If some values are needed on different levels of the components tree and for many elements, it will be a good idea to use context for this data.
- Can a component outside of a provider get its context?
  - To access a React context outside of the render function, we can use the useContext hook. We create the UserContext by calling the React. createContext method with a default context value. Then in the Users component, we call the useContext hook with UserContext to accxess the current value of UserContext
- What are some common use cases for using the Context API?
  - Theming, User Language, Authentication
- Describe “Context Hell”
  - A scenario in which an individual extensively uses React.Context creating a multitude of providers for various components.

## Terminology
|Global State|Global Context|Provider|Consumer|
|------------|--------------|--------|--------|
|To put it simply, global state is the data that is shared between all the components within a React application. When the state is changed, or let's say a filter is added, the components re-render accordingly|Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. |Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes. The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers|A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component. Requires a function as a child. The function receives the current context value and returns a React node.|
