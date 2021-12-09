# Redux - Combined Reducers

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
