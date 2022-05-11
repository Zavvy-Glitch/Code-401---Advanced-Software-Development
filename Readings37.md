# Redux - Combined Reducers

What are they?
  - "it is a utility function to simplify the most common use case when writing Redux reducers" - redux.js.org

## Defining State Shape:
  - Two Ways to define `initial state`
    - `createStore` function can take `preloadedState` as it's second argument.
      - intended to initialize the store with state stored from else where. IE: localStorage.
    - other way is for the root reducer to return initial state value when the argument is `undefined`
  - `combineReducers` takes in an object full of reducer functions, and creates a function that spits out a corresponding state object with matching keys.
      - example:
      ```javascript
      // reducers.js
      export default theDefaultReducer = (state = 0, action) => state
      export const firstNamedReducer = (state = 1, action) => state
      export const secondNamedReducer = (state = 2, action) => state

      // rootReducer.js
      import { combineReducers, createStore } from 'redux'

      import theDefaultReducer, {
        firstNamedReducer,
        secondNamedReducer
      } from './reducers'

      // Use ES6 object literal shorthand syntax to define the object shape
      const rootReducer = combineReducers({
        theDefaultReducer,
        firstNamedReducer,
        secondNamedReducer
      })

      const store = createStore(rootReducer)
      console.log(store.getState())
      // {theDefaultReducer : 0, firstNamedReducer : 1, secondNamedReducer : 2}
      ```
      

- Why choose Redux instead of the Context API for global state?
  - Redux would allow you to persist state in a local storage straight out of the box, provides full inspection and control capabilities to the development tooling so that product developers can build custom tools for their apps, pass action objects over the network to implement collaborative environments without dramatic changes to how the code is written.

- What is the purpose of a reducer?
  - A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. We have tools, like Redux, that help manage an application's state changes in a single store so that they behave consistently
  
- What does an action contain?
  - A type / payload. The action describes what happened and it is the reducer's job to return the new state based on that action
  
- Why do we need to copy the state in a reducer?
  - If the new state is different, the reducer must create new object, and making a copy is a way to describe the unchanged part

## Terminology
|Immutable State|Time Travel in Redux|Action Creator|Reducer|Dispatch|
|---------------|--------------------|--------------|-------|--------|
|A state in which a value cannot be changed once it’s created|The ability step forward and backward through the state of you application, empowering the developer understand exactly what is happening at any point in the app’s lifecycle|An action creator is a function that literally creates an action object. In Redux, action creators simply return an action object and pass the argument value if necessary|A pure function that takes an action and the previous state of the application and returns the new state|A function that receives the store's dispatch method, which is then used to dispatch regular synchronous actions inside the function's body once the asynchronous operations have been completed|
