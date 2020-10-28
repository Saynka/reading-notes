## CALL STACK

* call stack
https://developer.mozilla.org/en-US/docs/Glossary/Call_stack

* javaScript call stack
https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/

* javaScript error messages
https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c

* javaSCript Error refrence
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors

A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

* When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
* Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
* When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
* If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

## Example 

function greeting() {
   // [1] Some codes here
   sayHi();
   // [2] Some codes here
}
function sayHi() {
   return "Hi!";
}

// Invoke the `greeting` function
greeting();

// [3] Some codes here
The code above would be executed like this:

* Ignore all functions, until it reaches the greeting() function invocation.
Add the greeting() function to the call stack list.
Call stack list:
- greeting

* Execute all lines of code inside the greeting() function.
Get to the sayHi() function invocation.
Add the sayHi() function to the call stack list.
Call stack list:
- sayHi
- greeting

* Execute all lines of code inside the sayHi() function, until reaches its end.
Return execution to the line that invoked sayHi() and continue executing the rest of the greeting() function.
Delete the sayHi() function from our call stack list.
Call stack list:
- greeting

* When everything inside the greeting() function has been executed, return to its invoking line to continue executing the rest of the JS code.
Delete the greeting() function from the call stack list.
Call stack list:
EMPTY

In summary, then, we start with an empty Call Stack. Whenever we invoke a function, it is automatically added to the Call Stack. Once the function has executed all of its code, it is automatically removed from the Call Stack. Ultimately, the Stack is empty again.

# Call stack notes

* At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

Let’s break down our definition:

LIFO: When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

* The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

* The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.


* function firstFunction(){
  console.log("Hello from firstFunction");
}

function secondFunction(){
  firstFunction();
  console.log("The end from secondFunction");
}

secondFunction();

This is what happens when the code is run:

1. When secondFunction() gets executed, an empty stack frame is created. It is the main (anonymous) entry point of the program.
2. secondFunction() then calls firstFunction()which is pushed into the stack.
3. firstFunction() returns and prints “Hello from firstFunction” to the console.
4. firstFunction() is pop off the stack.
5. The execution order then move to secondFunction().
6. secondFunction() returns and print “The end from secondFunction” to the console.
7. secondFunction() is pop off the stack, clearing the memory.

* What causes a stack overflow?
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

# JavaScriptSyntax errors refrence website for debugging

* Syntax errors
I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

* Range errors
Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

* Type errors
Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.
This is probably the most frequent error in JS, trying to access a property/method thinking that bar is of the type object when in reality, since it hasn’t been declared yet, it’s undefined which doesn’t have any baz available.

* Reference errors
This is as simple as when you try to use a variable that is not yet declared you get this type os errors.