# CLASS 2 NOTES - Express

***1. What’s the difference between PUT and PATCH?***

- `PUT` is an HTTP request method that is a complete representation of a resource. It creates a new resource or replaces a representation of the target resource with the request payload. Calling it once or several times successively has the same effect.
- `PATCH` is an HTTP request method that can be considered a set of instructions on how to modify a resource. This can be thought of as 'updating.'

***2. Provide links to 3 services or tools that allow you to “mock” an API for development like json-server***

- [Postman](https://learning.postman.com/docs/designing-and-developing-your-api/mocking-data/setting-up-mock/)
- [Stoplight](https://stoplight.io/)
- [Mocky.io](https://designer.mocky.io/)

***3. Compare and contrast Swagger and APIDoc.js***

- Swagger allows you to describe the structure of APIs so that machines can read them. By reading an API’s structure, we can automatically build interactive API documentation.
- ApiDoc creates documentation from API annotations in your source code and includes a default template which uses handlebars, Bootstrap, RequireJS and jQuery for the output of the generated api_data.js and api_project.js as an html-page.

***4. Which HTTP status codes should be sent with each type of (un)successful API call?***

- Status code 100s are informational.
- Status code 200s indicate success.
- Status code 300s indicate redirection where further action is needed by the user.
- Status code 400s indicate a client error.
- Status code 500s indicate a server error.

***5. Compare and contrast SOAP and REST***

- SOAP - Simple Object Access Protocol
  - SOAP was designed before REST, it is a protocol.
  - It requires more bandwidth than REST
  - It only works with XML formats.
  - SOAP ***cannot*** make use of REST.
- REST - Representational State Transfer
  - REST is an architectural pattern
  - It was designed specifically for working with components such as media, files, or even hardware objects.
  - It works with plaintext, XML, HTML, and JSON.
  - REST ***can*** make use of SOAP.

***6. Document the following Vocabulary Terms:***

- **Web Server** - computer software and underlying hardware that accepts requests via HTTP, the network protocol created to distribute web pages, or its secure variant HTTPS. It can be a single computer or an embedded system.
- **Express** - a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.
- **Routing** - a mechanism where HTTP requests are routed to the code that handles them. The Router determines what should happen when a user visits a certain page.
- **WRRC** - Web Request Response Cycle - traces how a user's request flows through the app.

- - -

## Preview:

- [An introduction to NodeJS and Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)
- [What is NPM?](https://docs.npmjs.com/about-npm)
- [What is TDD](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1))
- [CI / CD](https://www.youtube.com/watch?v=xSv_m3KhUO8)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Express as a Node.js framework
- Creating route handlers
- Writing tests

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Middleware
- CI/CD with testing
- Webhooks

***3. What are you most excited about trying to implement or see how it works?***

- CI/CD
- Building APIs
- Swagger

- - -

Sources:

- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Amadeus for Developers](https://developers.amadeus.com/blog/helpful-tools-to-create-mock-servers)
- [Stackshare.io](https://stackshare.io/stackups/apidocjs-vs-swagger-inspector)
- [Guru99](https://www.guru99.com/comparison-between-web-services.html)
- [Wikipedia](https://en.wikipedia.org/wiki/Web_server)

[back](../README.md)
