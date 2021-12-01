# Advanced State with Reducers

- How can we ensure that an effect hook runs only once?
  - If you want to run an effect and clean it up only once (on mount and unmount), you can pass an empty array ( [] ) as a second argument. This tells React that your effect doesn't depend on any values from props or state, so it never needs to re-run. 
- Can `useState()` update more than one state variable at the same time?
  - No. You would need multiple useState calls per variable made.
- Is `useState()` synchronous?
  - `useState()` is asynchronous. 

## Terminology
|State Hook|Component Lifecycle|
|----------|-------------------|
|A function that allows you to have state variables in functional components. You pass the initial state to this function and it returns a variable with the current state value (not necessarily the initial state) and another function to update this value|Every React Component has a lifecycle of its own, lifecycle of a component can be defined as the series of methods that are invoked in different stages of the component's existence|
