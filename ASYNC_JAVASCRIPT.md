### HTTP methods

When working with external data, such as that from an exernal JSON file with an http header, we can manipulate it with get, post, update, delete, and patch actions. ```get``` allows us to get data, ```post``` allows us to create new data, ```update``` allows us to update the date, ```patch``` is a more specific form of update, and ```delete``` allows us delete data. When writing these methods, we typically need to write these as ```async``` functions that ```await``` the ```fetch``` response of the JSON file.

### HTTP status codes

100 level codes are mainly to tell us information (what stuff is doing), it's not as well known/used. 200 level means something works. 300 means that we're redirecting someone because they're trying to access something they should't. 400 means something is wrong on the client side (404, something on the client side doesn't exist, 401 is unauthorized), 500 level is a server level error (maybe you're trying to connect and the server doesn't know.)

### Synchronous Code v Async

Synchronous code goes from top to bottom, each piece of code runs and then the next piece does. Asynchronous code flows similarly except certain lines of code will then run separately and then return something like an API response - which takes longer - while the rest of the code flow continues. Unless async/await is used, there will be different scripts running at once. 

### Timers

setTimeout() and setInterval() are the two main methods for timers in Javascript. ```setTimeout()``` takes in a function to call, the number of milliseconds it takes before the function executes, as well as any other parameters needed. ```setInterval()``` takes in parameters the exact same way but executes the function after every interval of milliseconds. To close either, running the globally defined ```clearTimeout()``` method will stop the timeout or the interval. It is worth noting that these methods are both asynchronous.

### Promises

A promise is a way of handling the response from asynchonous code, such as a GET request from an API. They're often used for user input. There is always an accepted case and a rejected case. Either way, one will resolve, so it would be worth using these within a try catch block.


###