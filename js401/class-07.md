# CLASS 7 NOTES - Bearer Authorization

***1. Write the following steps in the correct order:***

- 1) Register your application to get a client_id and client_secret
- 2) Ask the client if they want to sign in via a third party
- 3) Redirect to a third party authentication endpoint
- 4) Receive authorization code
- 5) Make a request to the access token endpoint
- 6) Receive access token
- 7) Make a request to a third-party API endpoint

***2. What can you do with an authorization code?***

- An authorization code is a temporary, one-time use code that a client can exchange for an access token.

***3. What can you do with an access token?***

- Applications use access tokens to make API requests on behalf of a user. An access token represents the authorization of a specific application to access specific parts of a user’s data.

***4. What’s a benefit of using OAuth instead of your own basic authentication?***

- OAuth enables apps to obtain limited access (scopes) to a user's data without giving away a user's password. It seperates authentication from authorization and supports multiple use cases addressing different device capabilities.

***5. Document the following Vocabulary Terms:***

- **Client ID** - a public identifier for applications.
- **Client Secret** - a secret known only to the application and the authorization server. Must be sufficiently random to not be guessable.
- **Authentication Endpoint** - a security mechanism used to verify the identity of a network's external or remote connecting device, which can include laptops, smartphones, tablets, and servers.
- **Access Token Endpoint** - where apps make a request to get an access token for a user. Describes how to verify token requests and how to return the appropriate response and errors.
- **API Endpoint** - the point of entry in a communication channel when an API and a server are interacting. The means from which the API can access the resources they need from a server to perform their task. In other words, A URL of a server or service.
- **Authorization Code** - a temporary code that the client will exchange for an access token.
- **Access Token** - used in token-based authentication to allow an application to access an API after a user successfully authenticates and authorizes access.

- - -

## Preview:

- [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)
- [Intro to JWT](https://jwt.io/introduction/)
- [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)
- [npm jsonwebtoken docs](https://www.npmjs.com/package/jsonwebtoken)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- JSON Web Tokens
- Secrets
- Basic vs Bearer Auth

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Headers, Payload, Signatures
- base64 / Encoding
- Hashing

***3. What are you most excited about trying to implement or see how it works?***

- OAuth
- JWTs
- Bearer schema

- - -

Sources:

- [Auth0 Docs](https://auth0.com/docs/authorization/flows/authorization-code-flow)
- [OAuth](https://www.oauth.com)
- [Okta Developer](https://developer.okta.com/blog/2017/06/21/what-the-heck-is-oauth)
- [IoTone](https://www.iotone.com/term/end-point-authentication/t219)
- [RapidAPI](https://rapidapi.com/blog/api-glossary/endpoint/)

[back](../README.md)
