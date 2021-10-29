# CLASS 9 NOTES - Authorization/Authentication

***1. What header(s) are used in authentication and authorization?***

- A `Basic` authorization header is used in conjunction with a base-64 encoding of username:password. A `Bearer` authorization header is used with a token.

***2. What is safe to put into a JWT?***

- A token should not be used without a signature, which is a basic protection that ensures that the token has not been tampered with. JWT are not encrypted by default, so care must be taken. If you need to include sensitive information inside a token, then an encrypted payload must be used.

***3. How are JWTs validated?***

- You can use any existing middleware for your web framework or an open source third-party library to parse and validate JWTs.

***4. Document the following Vocabulary Terms:***

- **RBAC** - Role-based access control - restricts network access or CRUD capabilities based on a person's role within an organization.
- **User Roles** - refer to the levels of access, or capabilities that employees have to the network. E.g. Admin, Editor, Writer, Generic User.
- **JWT Token** - defines a compact and self-contained way for securely transmitting information between a client and server as a JSON object. This information can be verified and trusted because it is digitally signed using a secret or a public/private key pair.

- - -

## Preview:

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Building a RESTful API with authentication and uthorization
- ACL capabilties and roles
- Using HTTP Clients

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Models within models in a database
- Creating a CLI
- More practice with tests.

***3. What are you most excited about trying to implement or see how it works?***

- 3rd Party Libraries
- Postman
- Webstorm

- - -

Sources:

- [Auth0 Docs](https://auth0.com/docs/security/tokens/json-web-tokens/validate-json-web-tokens)
- [BBVA](https://www.bbva.com/en/json-web-tokens-jwt-how-to-use-them-safely/)
- [Digital Guardian](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)
- [JWT](https://jwt.io/introduction)

[back](../README.md)
