HTTP

- What are the common request types associated with RESTful routing?

GET, POST, PUT/PATCH, and DELETE

- What are the components of an HTTP request?

Method, URL/path, protocol, headers, and body

- What is the content type associated with html form submissions?

application/x-www-form-urlencoded

- What is the request header that can simulate state across requests?

Cookies

- What is the request header that indicates the request is an AJAX request?

X-Requested-With:XMLHttpRequest

[post-man: makes arbitrary http requests]

- What is the purpose of a cookie header?

A cookie header uses stored cookies in a request. The purpose of a cookie header is to maintain a state based on a previous session that a user had been in in the broswer.

- What are the different HTTP Verbs and what are they used for?

GET - read

POST - create

PUT/PATCH - edit

DELETE - delete

- What is the underlying data format of HTTP?

Text/string

- You should be able to draw a diagram of a request/response cycle from the client to the server and back


- What are the responsibilities of the HTTP client?

The client must send requests and be able to receive responses

- What are the responsibilities of the HTTP server?

The HTTP server must be able to receive requests and properly process them so that they may send the responses to the client

- What are some common HTTP reponse codes and what are they for?

2XX - OK
200
3XX - Redirect
302
303
4XX - Internal Error
404
418
422
5XX - Server Error
500
503

[more detail about specific status codes]

- What are the components of an HTTP Reponse?

Status code, body, headers

- What is the purpose of the set-cookie header?

? The set-cookie header sends cookies from the server to the client so that some data might persist on the client's end

[Client can repeat data to server on each subsequent request]

- What are the different components of a URL?

Protocol, domain name/host, port, resource path, query

- What is the default port for HTTP?

80

- What is the scheme for securely passing information to/from the server?

https

[google scheme]

Sinatra

- What is sinatra?

Sinatra is a DSL (domain specific language) that works with Ruby to create web applications.

- What is the simplest sinatra app we could make?

? The simplest Sinatra web app that we can make would involve two files: one config, and one file that includes the logic for models, controllers, and views.

- What is the underlying middleware that Sinatra sits on top of?

Rack

- What does this middleware do for us?

?

- Before responding to an HTTP request, we may need to reference or use various forms of data and state that are either managed by the server or included in the client’s request. Please give a few examples.

? We could use instance variables that access different portions of data that are within the server. These portions of data can be accessed from a get request using the params

- What is the relationship between the erb templates and the HTTP response body?

? The erb template includes HTML and Ruby data, but the HTTP response body is that data converted into text format

- What is the difference between redirect and rendering a template?

? Redirect works as a get request to a route that is already defined while rendering a template converts a file into text and displays that data as text for a webpage

- What is a method override and why do we need to do it?

? A method overrid


Javascript

- Why is accessing a property with bracket notation more appropriate than dot notation?

? Accessing a property with a bracket notation is more appropriate than dot notation because that property is a value in a key-value pair

[prohibits certain characters; ]

- How do you add a property to an object?

? One can add a property to an object by defining a parameter and having that parameter equal to a value

- How do you change the value of an object's property?
- How do you remove a property from an object?
- How do you write an if statement?

One writes an if statement by writing "if" before the condition written in parentheses and afterwards adding curly braces, in which one would include the action to perform if the condition is met

- How do you write a switch statement?
- How do you write a for loop?

One writes a for loop by writing "for" and afterwards writing in parentheses a defined variable which will work as the starting point; and comparing that variable to a determined length; and incrementing that variable until that variable reaches the determined length.

- How do you write a for..in loop?
- What is the difference between declaring a variable using and not using var?

? Declaring a variable not using var will confuse Javascript because the variable is not defined; one would need to use var so that Javascript knows that we are defining a variable.

[Javascript will create that variable with global scope; var will create variable within the scope of that function or any functions nested within that function]

- What happens when we try to access property of an object that doesn't exist?
- What is variable hoisting?
- How can we split a string into segments in javascript?
- How do you write a function?
- What is the inheritance system that JavaScript uses?
- How does property lookup work in JavaScript?
- What is the relationship between a function's prototype and objects created with the function?
- How do we define a constructor function?
- How do you add functions to a constructor function's prototype?
- What is an object literal?
- When do we use an object literal vs a contructor function?
- What is a callback function and how do we use it?
- What is a closure and how do we use it?
- How is scope determined in JavaScript?
- What is a higher-order function?
- What does it mean for a function to be a 'first-class citizen'?
- Can you write a function that returns a function?
- What type of scope is used JavaScript?
- What is this?
- What are the methods call, apply, and bind used for?
- What is variable shadowing?
