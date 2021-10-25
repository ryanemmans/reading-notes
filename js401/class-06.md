# CLASS 6 NOTES - Authentication

***1. Explain what a “Singleton” is (in Computer Science terms)***

- A class that allows only a single instance of itself to be created and gives access to that created instance. It contains static variables that can accommodate unique and private instances of itself.

***2. Explain how the Singleton pattern can be used with Node modules, specifically with classes***

- You can create two classes, Private and Singleton, which can hide the constructor in the Singleton class by throwing an error. By calling the instance, you would get it as expected. If there is no instance yet, you would call the “private” constructor of the Private class and return the instance. Otherwise, if the instance is already there, you just return it.

  ```js
  class PrivateSingleton {
      constructor() {
          this.message = 'I am an instance';
      }
  }
  class Singleton {
      constructor() {
          throw new Error('Use Singleton.getInstance()');
      }
      static getInstance() {
          if (!Singleton.instance) {
              Singleton.instance = new PrivateSingleton();
          }
          return Singleton.instance;
      }
  }
  module.exports = Singleton;
  ```

***3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?***

- By creating a logger file, we can create a Logger class and a Singleton class. We can use the log method when new instances of an object are created. We can use a get instance method to return our singleton instance. Within the logger, we can export the only singleton Class.

***4. Document the following Vocabulary Terms:***

- **Router Middleware** - used to manage incoming HTTP requests by routing them to the correct handler or code
- **Dynamic Module Loading** - a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory.
- **Singleton Pattern** - represents a single instance of an object. Only one can be created, no matter how many times the object is instantiated. If there’s already an instance, the singleton will create a new one.
- **CRUD -> REST Method Matches** - POST - Create, GET - Read, PUT - Update/Replace, PATCH - Update/Modify, DELETE - Delete.
- **Mock Testing** - creating a fake version of an external or internal service that can stand in for the real one, helping your tests run more quickly and more reliably. When your implementation interacts with an object’s properties, rather than its function or behavior, a mock can be used.

- - -

## Preview:

- [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)
- [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)
- [OWASP Auth Cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
- [bcrypt Docs](https://www.npmjs.com/package/bcrypt)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Basic access authentication
- Encoding vs encryption
- CAPTCHA

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Hash functions
- BCrypt
- TLS Client Authentication

***3. What are you most excited about trying to implement or see how it works?***

- Hashing algorithms
- Implementing multi-factor authentication
- BCrypt

- - -

Sources:

- [Techopedia](https://www.techopedia.com/definition/15830/singleton)
- [Medium, Singleton Pattern](ttps://medium.com/swlh/node-js-and-singleton-pattern-7b08d11c726a)
- [Medium Design Patterns](https://medium.com/@maheshkumawat_83392/node-js-design-patterns-singleton-pattern-series-1-1e0ab71e3edf)
- [Stack Overflow](https://stackoverflow.com/questions/63106648/what-is-router-middleware-in-express)
- [Wikipedia](https://en.wikipedia.org/wiki/Dynamic_loading)
- [REST API Docs](https://www.restapitutorial.com/lessons/httpmethods.html)
- [CircleCi](https://circleci.com/blog/how-to-test-software-part-i-mocking-stubbing-and-contract-testing/)

[back](../README.md)
