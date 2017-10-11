HTTP

- What are the common request types associated with RESTful routing?

GET, POST, PUT/PATCH, and DELETE

- What are the components of an HTTP request?

Method, URL/path, protocol, headers, and body

- What is the content type associated with html form submissions?

? Form submission that is sent to a POST route

- What is the request header that can simulate state across requests?

? Sessions or cookies

- What is the request header that indicates the request is an AJAX request?

? X-Requested-With:XMLHttpRequest

? Host:ajax.googleapis.com

- What is the purpose of a cookie header?

A cookie header uses stored cookies in a request. The purpose of a cookie header is to maintain a state based on a previous session that a user had been in in the broswer.

- What are the different HTTP Verbs and what are they used for?

? GET - read

? POST - create

? PUT/PATCH - edit

? DELETE - delete

- What is the underlying data format of HTTP?

? Text/string

- You should be able to draw a diagram of a request/response cycle from the client to the server and back


- What are the responsibilities of the HTTP client?

? The responsibilities of the HTTP client are to enable the user to view the data in a legible and readable format; additionally the client must send requests and be able to receive responses

- What are the responsibilities of the HTTP server?

? The HTTP server must be able to receive requests and properly process them so that they may send the responses to the client

- What are some common HTTP reponse codes and what are they for?

2XX - OK
3XX - Redirect
4XX - Internal Error
5XX - Server Error

- What are the components of an HTTP Reponse?

Status code, body, headers

- What is the purpose of the set-cookie header?

? The set-cookie header sends cookies from the server to the client so that some data might persist on the client's end

- What are the different components of a URL?

Protocol, domain name/host, port, resource path, query

- What is the default port for HTTP?

80

- What is the scheme for securely passing information to/from the server?

?

Sinatra

- What is sinatra?
- What is the simplest sinatra app we could make?
- What is the underlying middleware that Sinatra sits on top of?
- What does this middleware do for us?
- Before responding to an HTTP request, we may need to reference or use various forms of data and state that are either managed by the server or included in the client’s request. Please give a few examples.
- What is the relationship between the erb templates and the HTTP response body?
- What is the difference between redirect and rendering a template?
- What is a method override and why do we need to do it?
