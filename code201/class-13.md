# CLASS 13 NOTES - Local Storage

## ***The Past, Present, & Future of Local Storage for Web Applications***

- html5doctor.com
- *Code examples referenced from the text*

- - -

Native clients have always held an advantage over web applications with persistent local storage

Cookies can be used for persistant local storage, but have their downsides

- Slow down applications by transmitting same data over and over
- Send data unencrypted over the internet
- Limited to about 4 KB of data, enough to slow down your application

## Local Storage Before HTML5

`userData` allows web pages to store up 64 KB of data per domain

2002 - Adobe introduced "Flash cookies"

2007 - Google launched Gears - open source browser plugin

2009 - `dojox.storage` provided a unified interface

HTML5 set out to provide a standardized API, implemented natively and consistently in multiple browsers without third-party plugins.

## Introducing HTML5 Storage

A way for web pages to store named key/value pairs locally, within the client web browser

- Data persists after exiting site, tab, or browser
- Never transmitted to remote web server
- implemented natively

Supported by the latest versions of all browsers, even Internet Explorer

## Using HTML5 Storage

In the key/value pair, the key is a string

- data can be anything supported by JavaScript, including string, Boolean, integer or float
  - stored as a string
  - `parseInt()` or `parseFloat()` are used for anything that isn't a string

`localStorage` can be treated as an associative array.

- square brackets can be used in place of `getItem` and `setItem`
- Values can be removed
- Keys can be accessed through an index

### Tracking Changes

`storage` event is "trapped" to keep track of when storage area changes

- cannot be canceled

### Limitations

Each origin gets 5 MB of storage by default

- You are storing strings, not data in its original format
- More storage space cannot be requested

## HTML5 Storage in Action

A game for example - Progress can be saved locally, within the browser itself

- Even if browser is closed, reopen and position is rememebered

`localStorage` object is used to save whether there is a game in progress

On page load, `resumeGame()` can be called instead of `newGame()`

Data is stored as strings, any data other than a string needs to be coerced upon retrieval

## Beyond Named Key-Value Pairs

A new API has been standardized and implemented across all major browsers, platforms, and devices.

Future of persistent local storage is competitive

In 2007, Google's "Gears" plugin included an embedded database on "SQLite"

- Web SQL Database then followed
  - Wraps a SQL database and is widely supported on most browsers except Internet Explorer and FireFox

IndexedDB (or Indexed Database API) uses an *object store*

- shares many concepts with a SQL database
- databases have "records" with a set number of "fields" - each with specific datatypes.

[back](../README.md)
