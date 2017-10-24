<h1>HTTP</h1>

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

<h1>Sinatra</h1>

- What is sinatra?

Sinatra is a DSL (domain specific language) that works with Ruby to create web applications.

- What is the simplest sinatra app we could make?

? The simplest Sinatra web app that we can make would involve two files: one config, and one file that includes the logic for models, controllers, and views.

- What is the underlying middleware that Sinatra sits on top of?

Rack

- What does this middleware do for us?

? This middleware enables the app to require each of the files so that within each file we don't need to specify which files depend on which other files, which in turn enables the app to function properly.

- Before responding to an HTTP request, we may need to reference or use various forms of data and state that are either managed by the server or included in the client’s request. Please give a few examples.

? We could use instance variables that access different portions of data that are within the server. These portions of data can be accessed from a get request using the params

- What is the relationship between the erb templates and the HTTP response body?

? The erb template includes HTML and Ruby data, but the HTTP response body is that data converted into text format

- What is the difference between redirect and rendering a template?

? Redirect works as a get request to a route that is already defined while rendering a template converts a file into text and displays that data as text for a webpage

- What is a method override and why do we need to do it?

? A method override is used to perform a different function aside from the standard functionaliy. We would need to use it when using BCrypt so that we might be able to authenticate a user's password.

<h1>Sessions</h1>

- What are sessions?

? Sessions are cookies that enable certain data to be accessible by certain users.

- Why do we need to use sessions?

? We need to use sessions so that we can enable users to obtain the data that is unique to them.

- What types of data can be stored in session?

? A session can store strings and even objects. It can be used to store a user's id so that we may enable that user to access their data.

- What types of things should we not store in session?

? Objects

- How is the session passed from the server to the client?

? The session is passed from the server to the client by

<h1>Authentication</h1>

- What is authentication?

Authentication is matching a user's inputted data with the data that that user might have within the server so that the user might be able to access more of their unique data within the server.

- Why do we need it?

We need authentication so that a user's private data would not be accessed by anyone else besides that user.

- How do we authenticate a user?

We authenticate a user by finding their username or e-mail address, and checking to see if the password that is inputted matches the BCrypted password.

<h1>BCrypt</h1>

- What is BCrypt?

BCrypt is a functionality that hashes passwords so that we do not store plain text passwords within our database.

- Why do we need it?

We need BCrypt so that we do not store plain text passwords within our database.

- Why should we never store plain text passwords in the database?

We should never store plain text passwords within the database because that would be a security hazard. Users have private data stored within the server, so it's important that we have security measures ensured so that that data remains private.

- The BCrypt methods that we write, what do they do for us?

We write two methods: a setter and a getter. The setter method is called upon on registration. It takes the plain text password and creates a new password object by adding a salt to the plain text password and hashing it. That hashed password is then stored as a string within the database.

? The getter method is called upon when a user logs in, using authintication. The string version of the hashed password that is saved in the database is placed within the Password.new function, which can only take in string versions of a hashed password. The plain text is compared with this hashed password using a double equal comparison that works as a method override from its standard usage.

- When we authenticate a user, how are we able to compare the plaintext password with the encrypted one stored in the database?

? The getter method is called upon when a user logs in, using authintication. The string version of the hashed password that is saved in the database is placed within the Password.new function, which can only take in string versions of a hashed password. The plain text is compared with this hashed password using a double equal comparison that works as a method override from its standard usage.

<h1>Authorization</h1>

- What is authorization?

Authorization is the active prevention of users from accessing data that is not meant for them.

- What is the difference between authorization and authentication?

Authentication is used to ensure that a user has the right to data that is stored within the database. Authorization is used to ensure that that user accesses that data only and not other users' data.

- Why do we use authorization?

We use authorization to ensure privacy for users.

- Why is it not enough to just show / hide buttons in an application?

It is not enough to show/hide buttons because it would be possible for users to manually enter the route to get to that data.

- How do we fully secure an application?

We fully secure an application by placing authorize methods within routes that should remain private and only for specific users.


<h1>Javascript</h1>

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

? We would end up getting a return that is undefined

- What is variable hoisting?

? Variable hoisting is defining a variable as null before redefining it within a different scope so that we might be able to access that variable within any function written in the program

- How can we split a string into segments in javascript?

? We can split a string into segments in javascript using the prototyle method ".split()"

- How do you write a function?

? There are a few ways to write a function. One way is:

function FunctionName()

Another is:

var functionName = function()

The function is then followed by curly braces, in which we would nest the logic that the function performs. If we are expecting a return, we must specify what we are returning by writing "return" in front of that which we want to be returned.

- What is the inheritance system that JavaScript uses?

? The inheritance system that Javascript uses is that we would first need to define an object and its attributes. After defining that object, we would write prototype functions that we might be able to call with each instance of that object.

- How does property lookup work in JavaScript?

? In Javascript we may lookup a property using dot notation (object.propertyName) or bracket notation (object['propertyName']. This is highly similary to accessing the value of a hash in Ruby.

- What is the relationship between a function's prototype and objects created with the function?

? The objects created with the function are meant to be unique to the instances of each specific object, while the function's prototype are meant to be the same function that will be ran with each instance.

- How do we define a constructor function?

? A constructor function is defined similarly to an object literal. We would define the function like a standard function, with parameters defined as variables. Within the curly braces we would define each parameter as attributes using "this." For example:

function(name, age, favoriteCartoon) {
  this.name = name;
  this.age = age,
  this.favoriteCartoon = favoriteCartoon
};

- How do you add functions to a constructor function's prototype?

? One would add functions to a constructor function's prototype by defining an attribute and having it equalled to a callback function. For example:

function(name, age, favoriteCartoon) {
  this.name = name;
  this.age = age,
  this.favoriteCartoon = favoriteCartoon;
  this.favoriteIceCreamFlavor = function(flavor) {
    return flavor
  }
};

- What is an object literal?

? An object literal is an object that is defined in simplest terms. It is set to a variable, and it is equal to curly braces, and within the curly braces are the object's attributes that are defined in key-value pairs.

- When do we use an object literal vs a contructor function?

? We would use an object literal if we just needed that one object at a given moment. We would use constructor functions if we would need to make multiple instances of that object.

- What is a callback function and how do we use it?

? A callback function is an anonymous function, or unnamed function, that we would use to perform specific tasks within a named function.

- What is a closure and how do we use it?

? (What) A closure is the combination of a function and the lexical environment within which that function was declared.

- How is scope determined in JavaScript?

? Scope is determined in javascript by what data is accessible by which function.

- What is a higher-order function?

? A higher-order function is a function that takes a function as a parameter and may return a function as a result

- What does it mean for a function to be a 'first-class citizen'?

? A function that is a first-class citizen is a function that may be accessed by anything within the program

- Can you write a function that returns a function?

? Yes, these are called higher-order functions

- What type of scope is used JavaScript?

? Local and global

- What is this?

? This is similar to self in Ruby; this is referencing the object in which the current scope is within

- What are the methods call, apply, and bind used for?

? Call invokes the function and allows you to pass in arguments one by one.
Apply invokes the function and allows you to pass in arguments as an array.
Bind returns a new function, allowing you to pass in a this array and any number of arguments.

- What is variable shadowing?

? Variable shadowing is when a variable within one scope has the same name as a variable within another scope.
