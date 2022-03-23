# Express REST API

## ES6 Classes:
[Source Document](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- Classes are used as templates to create objects by encapsulateing the data with code to work on that data.
- Classes are "special" functions that contain two components: class expressions and class declarations
    - Class Declaration Example:
    ```javascript 
    class Rectangle {
       constructor(height, width) {
           this.height = height;
           this.width = width;
           }
        }
    ```
    - *Hoisting*: The difference between function declarations and class declarations is that while functions can be called in code that appears before they are defined, classes must be defined before they can be constructed. *The following will not work*
    ```javascript
    const p = new Rectangle(); // This will create a ReferenceError

    class Rectangle {}
    ```
     *`*`occurs because while the class is hoisted its values are not initialized*
     
## Express Routing:
[Source Document](https://expressjs.com/en/guide/routing.html)
- Routing refers to how an application's endpoints respond to requests.
    - Express app objects correlate to HTTP methods. IE:
        - GET
        - POST
        - PUT
        - DELETE 
    -*NOTE*: There are more methods than the listed 4 above. You can find the others here at [ExpressJS.com](https://expressjs.com/en/4x/api.html#app.METHOD)
 - Route Paths: In combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions
    ```javascript
    app.get('/', (req, res) => {
        res.send('root')
    })
    
    app.get('/ab?cd', (req, res) => {
        res.send('ab?cd')
    })
    
    app.get(/.*fly$/, (req, res) => {
    res.send('/.*fly$/')
    })
    ```
- Route Parameters: Route parameters are named URL segments that are used to capture the values specified at their position in the URL. The captured values are populated in the req.params object, with the name of the route parameter specified in the path as their respective keys
    ```javascript
    Route path: /users/:userId/books/:bookId
    Request URL: http://localhost:3000/users/34/books/8989
    req.params: { "userId": "34", "bookId": "8989" }
    ```
## Definitions

| MiddleWare | Request Object | Response Object | Application Middleware | Routing Middleware | Test Driven Development | Behavioral Testing |
| ------ | ----- | ----- | ----- | ----- | ----- | ----- |
| Middleware are functions that execute during the lifecycle of a request to the Express server. Each middleware has access to the HTTP request and response for each route (or path) it's attached to. | The request object is the main entry point for an application to issue a request to the Library - all operations on a URL must use a Request object. | Used to send data from the server to the client through an HTTP request | Send requests to the server. `app.use()`, `app.get()`. | bound to an instance of `express.Router()`. | Test Driven Development (TDD)'s main idea is to simply start working on code by writing automated tests BEFORE writing the code that is being tested. | Testing of outputs with out interference of how the software derives them. |

