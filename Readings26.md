# Component Based UI

## Why JSX?
  - Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both.
  - React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.

## Embedding Expressions in JSX
  - You can put any valid JavaScript expression inside the curly braces in JSX.
  
      - Example: In the example below, we embed the result of calling a JavaScript function, formatName(user), into an `<h1>` element
      
       
                 function formatName(user) {
                    return user.firstName + ' ' + user.lastName;
                  }

                    const user = {
                      firstName: 'Harper',
                      lastName: 'Perez'
                  };

                    const element = (
                      <h1>
                        Hello, {formatName(user)}!
                     </h1>
                   );
                   
## JSX as an Expression
  - After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.
  - This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions

            function getGreeting(user) {
              if (user) {
                return <h1>Hello, {formatName(user)}!</h1>;
              }
              return <h1>Hello, Stranger.</h1>;
            }

# Rendering Elements

## Rendering an Element to the DOM
  - Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.
  - To render a React element, first pass the DOM element to ReactDOM.createRoot(), then pass the React element to root.render():

        const element = <h1>Hello, world</h1>;
        const root = ReactDOM.createRoot(
          document.getElementById('root')
        );
        root.render(element);
        
## Updating the Rendered Element
  - React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.
  - With our knowledge so far, the only way to update the UI is to create a new element, and pass it to root.render().

        const root = ReactDOM.createRoot(
          document.getElementById('root')
        );

        function tick() {
          const element = (
            <div>
              <h1>Hello, world!</h1>
              <h2>It is {new Date().toLocaleTimeString()}.</h2>
            </div>
          );
          root.render(element);
        }

        setInterval(tick, 1000);
        
        
