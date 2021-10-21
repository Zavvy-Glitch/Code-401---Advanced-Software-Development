# Express REST API

1. Name 3 real world use cases where you’d want to change the request with custom middleware
    - Logging Messages
    - Validation of Data
    - Time Stamping Requests
  
2. True or false: The route handler is middleware? 
    - False
  
3. In what ways can a middleware function end the process and send data to the browser?
    - Usage of `next()` or by implementing `res.end`,`res.send`, etc
  
4. At what point in the request lifecycle can you “inject” middleware?
    - Bewteen HTTP methods and the `/path` intended

5. What can cause express to error with “Request headers sent twice, cannot start a second response”
    - another function setting a header / status code
    - Callback may have been called twice

## Define the following

| MiddleWare | Request Object | Response Object | Application Middleware | Routing Middleware | Test Driven Development | Behavioral Testing |
| ------ | ----- | ----- | ----- | ----- | ----- | ----- |
| Middleware are functions that execute during the lifecycle of a request to the Express server. Each middleware has access to the HTTP request and response for each route (or path) it's attached to. | The request object is the main entry point for an application to issue a request to the Library - all operations on a URL must use a Request object. | Used to send data from the server to the client through an HTTP request | Send requests to the server. `app.use()`, `app.get()`. | bound to an instance of `express.Router()`. | Test Driven Development (TDD)'s main idea is to simply start working on code by writing automated tests BEFORE writing the code that is being tested. | Testing of outputs with out interference of how the software derives them. |

### PREVIEW
 - [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
 - [Using Express Routing](https://expressjs.com/en/guide/routing.html)
 - [Express Routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)

