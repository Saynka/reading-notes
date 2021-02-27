# Express REST API

## refrences 

* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes

* https://expressjs.com/en/guide/routing.html

* https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4

### Review, Research, and Discussion

1. Name 3 real world use cases where you’d want to change the request with custom middleware
#### checking if a user is authenticated, logging data for analytics, or anything else we'd like to do before we actually spit out information to our user.

2. True or false: The route handler is middleware?
#### i guess true cuz you can tell the route to go threw your middle ware

3. In what ways can a middleware function end the process and send data to the browser?
#### The order you place your middleware and routes is very important. Everything will happen in the order that they appear. This means that if you place your middleware after a route, then the route will happen before the middleware and the request will end there. Your middleware will not run at that point. 

4. At what point in the request lifecycle can you “inject” middleware?
#### after you send for a request but before your end route

5. What can cause express to error with “Request headers sent twice, cannot start a second response”
#### not using the provide next as an argument to the callback function and then call next() within the body of the function to hand off control to the next callback.

## terms

### middleware - software that acts as a bridge between an operating system or database and applications, especially on a network.

### Request Object - is the main entry point for an application to issue a request to the Library - all operations on a URL must use a Request object. ... A request object is registered in the library by issuing an operation on a URL - for example PUT, POST, or DELETE.

### Response Object - The Response interface of the Fetch API represents the response to a request. ... Response() constructor, but you are more likely to encounter a Response object being returned as the result of another API operation

### Application Middleware -  software that lies between an operating system and the applications running on it. ... This can include security authentication, transaction management, message queues, applications servers, web servers, and directories.

### Routing Middleware -  Express is a routing and middleware web framework that has minimal functionality of its own: An Express application is essentially a series of middleware function calls. ... Middleware functions can perform the following tasks: Execute any code. Make changes to the request and the response objects.

### Test Driven Development -  “Test-driven development” refers to a style of programming in which three activities are tightly interwoven: coding, testing (in the form of writing unit tests) and design (in the form of refactoring).

### Behavioral Testing - is a testing of the external behaviour of the program, also known as black box testing. It is usually a functional testing.