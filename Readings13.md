# Socket.IO Chat
  STEPS TO STARTUP A Socket.IO CHAT
  
  [Source: Socket.IO](https://socket.io/get-started/chat/)
  - `npm init -y`: to create a package.json file
    ```javascript
      {
        "name": "socket-chat-example",
        "version": "0.0.1",
        "description": "my first socket.io app",
        "dependencies": {}
      }
      ```
      
  - `npm install express@4`: this will populate the express library as a dependency
  - `touch index.js`: this index file will serve as an entry point
 
    ```javascript
        const express = require('express');
        const app = express();
        const http = require('http');
        const server = http.createServer(app);

        app.get('/', (req, res) => {
          res.send('<h1>Hello world</h1>');
        });

        server.listen(3000, () => {
          console.log('listening on *:3000');
        });
        ```
            - Express initializes app to be a function handler that you can supply to an HTTP server.
            - We define a route handler / that gets called when we hit our website home.
            - We make the http server listen on port 3000.
  - if you run node index.js from your cli you should see `listening on *:3000`
  - if you go to `http://localhost:3000` on your browser you should see `Hello world`

  - refactor this part of your code in the index.js file:
    ``` javascript 
       app.get('/', (req, res) => {
          res.send('<h1>Hello world</h1>');
        });
        
        TO THIS:
        app.get('/', (req, res) => {
          res.sendFile(__dirname + '/index.html');
        });
    ```
  - below the `app.get` you'll need this code
    ```javascript
      <!DOCTYPE html>
      <html>
        <head>
          <title>Socket.IO chat</title>
          <style>
            body { margin: 0; padding-bottom: 3rem; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; }

            #form { background: rgba(0, 0, 0, 0.15); padding: 0.25rem; position: fixed; bottom: 0; left: 0; right: 0; display: flex; height: 3rem; box-sizing: border-box; backdrop-filter: blur(10px); }
            #input { border: none; padding: 0 1rem; flex-grow: 1; border-radius: 2rem; margin: 0.25rem; }
            #input:focus { outline: none; }
            #form > button { background: #333; border: none; padding: 0 1rem; margin: 0.25rem; border-radius: 3px; outline: none; color: #fff; }

            #messages { list-style-type: none; margin: 0; padding: 0; }
            #messages > li { padding: 0.5rem 1rem; }
            #messages > li:nth-child(odd) { background: #efefef; }
          </style>
        </head>
        <body>
          <ul id="messages"></ul>
          <form id="form" action="">
            <input id="input" autocomplete="off" /><button>Send</button>
          </form>
        </body>
      </html>
    ```
  - Restart your index.js and you should see a input field at the bottom along with a send button

# Rooms and NameSpaces

[Rooms&NameSpaces Source](https://socket.io/docs/v4/rooms/)

  - to join a room
    ``` javascript
    io.on("connection", (socket) => {
      socket.join("some room");
    });
    ```
  - to broadcast/emit to a specific room
    ``` javascript
      io.to("some room").emit("some event");
    ```
  - you can also emit to multiple rooms at the same time
     ``` javascript
      io.to("room1").to("room2").to("room3").emit("some event");
     ```
    

# Socket Emit CheatSheet

  [CheatSheet Source](https://socket.io/docs/v4/emit-cheatsheet/)
  
  - Reserved Events!:
    - connect
    - connect_error
    - disconnect
    - disconnecting
    - newListener
    - removeListener
