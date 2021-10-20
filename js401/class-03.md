# CLASS 3 NOTES - Express REST API

***1. Name 3 real world use cases where you’d want to change the request with custom middleware.***

- Printing a message (logging).
- Displaying a request timestamp.
- Triggering an error handler.

***2. True or false: The route handler is middleware?***

- false - Route handlers do not require the `next` argument.

***3. In what ways can a middleware function end the process and send data to the browser?***

- Calling `next();`
- `response.end();`
- `response.status('status code');`

***4. At what point in the request lifecycle can you “inject” middleware?***

- Between the HTTP Method and the Path.

***5. What can cause express to error with “Request headers sent twice, cannot start a second response"***

- Another function tried to set a header or status code.
- You are already in the Body or Finished state.
- A callback may have accidentally been called twice.

***6. Document the following Vocabulary Terms:***

- **Middleware** - functions that have access to the request object (req), the response object (res), and the next function in the application’s request-response cycle.
- **Request Object** - represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers, etc.
- **Response Object** - represents the HTTP response that an Express app sends when it gets an HTTP request.
- **Application Middleware** - bound to an instance of Express by using `app.use()`
- **Routing Middleware** - bound to an instance of `express.Router()`
- **Test Driven Development** - a style of programming interwoven by coding, testing (writing unit tests) and design (refactoring).
- **Behavioral Testing** - aka Black Box Testing - a software testing method in which internal structure / design / implementation of the item being tested is not known to the tester. Compares the input value with the output value and can be functional or non-functional.

- - -

## Preview:

- [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- [Using Express Routing](https://expressjs.com/en/guide/routing.html)
- [Express Routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- JavaScript Classes, sub classes with `extends`
- Constructors
- Setting up routes in Express

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Hoisting
- Generator Methods
- Express Router

***3. What are you most excited about trying to implement or see how it works?***

- Express Router
- Route Middleware
- Login Routes

- - -

Sources:

- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Express Docs](https://expressjs.com/en/guide/writing-middleware.html)
- [NewbeDev](https://newbedev.com/error-can-t-set-headers-after-they-are-sent-to-the-client)
- [Stack Overflow](https://stackoverflow.com/questions/29457008/whats-the-difference-between-application-and-router-level-middleware-when-rou)
- [Agile Alliance](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1))
- [Software Testing Fundamentals](https://softwaretestingfundamentals.com/black-box-testing/)

[back](../README.md)
