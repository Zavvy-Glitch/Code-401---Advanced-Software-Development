# Advanced State with Reducers
[Source: ReactJS Hooks API](https://reactjs.org/docs/hooks-reference.html#usereducer)

What is useReducer?
  - An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method
  - useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one
  - useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks
  - Example: 
    ``` javascript
    const initialState = {count: 0};

    function reducer(state, action) {
      switch (action.type) {
        case 'increment':
          return {count: state.count + 1};
        case 'decrement':
          return {count: state.count - 1};
        default:
          throw new Error();
      }
    }

    function Counter() {
      const [state, dispatch] = useReducer(reducer, initialState);
      return (
        <>
          Count: {state.count}
          <button onClick={() => dispatch({type: 'decrement'})}>-</button>
          <button onClick={() => dispatch({type: 'increment'})}>+</button>
        </>
      );
    }
    ```
Two Different Ways ato Initialize `useReducer`
  - Specifying Initial State
  - Example:
    ``` javascript
     const [state, dispatch] = useReducer(
      reducer,
      {count: initialCount}
    );
    ```
  - Lazy Initialization
  - Example:
    ``` javascript
    function init(initialCount) {
      return {count: initialCount};
    }
    ```
    
## How does the useReducer Hook work?
  - The `useReducer` Hook is used to store and update states, just like the `useState` Hook. It accepts a `reducer` function as its first parameter and the initial state as the second
  - `useReducer` returns an array that holds the current state value and a `dispatch` function to which you can pass an action and later invoke it

## `reducer` Function
  - The JavaScript reduce() method executes a reducer function on each element of the array and returns a single value. The reduce() method accepts a reducer function, which itself can accept up to four arguments
  ``` javascript
  const reducer = (accumulator, currentValue) => accumulator + currentValue;
  [2, 4, 6, 8].reduce(reducer)
  // expected output: 20
  ```
  - In React, useReducer essentially accepts a reducer function that returns a single
  ``` javascript
  const [count, dispatch] = useReducer(reducer, initialState);
  ```
  - The reducer function itself accepts two parameters and returns one value. The first parameter is the current state, and the second is the action. The state is the data we are manipulating. The reducer function receives an action, which is executed by a dispatch function
  ``` javascript
  function reducer(state, action) { }

  dispatch({ type: 'increment' })
  ```
