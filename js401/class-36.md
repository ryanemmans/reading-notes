# CLASS 36 NOTES - Application State with Redux

***1. What are the advantages of storing tokens in “Cookies” vs “Local Storage”***

- Tokens in local storage are vulnerable to XSS attacks. Cookies are not accessible via JavaScript, making them less vulnerable. Using the `sameSite` flag can help prevent CSRF attacks.

***2. Explain 3rd party cookies.***

- Third-party cookie are stored under a different domain than the user is currently visiting. They are mostly used to track users between websites and display more relevant ads between websites. Without realizing it, users are creating a "trail of crumbs."

***3. How do pixel tags work?***

- Also known as tracking pixels, they obtain and analyze data that is unknowingly provided by users when visiting a webpage or reading an email. This data can include OS, time visited, website type, client type (browser or email application), IP address, site activities, and screen resolutions.

***4. Document the following Vocabulary Terms:***

- **Cookies** - text files with small pieces of data (e.g.: username / password) that are used to identify your computer as you use a network. Data stored in a cookie is created by the server upon connection, which is labeled with an ID unique to the user and their device.
- **Authorization** - process of granting or denying a user access to resources, taking place after Authentication.
- **Access control** - dictates who’s allowed to access and use company information and resources. Makes sure users are who they say they are and that they have appropriate access to company data.
- **Conditional Rendering** - rendering distinct components depending on the state of your application using if statements or conditional (ternary) operators.

- - -

## Preview:

- [Dan Abramov Redux Tutorials](https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867)
- [World's Easiest Guide to Redux](https://www.freecodecamp.org/news/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6/)
- [Testing Reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)
- [Redux Docs](https://redux.js.org/)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Cookies
- Access Control
- Conditional Rendering

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Redux / reducers
- Jest testing with Redux
- react-cookies

***3. What are you most excited about trying to implement or see how it works?***

- Redux
- Gatsby
- Next.js

- - -

Sources:

- [In Depth Dev](https://indepth.dev/posts/1382/localstorage-vs-cookies)
- [Cookie Script](https://cookie-script.com/all-you-need-to-know-about-third-party-cookies.html)
- [Whatagraph](https://whatagraph.com/blog/articles/tracking-pixel)
- [Kaspersky](https://www.kaspersky.com/resource-center/definitions/cookies)
- [Auth0](https://auth0.com/intro-to-iam/what-is-authorization/)
- [Citrix](https://www.citrix.com/solutions/secure-access/what-is-access-control.html)
- [React Conditional Rendering](https://reactjs.org/docs/conditional-rendering.html)

[back](../README.md)
