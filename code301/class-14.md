# CLASS 14 NOTES - Authentication

## ***What is OAuth? How the open authorization framework works***

[https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

- - -

#### **1. What is OAuth?**

- OAuth is an authorization framework that describes how servers and services can safely allow authenticated access without sharing the logon credential.

#### **2. Give an example of what using OAuth would look like.**

- An example of OAuth would be if you go on a website and it asks you to log in, you are given the option to log in using another website's login.
- The other website authenticates you, and you are then connected to the original website.
- Two or more services will always be used for one transaction by the end-user.

#### **3. How does OAuth work? What are the steps that it takes to authenticate the user?**

1. Site A connects to site B providing user's verified identity.
2. Site B generates one-time token and secret unique to transaction.
3. Site A gives token and secret to user's client software.
4. Software presents *request* token and secret to authorization provider.
5. After authentication on site A, client is asked to approve authorization transaction to site B
6. User or software approves type of transaction at site A.
7. User is given approved *access* token to site A.
8. User gives approved *access* token to site B.
9. Site A gives *access* token to site B as proof of authentication.
10. Site B gives site A access on behalf of user.
11. Successfully completed transaction is presented to user.

#### **4. What is OpenID?**

- OpenID is about authentication.
- It differs from OAuth in that it enables users to log into machines, whereas OAuth is used for machines logging into other machines on behalf of users.
- In 2014, OpenID Connect became an authentication layer for OAuth.

- - -

## ***Authentication and Authorization Flows***

[https://auth0.com/docs/authorization/flows](https://auth0.com/docs/authorization/flows)

- - -

#### **1. What is the difference between authorization and authentication?**

- Authorization is the process of verifying what the user has access to. (WHAT YOU CAN SEE OR DO)
- Authentication is the process of verifying who a user is. (WHO YOU ARE)

#### **2. What is Authorization Code Flow?**

- Authorization code flow exchanges an Authorization Code for a token.

#### **3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?**

- It is additional security that introduces a secret, or Code Verifier, created by the calling application that can be verified by the authorization server.
- The calling app also creates a transform value called the Code Challenge, which is sent over HTTPS to retrieve an authorization code.
- Malicious attackers cannot exchange the authorization code for a token without the code verifier.

#### **4. What is Implicit Flow with Form Post?**

- This is intended for public clients, or applications which are unable to securely store client secrets.
- No longer considered best practice for requesting access tokens, but does offer streamlined workflow with form post response mode if only an ID token is needed.

#### **5. What is Client Credentials Flow?**

- Client Crdentials Flow is used with machine-to-machine (M2M) applications.
- The app is being authenticated and authorized by the system instead of the user.

#### **6. What is Device Authorization Flow?**

- With Device Authorization Flow, the device asks the user to go to a link to authorize their device.
- This avoids poor user experience.

#### **7. What is Resource Owner Password Flow?**

- This requests that users provide username and password credentials, typically using an interactive form.
- It should only be used when redirect-based flows cannot be used.

- - -

## Things I want to know more about

- How do we implement Auth0 into our applications? What is needed?
- How are different flows programmed, and how do we determine when to use each?

[back](../README.md)
