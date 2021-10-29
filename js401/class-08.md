# CLASS 8 NOTES - Access Control (ACL)

***1. When is Basic Authorization used vs. Bearer Authorization?***

- Basic auth should be used through HTTPS using SSL encryption. Base-64 encodes a username:password string. Bearer auth is used to gain access tokens which can then make API requests on behalf of a user.

***2. What does the JSON Web Token package do?***

- It defines a compact and self-contained way for securely transmitting information between a client and a server as a JSON object. It is digitally signed using a cryptographic algorithm to ensure that the claims cannot be altered after the token is issued.

***3. What considerations should we make when creating and storing a SECRET?***

- Never store unencrypted secrets in .git repositories
  - Avoid git add * commands on git
  - Add sensitive files in .gitignore
  - Don’t rely on code reviews to discover secrets
  - Use automated secrets scanning on repositories
- Don’t share your secrets unencrypted in messaging systems like Slack
- Store secrets safely
  - Use encryption to store secrets within .git repositories
  - Use environment variables
  - Use "Secrets as a service" solutions
- Restrict API access and permissions
  - Default to minimal permission scope for APIs
  - Whitelist IP addresses where appropriate
  - Use short-lived secrets

***4. Document the following Vocabulary Terms:***

- **encryption** - a way of scrambling data so that only authorized parties can understand the information. The process of converting human-readable plaintext to incomprehensible format.
- **token** - a single string which acts as the authentication of an API request, sent in an HTTP Authorization header.
- **bearer** - any party in possession of a token
- **secret** - digital authentication credentials that grant access to systems or data. These are most commonly API keys, usernames and passwords, or security certificates.
- **JSON Web Token** - an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

- - -

## Preview:

- [RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA)
- [5 steps to RBAC](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)
- [Wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- JWTs
- Basic RBAC concepts
- Bearer middleware

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- RBAC
- Obtaining tokens
- Writing tests (still...)

***3. What are you most excited about trying to implement or see how it works?***

- JWTs
- Implementing RBAC
- 3rd Party APIs

- - -

Sources:

- [Stack Exchange](https://security.stackexchange.com/questions/988/is-basic-auth-secure-if-done-over-https)
- [JWT.io](https://jwt.io/introduction)
- [Akana](https://www.akana.com/blog/what-is-jwt)
- [GitGuardian](https://blog.gitguardian.com/secrets-api-management/)
- [OAuth Docs](https://www.oauth.com/oauth2-servers/differences-between-oauth-1-2/bearer-tokens/)

[back](../README.md)
