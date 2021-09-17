# Web API Basics with Sinatra

## Intro Topics 
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

## Questions

Q: In the request/response cycle, the ______ (usually the browser) sends a
request, and the _____ returns a response. (client, server)

Q: A completely specified route consists of two parts: the _______ (which
specifies the type of action being requested) and the _________ (also known as
the resource). (HTTP verb, path)

Q: To define a **dynamic** route, we need to include a/an __________ in the
path. (parameter/named parameter)

Q: Which of the following can be accessed from the `params` hash? (select all that apply)

*a) Values of named parameters defined in a route
*b) User-provided information (e.g., from a form)
*c) Information to be passed in the body of a `POST` or `PATCH` request.
d) Metadata about a server request

Q: Match each of the files/folders below with what it's responsible for.

Options:

a) `app/models`
b) `config`
c) `db/migrate`
d) `db/seed`
e) `Gemfile`
f) `Rakefile`

Descriptions:

* Contains code that accesses and updates data in our database
* Contains for environment setup, like requiring files/gems, and establishing a connection to the database
* Contains code that is responsible for creating and altering the structure of the database
* Allows us to easily add sample data to the database
* Lists all the dependencies for our application
* Contains code for tasks we can run from the command line

Q: In order to set up the MVC architecture in a Sinatra app, we need to include
code to run the controller (e.g., `run ApplicationController`) in the
____________ file. (config.ru)

Q: In the code snippet below, what goes inside the parentheses? (params[:id])

```rb
  get '/recipes/:id' do
    recipe = Recipe.find(_________)
    recipe.to_json
  end
```

Q: To return associated data in our JSON (e.g., if we want the JSON for an
Author to also contain a list of their books), we can do that using the
_________ method. (include)

Q: If we want to set up our app to return associated data in our JSON using
Active Record, which of the following steps are **required** (select all that
apply):

*a) Set up the association in our Model file
*b) Specify the association we want to include by using the  `to_json` method's `include` option
c) Use the `only` option to specify which attributes we want to include
d) Create a separate request for the associated data in our frontend

Q: In the code snippet below, what goes in the blank? (post '/recipes')

```rb
_________________ do
  recipe = Recipe.create(
    name: params[:name],
    ingredients: params[:ingredients]
  )
  recipe.to_json
end
```
