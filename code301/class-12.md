# CLASS 12 NOTES - CRUD

## ***Which HTTP Status Code to Use for Every CRUD App***

[https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

- - -

#### **1. In your own words, describe what each group of status code represents:**

- 100’s = Status codes 100-199 are informational.
  - They provide information to the client in regard to receiving a request in which the server will attempt to comply.
- 200’s = Status codes 200-299 are success codes.
  - The client is being told that it's request has been accepted or that it met validation requirements.
- 300’s = Status codes 300-399 are redirection codes.
  - The client is being told their request no longer exists at the specified location
- 400’s = Status codes 400-499 are *client* error codes.
  - These requests from client to server are invalid.
  - Incorrect input is being sent from the client.
  - Causes for errors are numerous.
- 500’s = Status codes 500-599 are *server* error codes.
  - These caused be caused by a server being overwhelmed or unreachable behind proxies.
  - They are sometimes related to client requests.
  - Usually the client can retry the same request.

#### **1. What is a status code 202?**

- A status code 202 means 'accepted' and is often used for asynchronous processing.
- This tells the client the request was valid, but is still processing.

#### **2. What is a status code 308?**

- A status code 308 is a permanent redirect.
- It asks the client to use a different URL to access the resource.

#### **3. What code would you use if an update didn’t return data to a client?**

- In this instance, a status code 204 (No Content) would be used.

#### **4. What code would you use if a resource used to exist but no longer does?**

- A status code 410 (Gone) tells us that the resource existed in the past, but it has been deleted or moved to an unknown location.

#### **5. What is the ‘Forbidden’ status code?**

- 403 Forbidden is when the client does not have permissions to access a resource, despite authorizing itself.

- - -

## ***Build A REST API With Node.js, Express, & MongoDB - Quick***

[https://www.youtube.com/watch?v=fgTGADljAeg&ab_channel=WebDevSimplified](https://www.youtube.com/watch?v=fgTGADljAeg&ab_channel=WebDevSimplified)

- - -

#### **1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?**

- When we deploy our application, we are going to want to use something that is not our localhost.

#### **2. What is middleware?**

- Middleware is essentially code that runs when the server gets a request but before it gets passed to your routes.

#### **3. What does app.use(express.json()) do?**

- This allows our server to accept JSON as a *body* instead of git or post element.

#### **4. What does the /:id mean in a route?**

- Because it has a colon `:`, it means that it is a parameter.
- `req.params.id` would give us access to anything passed in after the first slash `/`.

#### **5. What is the difference beween PUT and PATCH?**

- PUT would update *all* information at once.
- PATCH will only update specific information based on what the user is passing such as subscriber name.

#### **6. How do you make a default value in a schema?**

- In your schema inside the key you want to set to default, you would just use `default:` value.
- In the example of a date, the default value could be set to `Date.now`.

#### **7. What does a 500 error status code mean?**

- A 500 status code means that there is an error on the server, causing the transaction not to work.
- This means it has nothing to do with the actual user or client using the API.

#### **8. What is the difference between a status 200 and a status 201?**

- A 200 only means that everything was successful without any specification.
- A 201 status means that an object has been successfully created and is more specific than a 200.
- You should always use a 201 when using the `post` route.

- - -

## Things I want to know more about

- Would we ever use status codes 100-199 or 300-399 in a try/catch?

[back](../README.md)
