# Authentication

## refrences

- https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html
- https://en.wikipedia.org/wiki/Basic_access_authentication
- https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html
- https://www.npmjs.com/package/bcrypt

## Review, Research, and Discussion

1. Explain what a “Singleton” is (in Computer Science terms)

- singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. The term comes from the mathematical concept of a singleton.

2. Explain how the Singleton pattern can be used with Node modules, specifically with classes

- Sometimes you need to make sure that you have one and only one instance of an object. This is where the singleton pattern can be useful. A singleton represents a single instance of an object. Only one can be created, no matter how many times the object is instantiated. If there’s already an instance, the singleton will create a new one.

3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

- my best guess on this is i would start with some sort of modulization of my project and funnle the things that needed middleware to get funnled threw some kind of function or class that defines what ever you might need the middle ware for and send it on its way

## Terms

- Router Middleware - Router is used to manage these incoming requests. It kind of routes your requests to correct handler/code. Middleware it kind of hijacks your request so that you can do anything that you want with your request or response.

- Dynamic Module Loading - The import(module) expression loads the module and returns a promise that resolves into a module object that contains all its exports. It can be called from any place in the code We can use it dynamically in any place of the code,

- Singleton Pattern - singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. The term comes from the mathematical concept of a singleton.

- CRUD -> REST Method Matches - REST is an architectural system centered around resources and hypermedia, via HTTP protocols. CRUD is a cycle meant for maintaining permanent records in a database setting. CRUD principles are mapped to REST commands to comply with the goals of RESTful architecture.

- Mock Testing - is an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules.

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?

- modularity, linked lists, encription

2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- modularity, linked lists, encription, and also middleware

3. What are you most excited about trying to implement or see how it works?

- passwords
