# Web API Basics with Sinatra

### Intro Topics 
* How the request-response cycle works on a server
* How to handle requests from different routes
* A common file structure for a web server
* How to both send and receive JSON-formatted data

## How the Web Works 
> source/s: https://learning.flatironschool.com/courses/3299/pages/how-the-web-works?module_item_id=278730

* Define a client and server
* Explain what an HTTP request is
* Explain the nature of request and response
* Define a static site vs. a dynamic site

## Creating a Sinatra Application
> source/s: https://learning.flatironschool.com/courses/3299/assignments/134039?module_item_id=278741

* Understand how Sinatra simplifies developing web applications
* Receive a request in Sinatra and send different kinds of responses
* Create dynamic routes in Sinatra 

### Application Structure / MVC 
> source/s: https://learning.flatironschool.com/courses/3299/assignments/134040?module_item_id=278736, https://learning.flatironschool.com/courses/3299/pages/video-sinatra-mvc?module_item_id=294227

* Understand the typical file structure for a Sinatra application
* Use the Rerun gem to help speed up development

## Sinatra with Active Record: GET Requests
> source/s: https://learning.flatironschool.com/courses/3299/assignments/134041?module_item_id=278733, https://learning.flatironschool.com/courses/3299/pages/video-sinatra-get?module_item_id=294225

* Handle multiple GET requests in a controller
* Use the params hash to look up data with Active Record
* Send a JSON response using data from an Active Record model
* Use the #to_json method to serialize JSON data

## Sinatra with Active Record: POST/PATCH/DELETE Requests
> source/s: https://learning.flatironschool.com/courses/3299/assignments/134063?module_item_id=278739, https://learning.flatironschool.com/courses/3299/pages/video-sinatra-show-and-destroy?module_item_id=294228, https://learning.flatironschool.com/courses/3299/pages/video-sinatra-create?module_item_id=294224

* Handle non-GET requests in a controller
* Access data in the request body with the params hash
* Perform CRUD actions with Active Record from the controller