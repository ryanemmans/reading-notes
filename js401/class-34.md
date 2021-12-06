# CLASS 34 NOTES - API Integration

***1. How do bearer tokens work?***

- They are a single string which act as the authentication of an API request, sent in an HTTP “Authorization” header. They are a much simpler way of making API requests, since they don’t require cryptographic signing of each request.

***2. Describe express middleware***

- It is a function that has access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next. Middleware can execute any code, make changes to req/res objects, end the req/res cycle, and call the next middleware function in the stack.

***3. What is a JWT?***

- It is an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed.

***4. Document the following Vocabulary Terms:***

- **role based access control** - RBAC restricts network access based on a someone's role. The roles in RBAC refer to the levels of access that employees have to the network.
- **http cookies** - (web cookies or browser cookies) are small pieces of data that a server sends to a user's web browser. The browser may store the cookies and send them back to the same server with later requests. Typically, an HTTP cookie is used to tell if two requests come from the same browser.

- - -

## Preview:

***1. Which 3 things had you heard about previously and now have better clarity on?***

- JWTs
- RBAC
- Express middleware

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Redux
- RBAC in React
- react-cookies

***3. What are you most excited about trying to implement or see how it works?***

- Redux
- BlueprintJS
- JWTs in React

- - -

Sources:

- [OAuth](https://www.oauth.com/oauth2-servers/differences-between-oauth-1-2/bearer-tokens/)
- [Express](https://expressjs.com/en/guide/using-middleware.html)
- [JWT](https://jwt.io/introduction)
- [Digital Guradian](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)
- [MDN HTTP cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)

[back](../README.md)
