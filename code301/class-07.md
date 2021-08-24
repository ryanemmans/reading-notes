# CLASS 7 NOTES - REST

## ***A Conversation About REST With My Brother***

[https://gist.github.com/brookr/5977550](https://gist.github.com/brookr/5977550)

- - -

#### **1. Who is Roy Fielding?**

- Roy Fielding helped write the first web servers that sent documents across the internet.
- His research explained why the web works the way it does.
- He helped write HTTP, or the specification for the protocol that is used to get pages from servers to browsers.

#### **2. Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?**

- Computers were not initially designed to send information back and forth to each other.
- The primary concern when creating HTTP was to enable users to be able to talk to a small group of machines.
- Now we need machines to be able to tell each other about a resource that might be on yet another machine using a URL.

#### **3. What is the HTTP protocol that Fielding and his friends created?**

- HTTP refers to applying verbs (such as GET) to nouns when computers communicate.
- An example would be when a webpage loads any file type, or noun (such as an image), it has to specify the URL to the image for the browser to GET (verb) the image using HTTP protocol.
- This keeps happening until all resources are obtained and the page is displayed.

#### **4. What does a `GET` do?**

- `GET` describes what a machine would do in relation to retrieving information, or finding machine-readable resources or data.
- When a browser `GET`s a resource for a human, it is asking for a "representation" of that data.

#### **5. What does a `POST` do?**

- `POST` is the verb used if one system needs to **add** something to another system

#### **6. What does `PUT` do?**

- `PUT` is used if a system wants to **replace** something in another system.

#### **7. What does `PATCH` do?**

- `PATCH` will do a partial update on a system.

- - -

## ***API Keys***

- - -

[Geocoding API](https://locationiq.com/)

#### **Did you get your API key?**

- yes

[Weather Bit API](https://www.weatherbit.io/)

#### **Did you get your API key?**

- yes

[Yelp API Docs](https://www.yelp.com/developers/documentation/v3/business_search)

#### **Did you get your API key?**

- yes

[The Movie DB API Docs](https://developers.themoviedb.org/3/getting-started/introduction)

#### **Did you get your API key?**

- yes

- - -

## Things I want to know more about

- What exactly is REST, and how does it tie into HTTP?

[back](../README.md)
