### HTTP methods

When working with external data, such as that from an exernal JSON file with an http header, we can manipulate it with get, post, update, delete, and patch actions. ```get``` allows us to get data, ```post``` allows us to create new data, ```update``` allows us to update the date, ```patch``` is a more specific form of update, and ```delete``` allows us delete data. When writing these methods, we typically need to write these as ```async``` functions that ```await``` the ```fetch``` response of the JSON file.

### HTTP status codes

100 level codes are mainly to tell us information (what stuff is doing), it's not as well known/used. 200 level means something works. 300 means that we're redirecting someone because they're trying to access something they should't. 400 means something is wrong on the client side (404, something on the client side doesn't exist, 401 is unauthorized), 500 level is a server level error (maybe you're trying to connect and the server doesn't know.)