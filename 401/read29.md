# Application State with Redux

## Refrences

- https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867
- https://www.freecodecamp.org/news/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6/
- https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1
- https://redux.js.org/

## Review, Research, and Discussion

1. What are the advantages of storing tokens in “Cookies” vs “Local Storage”

- It's convenient.

- If you don't have a back-end and you're relying on a third-party API, you can't always ask them to set a specific cookie for your site. Works with APIs that require you to put your access token in the header like this: Authorization Bearer ${access_token}

2. Explain 3rd party cookies.

- Third-party cookies are created by domains that are not the website (or domain) that you are visiting. These are usually used for online-advertising purposes and placed on a website through adding scripts or tags. A third-party cookie is accessible on any website that loads the third-party server's code.

3. How do pixel tags work?

- A tracking pixel (also called 1x1 pixel or pixel tag) is a graphic with dimensions of 1x1 pixels that is loaded when a user visits a webpage or opens an email. ... The tracking pixel URL is the memory location on the server. When the user visits a website, the image with the tag is loaded from this server.

## Vocabulary

- cookies - Cookies are text files with small pieces of data — like a username and password — that are used to identify your computer as you use a computer network. ... Data stored in a cookie is created by the server upon your connection. This data is labeled with an ID unique to you and your computer.
- authorization - is a security mechanism to determine access levels or user/client privileges related to system resources including files, services, computer programs, data and application features. ... Key factors contain user type, number and credentials, requiring verification and related actions and roles.
- access control - is a security technique that regulates who or what can view or use resources in a computing environment. It is a fundamental concept in security that minimizes risk to the business or organization. ... Logical access control limits connections to computer networks, system files and data.
- conditional rendering - (that is, conditional statements, conditional expressions and conditional constructs,) are programming language commands for handling decisions. ... Although dynamic dispatch is not usually classified as a conditional construct, it is another way to select between alternatives at runtime.
