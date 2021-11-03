# Socket.io

1. What is the benefit of transforming data into packets?
    - Packet switching is a method for communication over a network in which the data being sent is split into smaller pieces, called packets. Each packet is assigned its place in the original data, to allow for reconstruction at the other end, along with the source and destination sockets. This accommodates various bandwidths, to allow for multiple routes to a destination, and to retransmit the pieces of data which are interrupted or lost 
      - [Source: UITS](https://kb.iu.edu/d/anyq)

2. UDP is often referred to as a connectionless protocol. Why is this?
    - No connection needs to be established between the source and destination before you transmit data. UDP does not have a mechanism to make sure that the payload is not corrupted. As a result, the application must take care of data integrity all by itself
      - [Source: Science Direct](https://www.sciencedirect.com/topics/computer-science/connectionless-protocol#:~:text=UDP%20is%20a%20connectionless%20protocol,data%20integrity%20all%20by%20itself.)

3. Can a socket server application have multiple socket connections?
    - It is possible to have multiple TCP sockets listen on the same port number. There is a caveat to this though, each socket on the same server listening on the same port number must be associated with a different IP address
      - [Source: Quora](https://www.quora.com/Can-a-socket-of-a-server-be-used-by-multiple-clients-simultaneously#:~:text=It%20is%20possible%20to%20have%20multiple%20TCP%20sockets%20listen%20on,with%20a%20different%20IP%20address.)

4. Can a socket connection application be connected to multiple socket servers?
    - Yes - you need one socket for each connection. A socket is a client IP address + client port + server IP address + server port combination. If a client is talking to multiple servers, it is using multiple ports on the client machine 
      - [Source: StackOverflow](https://stackoverflow.com/questions/8798874/can-many-servers-communicate-with-one-client-on-one-socket/8798912)

5. Can an application be both a socket server and a socket connection
    - If you want to have a "peer-to-peer" type system, then you just have each client run both a client and a server socket - the server socket for accepting connections from other clients and the client socket for establishing connections to others
      - [Source: StackOverflow](https://stackoverflow.com/questions/2578254/connect-two-client-sockets#:~:text=If%20you%20want%20to%20have,for%20establishing%20connections%20to%20others.)

| Termimnology | Definitions |
| ------------ | ----------- |
| Observer Pattern | The observer pattern is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods |
| Listener | Indicates a readiness to accept client connection requests. It transforms an active socket into a passive socket. Once called, socket can never be used as an active socket to initiate connection requests. Calling listen() is the third of four steps that a server performs to accept a connection |
| Event Handler | When an event occurs, you can create an event handler which is a piece of code that will execute to respond to that event. An event handler is also known as an event listener. It listens to the event and responds accordingly to the event fires. |
| Event Driven Programming |  is a programming paradigm in which the flow of the program is determined by events such as user actions (mouse clicks, key presses), sensor outputs, or message passing from other programs or threads. Event-driven programming is the dominant paradigm used in graphical user interfaces and other applications (e.g., JavaScript web applications) that are centered on performing certain actions in response to user input. |
| Event Loop | is the secret behind JavaScript’s asynchronous programming. JS executes all operations on a single thread, but using a few smart data structures, it gives us the illusion of multi-threading. Let’s take a look at what happens on the back-end. |
| Event Queue | is a repository where events from an application are held prior to being processed by a receiving program or system. Event queues are often used in the context of an enterprise messaging system.|
| Call Stack | is a stack data structure that stores information about the active subroutines of a computer program. This kind of stack is also known as an execution stack, program stack, control stack, run-time stack, or machine stack, and is often shortened to just "the stack". |
| Emit/Raise/Trigger |
| Subscribe | is another classic pattern where senders of messages, called publishers, do not program the messages to be sent directly to specific receivers, called subscribers. Messages are published without the knowledge of what or if any subscriber of that knowledge exists. |
| database | is a facility in computer science that allows client software to talk to database server software, whether on the same machine or not. A connection is required to send commands and receive answers, usually in the form of a result set. Connections are a key concept in data-centric programming. |
