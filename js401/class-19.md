# CLASS 19 NOTES - AWS: Events

***1. Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server***

- Both are used to set up REST APIs as well as web applications. Express applications can also be run in a serverless fashion using API Gateway and Lambda functions.

***2. List the AWS Database offerings and talk about the pros and cons of each***

- RDS - Managed Relational Database Service
  - Pros: for MySQL, PostgreSQL, MariaDB, Oracle BYOL, or SQL Server, easy to use
  - Cons: downtime required for scaling, lacks automation, CPU / Storage performance not guaranteed
- DynamoDB - NoSQL Database Service
  - Pros: serverless, high performance at any scale, free
  - Cons: only deployable on AWS, no table joins, limited querying data
- Redshift - Data Warehouse
  - Pros: fast and simple, cost effective, performance and scalability
  - Cons: not a multi-cloud solution, not a serverless architecture
- Database Migration Service - Data Migration
  - Pros: minimal downtime, scalability, user friendly
  - Cons: - network dependent bandwidth, analytics migration needs improvement
- ElastiCache - In-Memory Data Store
  - Pros: deploy, operate, and scale, open source compatible, fully managed
  - Cons: limited to Amazon hosted services, steep learning curve, expensive

***3. What’s the difference between a FIFO and a standard queue?***

- Standard queues provide *at-least-once* delivery - each message is delivered at least once. FIFO queues provide *exactly-once* processing, - each message is delivered once and remains available until a consumer processes it and deletes it.

***4. How can the server be assured a message was properly received?***

- With a status code of 200.

***5. Document the following Vocabulary Terms:***

- **Serverless API** - a method of providing backend services on an as-used basis where companies are charged based on usage.
- **Triggers** - a mechanism that initiates an action when an event occurs such as reaching a certain time or date or upon receiving some type of input. Generally causes a program routine to be executed.
- **Dynamo vs Mongo**
  - Dynamo: scalable, hosted NoSQL DB, provided by Amazon
    - Uses tables --> collections of items --> collections of attributes
    - Easy setup and installation
    - Supports Java, JavaScript, Swift, Node.js, .NET, PHP, Python
    - Security through IAM access/secret key pair
  - Mongo: One of the most famous stores of documents
    - Uses JSON documents --> schema-free data, no need for predefined structure
    - Difficult to setup and install, cloud hosted Atlas makes it easier
    - Supports almost **ALL** major programming languages
    - Weaker security, user authentication should be enabled.
- **Dynamoose vs Mongoose**
  - Dynamoose: a modeling tool for Amazon's DynamoDB. Heavily inspired by Mongoose with familiar syntax.
    - Type safety, high level API, easy to use syntax
    - Ability to transform data before saving or retrieving documents
    - Strict data modeling (validation, required attributes, and more)
    - Support for DynamoDB Transactions, Powerful Conditional/Filtering Support, Callback & Promise support
  - Mongoose: mongoDB object modeling for node.js
    - Straight-forward, schema-based
    - Used for modeling application data
    - Includes built-in type casting, validation, query building, business logic hooks and more

- - -

## Preview:

- [SQS and SNS Basics](https://www.youtube.com/watch?v=UesxWuZMZqI)
- [AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Dynamoose
- SQS - queueing service
- SNS - Pub/Sub

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- SQS / SNS
- Decoupling
- AWS SDK

***3. What are you most excited about trying to implement or see how it works?***

- React
- Sass
- Next.js

- - -

Sources:

- [Going Serverless](https://aws.amazon.com/blogs/compute/going-serverless-migrating-an-express-application-to-amazon-api-gateway-and-aws-lambda/)
- [Express / Lambda](https://aws.amazon.com/blogs/aws/running-express-applications-on-aws-lambda-and-amazon-api-gateway/)
- [AWS Databases](https://aws.amazon.com/free/database/?trk=ps_a134p000007CdBGAA0&trkCampaign=acq_paid_search_brand&sc_channel=PS&sc_campaign=acquisition_US&sc_publisher=Google&sc_category=Database&sc_country=US&sc_geo=NAMER&sc_outcome=acq&sc_detail=aws%20database%20solution&sc_content=Cloud%20Database_e&sc_matchtype=e&sc_segment=548665196142&sc_medium=ACQ-P|PS-GO|Brand|Desktop|SU|Database|Solution|US|EN|Text&s_kwcid=AL!4422!3!548665196142!e!!g!!aws%20database%20solution&ef_id=CjwKCAiAm7OMBhAQEiwArvGi3ESp5_-t6HhL3WkXByED_ugxeMM0X8cReurVqvpZl8FfBhvoV1ccJxoC5YEQAvD_BwE:G:s&s_kwcid=AL!4422!3!548665196142!e!!g!!aws%20database%20solution)
- [Saras](https://sarasanalytics.com/blog/amazon-rds-pros-and-cons)
- [Trigent](https://blog.trigent.com/when-to-opt-for-aws-dynamodb/)
- [CloudZero](https://www.cloudzero.com/blog/amazon-elasticache)
- [Amazon SQS FAQs](https://aws.amazon.com/sqs/faqs/#:~:text=Standard%20queues%20provide%20at%2Dleast,processes%20it%20and%20deletes%20it.)
- [CloudFlare](https://www.cloudflare.com/learning/serverless/what-is-serverless/)
- [PCMag](https://www.pcmag.com/encyclopedia/term/trigger)
- [EDUCBA](https://www.educba.com/mongodb-vs-dynamodb/)

[back](../README.md)
