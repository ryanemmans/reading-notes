# CLASS 12 NOTES - Socket.io

***1. What is the benefit of transforming data into packets?***

- Packets are smaller pieces of data that are assigned their place in the original data, to allow for reconstruction at the other end of transport. Packet-based networks are the most cost-effective, efficient, and scalable networks for content delivery.

***2. UDP is often refereed to as a connectionless protocol. Why is this?***

- UDP is considered a connectionless protocol because no connection needs to be established between the source and destination before you transmit data. It just sends the data as soon as it's ready and assumes the endpoint receives it all.

***3. Can a socket server application have multiple socket connections?***

- Yes, as long as they are associated with different client-side IP/Port pairs.

***4. Can a socket connection application be connected to multiple socket servers?***

- I believe so. Broadcasting works with multiple servers, but you would need to replace the default adapter.

***5. Can an application be both a socket server and a socket connection?***

- I believe so, I think this would be considered a "peer-to-peer" type system. The server socket accepts connections from other clients and the client socket establishes connections to others.

***6. Document the following Vocabulary Terms:***

- **Observer Pattern** - an object or "subject" that maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.
- **Listener** - function that waits for an event to occur. Is programmed to react to an input or signal by calling the event's handler.
- **Event Handler** - a function that runs when an event fires.
- **Event Driven Programming** - paradigm in which the flow of the program is determined by events such as user actions, sensor outputs, or messages passing from other programs or threads.
- **Event Loop** - executes code, collects and processes events, and executes queued sub-tasks.
- **Event Queue** -  a queue of events (or asynchronous messages) that is waiting to be processed by the receiving program.
- **Call Stack** - data structure that stores information about the active subroutines of a program. AKA execution stack, program stack, control stack, run-time stack, or machine stack.
- **Emit/Raise/Trigger** - to create or publish events (messages) that cause function objects (listeners, or subscribers) to be called to act on said events.
- **Subscribe** - to listen/react to published/fired events sent by the EventEmitter
- **Database** - an organized collection of data structured in a way that it can be easily fetched.

- - -

## Preview:

- [OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)
- [TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk)
- [Web Sockets](https://en.wikipedia.org/wiki/WebSocket)
- [Socket.io Tutorial](https://www.tutorialspoint.com/socket.io/)
- [Socket.io vs Web Sockets](https://www.educba.com/websocket-vs-socket-io/)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Payloads
- Event Driven Programming
- EventEmitter

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- TCP
- Socket.io
- Data packets

***3. What are you most excited about trying to implement or see how it works?***

- Socket.io
- Observer Pattern
- OSI Model

- - -

Sources:

- [TCP/IP](https://users.cs.cf.ac.uk/MatthewsAJ1/Page1.html)
- [FNT Software](https://fntsoftware.com/blog/network-transformation-transitioning-to-packet-technology/)
- [Science Direct](https://www.sciencedirect.com/topics/computer-science/connectionless-protocol)
- [Stack Overflow TCP](https://stackoverflow.com/questions/11129212/tcp-can-two-different-sockets-share-a-port)
- [Socket.io Docs](https://socket.io/docs/v4/broadcasting-events/#with-multiple-socketio-servers)
- [Stack Overflow Sockets](https://stackoverflow.com/questions/2578254/connect-two-client-sockets)
- [Observer Pattern Wiki](https://en.wikipedia.org/wiki/Observer_pattern)
- [Computer Hope](https://www.computerhope.com/jargon/e/event-listener.htm#:~:text=An%20event%20listener%20is%20a,for%20an%20event%20to%20occur.&text=The%20listener%20is%20programmed%20to,specific%20to%20Java%20and%20JavaScript.)
- [Event-Driven Programming Wiki](https://en.wikipedia.org/wiki/Event-driven_programming)
- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)
- [Call Stack Wiki](https://en.wikipedia.org/wiki/Call_stack)
- [Stack Abuse](https://stackabuse.com/handling-events-in-node-js-with-evenemitter/)

[back](../README.md)
