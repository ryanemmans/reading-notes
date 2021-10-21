# CLASS 4 NOTES - Data Modeling

***1. Name 3 advantages to Test Driven Development***

- Reductions in defect rates, despite moderate increase in initial development effort.
- Overheads are more than offset by a reduction in effort in projects’ final phases.
- Leads to improved design qualities in code, a higher degree of “internal” or technical quality, for instance improving the metrics of cohesion and coupling

***2. In what case would you need to use `beforeEach()` or `afterEach()` in a test suite?***

- `beforeEach()` is run before *each* test in a `describe`.
  - If each test in your `describe` needs a new copy of the structure because each test is modifying the structure then you should use `beforeEach()` to create the structure anew for each test.
- `afterEach()` is run after *each* test in a `describe`.
  - use `afterEach()` if you need to tear the structure down cleanly.

***3. What is one downside of Test Driven Development?***

- When requirements change, tests must be maintained. This adds to the sometimes slow and time consuming process of TDD. They are "special functions" with expressions and declarations.

***4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?***

- ES6 Classes are a template for creating objects. They encapsulate data with code to work on that data.
- With prototypes, classes are not explicitly defined, but rather derived by adding properties and methods to an *instance* of another class. They allow the creation of an object without first defining its class.

***5. Why REST?***

- REST is much easier than other approaches such as SOAP, which also requires separate server and client programs.
- Since REST is based on standard HTTP operations, it uses verbs with specific meanings such as "get" or "delete" which avoids ambiguity. Resources are assigned individual URIs, adding flexibility.
- With REST, information that is produced and consumed is separated from production and consumption technologies. As a result, REST performs well, is highly scalable, and easy to modify and extend.

***6. Document the following Vocabulary Terms:***

- **Functional Programming** - using functions to the best effect for creating clean and maintainable software. A set of approaches to coding, usually described as a programming paradigm.
- **Object-Oriented Programming (OOP)** - an approach in programming in which data is encapsulated within objects and the object itself is operated on, rather than its component parts.
- **Class** - a template for creating objects. They encapsulate data with code to work on that data. Class syntax has two components: Expressions and declarations.
- **`super`** - keyword that is used to call corresponding methods of super class. This is one advantage over prototype-based inheritance.
- **`this`** - refers to the object it belongs to. Has different values depending on where it is used. Refers to the global object whether in strict mode or not, if alone or in a function.
- **Test Driven Development (TDD)** - a style of programming in which three activities are tightly interwoven: coding, testing, and design (refactoring).
- **Jest** - a JavaScript testing framework. It allows you to write tests with an approachable, familiar and feature-rich API that gives you results quickly.
- **Continuous Integration (CI)** - the practice of automating the integration of code changes from multiple contributors into a single software project. A primary DevOps best practice, allowing developers to frequently merge code changes into a central repository where builds and tests then run.
- **REST** - Representational State Transfer - an architectural style for developing web services.
- **Data Model** - an abstract model that organizes elements of data and standardizes how they relate to one another and to the properties of real-world entities.

- - -

## Preview:

- [sql vs noql](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)
- [nosql vs sql](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)
- [sql modeling techniques](https://www.essentialsql.com/get-ready-to-learn-sql-7-simplified-data-modeling/)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Relational vs Non-relational
- Postgres
- Scaling

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Sequelize
- MySQL
- Use cases of SQL vs NoSQL

***3. What are you most excited about trying to implement or see how it works?***

- PostGres in the terminal
- Visualizing databases
- CouchDB

- - -

Sources:

- [Agile Alliance](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1))
- [Stack Overflow](https://stackoverflow.com/questions/21418580/what-is-the-difference-between-before-and-beforeeach)
- [MDN Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- [Service Objects](https://www.serviceobjects.com/articles-whitepapers/why-rest-popular/)
- [Info World](https://www.infoworld.com/article/3613715/what-is-functional-programming-a-practical-guide.html)
- [Jest](https://jestjs.io/)
- [Atlassian](https://www.atlassian.com/continuous-delivery/continuous-integration)
- [Wikipedia](https://en.wikipedia.org/wiki/Data_model)

[back](../README.md)
