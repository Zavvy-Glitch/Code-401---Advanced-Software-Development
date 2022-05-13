# Redux ToolKit
  ## Usage:
  Redux Toolkit is intended to be a standard in writing redux logic.
    
   - Features:
     - `configureStore()` : wraps `createStore` to provide simplified configuration options and good defaults. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes `redux-thunk` by default, and enables use of the Redux DevTools Extension.
     - `createReducer()`: that lets you supply a lookup table of action types to case reducer functions, rather than writing switch statements. In addition, it automatically uses the `immer` library to let you write simpler immutable updates with normal mutative code, like `state.todos[3].completed = true`
     - `createSlice()`: accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types
      
- What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?
  - Fire off async actions of a higher order component that wraps the app. It'd probably have to be handled in a reducer that places it into the apps `store`. May require `thunk` middleware to handle the async actions.

-  When using a thunk/async action that dispatches the actual action, which do you export from your reducer?
  - Well-written Redux apps don't actually write those action objects inline when we dispatch them. Instead, we use "action creator" functions. An action creator is a function that creates and returns an action object. We typically use these so we don't have to write the action object by hand every time. We then use them by calling the action creator, and then passing the resulting action object directly to `dispatch`.

## Terminology
|MiddleWare|Thunk|
|----------|-----|
|Software that acts as a bridge between an operating system or database and applications, especially on a network|A middleware that lets you call action creators that return a function instead of an action object. That function receives the store's dispatch method, which is then used to dispatch regular synchronous actions inside the function's body once the asynchronous operations have been completed|
