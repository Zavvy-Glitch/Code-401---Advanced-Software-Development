# Component Lifecycle / Hook
[Source Information: Using the Effect Hook - React](https://reactjs.org/docs/hooks-effect.html)
## Using the Effect Hook
- Effect Hook lets you perform side effects
- Data fetching, setting up a subscription, and manually changing the DOM in React components are all examples of side effects
- There are two common kinds of side effects in React components: those that don’t require cleanup, and those that do
    - Effects Without Cleanup
        - Network requests, manual DOM mutations, and logging are common examples of effects that don’t require a cleanup
        - We can run them and immediately forget about them
            - Classes:
                - We typically want to perform our effects after React has updated the DOM
                - Why in React classes, we put side effects into componentDidMount and componentDidUpdate
                - Example for Classes:
                    ``` javascript
                    class Example extends React.Component {
                        constructor(props) {
                            super(props);
                            this.state = {
                            count: 0
                            };
                        }

                        componentDidMount() {
                            document.title = `You clicked ${this.state.count} times`;
                        }
                        componentDidUpdate() {
                            document.title = `You clicked ${this.state.count} times`;
                        }

                        render() {
                            return (
                            <div>
                                <p>You clicked {this.state.count} times</p>
                                <button onClick={() => this.setState({ count: this.state.count + 1 })}>
                                Click me
                                </button>
                            </div>
                            );
                        }
                        }
                    ```
               - Example for Hooks:
                    ``` javascript
                    import React, { useState, useEffect } from 'react';

                    function Example() {
                        const [count, setCount] = useState(0);

                        useEffect(() => {
                            document.title = `You clicked ${count} times`;
                        });

                        return (
                            <div>
                                <p>You clicked {count} times</p>
                                <button onClick={() => setCount(count + 1)}>
                                    Click me
                                </button>
                             </div>
                            );
                        }
                        
                - What does useEffect do?
                    - By using this Hook, you tell React that your component needs to do something after render
                    - React will remember the function you passed and call it later after performing the DOM updates

                - Why is useEffect called inside a component?
                    -  Placing useEffect inside the component lets us access the count state variable right from the effect
                    -  We don’t need a special API to read it
                    -  
- Why do we not need more `.html` pages in a multi-page React app?
    - React is not designed to develop multi-page websites. So, we need to create multiple routes to handle multiple views.
- If we wanted a component to show up on every page, where would we put it and why?
  - Outside the `<BrowserRouter/>`
  - Inside the `<BrowserRouter />`, outside a `<Route />`
  - Inside a `<Route />`
- What does routing do with the components that were rendered when a new route is requested?
  - Each router creates a history object that it uses to keep track of the current location and re-renders the application whenever this location changes. For this reason, the other React Router components rely on this history object being present; which is why they need to be rendered inside a router.
The BrowserRouter uses the HTML5 history API to keep the user interface in sync with the URL in the browser address bar.
The history object created by the Router contains a number of properties and one of the location property whose value is also an object. [SRC: Medium](https://medium.com/the-andela-way/understanding-the-fundamentals-of-routing-in-react-b29f806b157e)
- What does `props.children` contain?
  - it is used to display whatever you include between the opening and closing tags when invoking a component? Essentially it'll contain anything you want to pass?
- How do `useState()` and `this.setState()` differ?
  - `setState` merges with the previous state with a new state > no need to pass a full state object. `useState` rewrites the previous state with a new one / does not merge. It will just replace the state. Say you have multiple values, with setState you can set a single value and it can merge with the current existing state. `useState` on the other hand, you have to pass the complete state each time.

## Vocabulary

|State Hook| Mounting and Un-Mounting|
|----------|-------------------------|
|`useState` is a Hook (function) that allows you to have state variables in functional components. You pass the initial state to this function and it returns a variable with the current state value (not necessarily the initial state) and another function to update this value|The main job of React is to figure out how to modify the DOM to match what the components want to be rendered on the screen. React does so by "mounting" (adding nodes to the DOM), "unmounting" (removing them from the DOM), and "updating" (making changes to nodes already in the DOM).|
