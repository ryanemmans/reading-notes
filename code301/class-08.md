# CLASS 8 NOTES - APIs

## ***RESTful web API design***

[https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

- - -

#### **1. What does REST stand for?**

- REST stands for Representational State Transfer.

#### **2. REST APIs are designed around a ____.**

- *resources*, or any kind of object, data, or service that can be accessed by the client.

#### **3. What is an identifer of a resource? Give an example.**

- An *identifier* of a resource is a URI.
- It is unique to that resource.
- An example would be `https://website.com/orders/1` for say a particular customer order


#### **4. What are the most common HTTP verbs?**

- The most common HTTP verbs are `GET`, `POST`, `PUT`, `PATCH`, and `DELETE`.

#### **5. What should the URIs be based on?**

- When possible, URIs should be based on nouns, or resources.

#### **6. Give an example of a good URI.**

- A good URI example would `https://website.com/orders`, as opposed to `/create-order`.
- In this example, we do not have a verb.

#### **7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?**

- A 'chatty' web API exposes a large number of small resources.
- This requires more requests, which imposes a bigger load.
- An application may need to send multiple requests to find all of the data it requires.
- Data could instead be demoralized and related information could be combined into bigger resources.
- These resources can then be retrieved in a single request.

#### **8. What status code does a successful `GET` request return?**

- A successful `GET` method will usually return an HTTP status code of 200, or "OK".

#### **9. What status code does an unsuccessful `GET` request return?**

- An unsuccessful `GET` request will return an HTTP status code of 406, or "Not Acceptable."

#### **10. What status code does a successful `POST` request return?**

- When a new resource is created by `POST`, it will return an HTTP status code of 201, or "Created."

#### **11. What status code does a successful `DELETE` request return?**

- If a `DELETE` operation is successful, the web server should give a response of HTTP status code 204, or "No Content."

- - -

## ***RegEx***

[https://regexr.com/](https://regexr.com/)

- - -

#### **1. How would you match your name using RegEx?**

- You would begin the string with `^`, and end it with `$`.
- `\w` will match a word character
- I believe it will need to go inside a character class `[`

- - -

## Things I want to know more about

- How does a URI differ from a URL?
- How the heck does RegEx work?

[back](../README.md)
