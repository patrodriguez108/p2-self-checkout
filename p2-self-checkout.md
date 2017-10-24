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

[getting HTTP requests and parsing the HTTP requests and making the responses]

- Before responding to an HTTP request, we may need to reference or use various forms of data and state that are either managed by the server or included in the client’s request. Please give a few examples.

We could use instance variables that access different portions of data that are within the server. These portions of data can be accessed from a get request using the params

- What is the relationship between the erb templates and the HTTP response body?

The erb template includes HTML and Ruby data, but the HTTP response body is that data converted into text format

- What is the difference between redirect and rendering a template?

Redirect works as a get request to a route that is already defined while rendering a template converts a file into text and displays that data as text for a webpage

- What is a method override and why do we need to do it?

We would also use it when using a form that upon submission would make a request other than a GET or a POST


<h1>Sessions</h1>

- What are sessions?

? Sessions are cookies that enable certain data to be accessible by certain users.

[Sessions are stored-in cookies so that we can send that data back and forth so that we can identify data for that certain user]

- Why do we need to use sessions?

? We need to use sessions so that we can enable users to obtain the data that is unique to them.

[Giving the HTTP request some state saying which user is making the request]

- What types of data can be stored in session?

? A session can store strings and even objects. It can be used to store a user's id so that we may enable that user to access their data.

- What types of things should we not store in session?

? Objects

- How is the session passed from the server to the client?

? The session is passed from the server to the client by using the cookie in the headers

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

The getter method is called upon when a user logs in, using authintication. The string version of the hashed password that is saved in the database is placed within the Password.new function, which can only take in string versions of a hashed password. The plain text is compared with this hashed password using a double equal comparison that works as a method override from its standard usage.

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

<h1>HTML</h1>

- What is HTML?

HyperText Markup Language is a language that is used as a standard for rendering web pages and web apps.

- Why do we use it?

We use HTML so that we may be able to view our web pages and web apps

- What is the effect of adding a label to various form elements?

The effect of adding a label to various form elements is allowing users to know what information they would need to fill in

- How and why would you use the alt attribute?

We would use the alt attribute by adding alt and setting it to the words that we would want to display. We would use the alt attribute as alternative text that a user may see if other text may be unrenderable

- How and why would you use the tabindex attribute?

One would use the tabindex attribute by adding it to a tag on a form and assigning a value to it. We would use it so as to make entering data easier for a user, so that when a user inputs information they may get to the next portion of the form by pressing tab.

- How and why would you use the title attribute?

One would use the title attribute by adding the title to a tag and assigning the value. We would use the title attribute to specify extra information

- What are common use cases for the meta element?

The meta element is used for explaining what data is used for using data

- What is the difference in how inline and block elements display?

Inline elements do not start on a new line and only take up as much width as necessary, while block elements always start on a new line and take up as much width as there is available.

- What are some common inline tags?

span, a, img

- What are some common block level tags?

div, header such as h1, p, form

- What are data- attributes for?

? The data- attributes are for defining a class of information that will be passed between HTML and the DOM

[custome attributes that we can make and put in any HTML tag; specialized HTML attributes that a user can input; similar to writing variables in HTML]

- What are some common html attributes and how do you write them?

href="[path]"

name="[name]"

src="[source]"

- What is the purpose of the form element's action attribute?

The form element's action attribute specifies the route to which the form's data will be taken to once the form is submitted.

- What is the purpose of the form element's method attribute?

The form element's method attribute defines what type of request is being made once the form is submitted.

- When do you use the different input types?

We would use type="text" when the input field is text that the user will be entering; type="password" is for when the user will be entering a password; type="hidden" is for when the data will need to be sent by a request type other than a GET or a POST, and is used as a way to redefine the form's method attribute.

- What is meant by semantic markup?

What is meant by semantic markup is that the code that is written in HTML is written within the proper context, similarly to proper grammar within a spoken language.

- What are the difference between some of the common container html elements?

? Some container elements are inline and some are block

- What does it mean for HTML to be valid?

Some HTML tags might not be supported, depending on the version. If the version of HTML that is being used does not support a tag that is written, then that tag is not valid.

- Why is it important that we write valid html?

? It is important that we write valid HTML so that we might be able to render the web page or the web app without any issues

<h1>CSS</h1>

- What is CSS?

Cascading Style Sheets is a language that is used to design and style HTML

- What does it allow us to do?

It allows us to design and style a web page or an app so that it may be more presentable

- What is the box model?

The box model is a principle that is followed when using CSS. It follows the thought process that all HTML elements are boxes, and when styling it we may nest the boxes in a way that is more visually appealing. The outermost box is the margin, followed by the border, padding, and right in the center is the content.

- How is the box size calculated?

? The box size is calculated using pixels

[uses pixels; box-size calculated using padding and border-size; box-size accounts everything that needs to be inputted]

- What is the difference between margin and padding?

Margin is the amount of space defined for the surroundings of an element. Padding is the space within an element

- Which box model properties apply to block, inline, inline-block elements?

Display

- What is the default positioning for elements?

Static

- What are the differences in static, relative, absolute, and fixed positioning?

Static: default; positioned according to the flow of the page

Relative: positioned relative to its normal position; setting a left property by 30px will move it 30px away from its normal position

Absolute: positioned relative to its nearest possible positioned ancestor; if no positioned ancestors, will be positioned relative to the document body and will remain tacked to the same spot as if its position were fixed

Fixed: positioned relative to the viewport; will remain in the same position as the page scrolls down

- How do floats effect positioning?

Floats effect positioning by placing the element that has the float property along the left or right side of an element and wrapping text or inline elements about it

- What are the benefits of responsive design?

The benefits of responsive design are that a user can change the size of their window and still view the page without any hindrances, and additionally it would give the option to view the web page on a mobile device.

- What is the relationship between relatively positioned and absolutely positioned elements?

An absolutely positioned element would be positioned relative to a relatively positioned element if the relatively positioned element were an ancestore

- How do you define inline styles?

Inline styles are lines that are added to a document that defines HTML that apply style

- Why is it best to avoid inline styles?

It is best to avoide inline styles because the lines are hardcoded into the HTML document, and in order to apply the styles consistently we would need to apply those lines throughout the document. It would be much easier to define those styles that apply to whichever elements using CSS.

- How do we link an external style sheet?

We link an exzternal style sheet using a link tag that includes the path of the CSS document

- What are some common css selectors?

#id and .class, as well as the name of the tag

<h1>Javascript</h1>

- Why is accessing a property with bracket notation more appropriate than dot notation?

? Accessing a property with a bracket notation is more appropriate than dot notation because that property is a value in a key-value pair

[prohibits certain characters; ]

- How do you add a property to an object?

? One can add a property to an object by defining a parameter and having that parameter equal to a value

- How do you change the value of an object's property?

Set it equal to the new value

- How do you remove a property from an object?

[Something like hash.delete]

- How do you write an if statement?

One writes an if statement by writing "if" before the condition written in parentheses and afterwards adding curly braces, in which one would include the action to perform if the condition is met

- How do you write a switch statement?

Similar to a case statement, but only operates on integers

- How do you write a for loop?

One writes a for loop by writing "for" and afterwards writing in parentheses a defined variable which will work as the starting point; and comparing that variable to a determined length; and incrementing that variable until that variable reaches the determined length.

- How do you write a for..in loop?

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in

- What is the difference between declaring a variable using and not using var?

? Declaring a variable not using var will confuse Javascript because the variable is not defined; one would need to use var so that Javascript knows that we are defining a variable.

[Javascript will create that variable with global scope; var will create variable within the scope of that function or any functions nested within that function]

- What happens when we try to access property of an object that doesn't exist?

 We would end up getting a return that is undefined

- What is variable hoisting?

? Variable hoisting is defining a variable as null before redefining it within a different scope so that we might be able to access that variable within any function written in the program

[]

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

[prototypal]

- How does property lookup work in JavaScript?

In Javascript we may lookup a property using dot notation (object.propertyName) or bracket notation (object['propertyName']. This is highly similary to accessing the value of a hash in Ruby.

- What is the relationship between a function's prototype and objects created with the function?

? The objects created with the function are meant to be unique to the instances of each specific object, while the function's prototype are meant to be the same function that will be ran with each instance.

[if within the prototype the function will be ran once with each]

- How do we define a constructor function?

? A constructor function is defined similarly to an object literal. We would define the function like a standard function, with parameters defined as variables. Within the curly braces we would define each parameter as attributes using "this." For example:

function(name, age, favoriteCartoon) {
  this.name = name;
  this.age = age,
  this.favoriteCartoon = favoriteCartoon
};

- How do you add functions to a constructor function's prototype?

? One would add functions to a constructor function's prototype by defining an attribute and having it equalled to a callback function. For example:

var Constructor = function(name, age, favoriteCartoon) {
  this.name = name;
  this.age = age,
  this.favoriteCartoon = favoriteCartoon;
};

Constructor.prototype.favoriteIceCreamFlavor = function(flavor) {
    return flavor
  };

- What is an object literal?

An object literal is an object that is defined in simplest terms. It is set to a variable, and it is equal to curly braces, and within the curly braces are the object's attributes that are defined in key-value pairs.

- When do we use an object literal vs a contructor function?

We would use an object literal if we just needed that one object at a given moment. We would use constructor functions if we would need to make multiple instances of that object.

- What is a callback function and how do we use it?

 A callback function is an anonymous function, or unnamed function, that we would use to perform specific tasks within a named function.

- What is a closure and how do we use it?

? (What) A closure is the combination of a function and the lexical environment within which that function was declared.

[Scope changes within a closure]

- How is scope determined in JavaScript?

? Scope is determined in javascript by what data is accessible by which function.

[Scope changes across function; function level scope]

- What is a higher-order function?

A higher-order function is a function that takes a function as a parameter and may return a function as a result

- What does it mean for a function to be a 'first-class citizen'?

? A function that is a first-class citizen is a function that may be accessed by anything within the program

[can pass functions around as data]

- Can you write a function that returns a function?

Yes, these are called higher-order functions

- What type of scope is used JavaScript?

Function scope

- What is this?

This is similar to self in Ruby; this is referencing the object in which the current scope is within

- What are the methods call, apply, and bind used for?

? Call invokes the function and allows you to pass in arguments one by one.
Apply invokes the function and allows you to pass in arguments as an array.
Bind returns a new function, allowing you to pass in a this array and any number of arguments.

- What is variable shadowing?

Variable shadowing is when a variable within one scope has the same name as a variable within another scope.

<h1>jQuery</h1>

- What is jQuery?

jQuery is a Javascript library that selects HTML and XML elements on a webpage

- What does it allow us to do?

jQuery allows us to manipulate the DOM

- What are the common types of selectors we can use?

$("#id") and $(".class")

<h1>Event Handling</h1>

- What are events?

Events are actions that the web page performs when the user interacts with the page

- How/Why do we bind events?

We bind events by specifying which element on the web page is performing the event and perform a request and a response.

We bind events because we would need to perform that request and manipulate the DOM based on the response that we receive.

- What is event bubbling?

Event bubbling is when an event is attempted to be bound, but the response that is meant to manipulate the DOM based off of that binding is not performed in the way that was intended. Instead the response manipulates several elements in the DOM, likely the parents and ancestors of the element that was originally intended to be manipulated.

- What is event delegation?

Event delegation is when an event handler is set up at a higher level. Rather than handling the event selecting a single element on the web page, a parent or ancestor is also selected to handle the event more specifically.

- Why do we need to delegate events?

We need to delegate events so that all elements on the webpage that we bind events to perform their intended functions regardless of whether or not they are on the web page when the document is ready.

<h1>AJAX</h1>

- What is AJAX?

AJAX is a tool that utilizes objects in HTMLand/or XML that enables those who utilize AJAX to manipulate the DOM when the client makes requests and receives responses. Using AJAX will prevent the default state of HTTP requests and responses from occurring. Instead the user will be kept on the same page as AJAX deals with the requests and response objects, manipulating the DOM as requests are made and responses are sent.

- What are the benefits of an AJAX request vs reloading the whole page?

? The benefits of an AJAX request are that it provides a much smoother and quicker user experience, enabling the user to submit data and interact with the webpage instead of being directed to multiple pages.

[Only receiving and sending small bits of data]

- What is the $.ajax() jQuery method actually doing for us?

$.ajax() is performing an HTTP request, but in an "asynchronous" way, or in its own speed.

- What are the common options that can be sent to the $.ajax() jQuery method and what are they used for?

Method: the type of request that the request being sent is

URL: the path of the request that is being sent

Data: the data that is being sent within the request if the user is inputting data

- When does the done / error callback actually execute?

? The done/error callback executes after the request has been made and the response has been sent

[done vs error; done will have 200 status and any 400 or 500 level status will lead to the fail]

- How do we know that we've made an ajax request in our controller?

? We know that we've made an ajax request in our controller when the response sends back data upon the done/error callback

[if the request header has X-Requested-With:XMLHttpRequest a part of it; request.xhr?]
