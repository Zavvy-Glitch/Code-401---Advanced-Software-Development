# Redux - Asynchronous Actions

- How granular should your reducers be?
  - This could be dependent on the separate reducers for each individual component.

- Pro or Con - multiple reducers can "fire" when a commonly named action is dispatched
  - Pro: that we can fire multiple reducers - reduction in work you'd need to produce.
  - Pro: each reducer can supply separate logic to different components when fired from the dispatch.
  - Con: can produce unwanted side effects

- Name a strategy for preventing the above
  - Ensure you're separating your reducers
  - Introduce `thunk` to handle it asychronously

## Terminology
|Store|Combined Reducers|
|-----|-----------------|
|A store is an immutable object tree in Redux. A store is a state container which holds the application's state. Redux can have only a single store in your application. Whenever a store is created in Redux, you need to specify the reducer.|A helper function turns an object whose values are different reducing functions into a single reducing function you can pass to `createStore`|
