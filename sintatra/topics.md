# Web API Basics with Sinatra

* How the request-response cycle works on a server
 * Define a client and server
 * Explain what an HTTP request is
 * Explain the nature of request and response
 * Define a static site vs. a dynamic site

* How to handle requests from different routes
* A common file structure for a web server
* How to both send and receive JSON-formatted data

* Understand how Sinatra simplifies developing web applications
* Receive a request in Sinatra and send different kinds of responses
* Dynamic routes in Sinatra
* Handle non-GET requests in a controller
* Access data in the request body with the params hash
* Perform CRUD actions with Active Record from the controller

## Sinatra with Active Record: GET Requests
> source/s: https://learning.flatironschool.com/courses/3299/assignments/134041?module_item_id=278733

how would i Handle multiple GET requests in a controller?

Use the params hash to look up data with Active Record
Send a JSON response using data from an Active Record model
Use the #to_json method to serialize JSON data