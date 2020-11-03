# Google API Documentation 

scotch nodeejs
https://github.com/scotch-io/node-ejs
Google api documents 
https://developers.google.com/books/docs/v1/using#WorkingVolumes

## Using the API

Using the API
Introduction
This document is intended for developers who want to write applications that can interact with the Books API. Google Books has a mission to digitize the world's book content and make it more discoverable on the Web. The Books API is a way to search and access that content, as well as to create and view personalization around that content.

If you're unfamiliar with Google Books concepts, you should read Getting Started before starting to code.

Authorizing requests and identifying your application
Every request your application sends to the Books API needs to identify your application to Google. There are two ways to identify your application: using an OAuth 2.0 token (which also authorizes the request) and/or using the application's API key. Here's how to determine which of those options to use:

If the request requires authorization (such as a request for an individual's private data), then the application must provide an OAuth 2.0 token with the request. The application may also provide the API key, but it doesn't have to.
If the request doesn't require authorization (such as a request for public data), then the application must provide either the API key or an OAuth 2.0 token, or both—whatever option is most convenient for you.
About authorization protocols
Your application must use OAuth 2.0 to authorize requests. No other authorization protocols are supported. If your application uses Google Sign-In, some aspects of authorization are handled for you.

Authorizing requests with OAuth 2.0
Requests to the Books API for non-public user data must be authorized by an authenticated user.

The details of the authorization process, or "flow," for OAuth 2.0 vary somewhat depending on what kind of application you're writing. The following general process applies to all application types:

When you create your application, you register it using the Google API Console. Google then provides information you'll need later, such as a client ID and a client secret.
Activate the Books API in the Google API Console. (If the API isn't listed in the API Console, then skip this step.)
When your application needs access to user data, it asks Google for a particular scope of access.
Google displays a consent screen to the user, asking them to authorize your application to request some of their data.
If the user approves, then Google gives your application a short-lived access token.
Your application requests user data, attaching the access token to the request.
If Google determines that your request and the token are valid, it returns the requested data.
Some flows include additional steps, such as using refresh tokens to acquire new access tokens. For detailed information about flows for various types of applications, see Google's OAuth 2.0 documentation.

Here's the OAuth 2.0 scope information for the Books API:

https://www.googleapis.com/auth/books

To request access using OAuth 2.0, your application needs the scope information, as well as information that Google supplies when you register your application (such as the client ID and the client secret).

Tip: The Google APIs client libraries can handle some of the authorization process for you. They are available for a variety of programming languages; check the page with libraries and samples for more details.

Acquiring and using an API key
Requests to the Books API for public data must be accompanied by an identifier, which can be an API key or an access token.

To acquire an API key:

Open the Credentials page in the API Console.
This API supports two types of credentials. Create whichever credentials are appropriate for your project:
OAuth 2.0: Whenever your application requests private user data, it must send an OAuth 2.0 token along with the request. Your application first sends a client ID and, possibly, a client secret to obtain a token. You can generate OAuth 2.0 credentials for web applications, service accounts, or installed applications.

For more information, see the OAuth 2.0 documentation.

API keys: A request that does not provide an OAuth 2.0 token must send an API key. The key identifies your project and provides API access, quota, and reports.

The API supports several types of restrictions on API keys. If the API key that you need doesn't already exist, then create an API key in the Console by clicking Create credentials > API key. You can restrict the key before using it in production by clicking Restrict key and selecting one of the Restrictions.

To keep your API keys secure, follow the best practices for securely using API keys.

After you have an API key, your application can append the query parameter key=yourAPIKey to all request URLs.

The API key is safe for embedding in URLs; it doesn't need any encoding.

## Google Books ID

Google Books IDs
You need to specify ID fields with certain API method calls. There are three types of IDs used within Google Books:

Volume IDs - Unique strings given to each volume that Google Books knows about. An example of a volume ID is _LettPDhwR0C. You can use the API to get the volume ID by making a request that returns a Volume resource; you can find the volume ID in its id field.
Bookshelf IDs - Numeric values given to a bookshelf in a user's library. Google provides some pre-defined shelves for every user with the following IDs:
Favorites: 0
Purchased: 1
To Read: 2
Reading Now: 3
Have Read: 4
Reviewed: 5
Recently Viewed: 6
My eBooks: 7
Books For You: 8 If we have no recommendations for the user, this shelf does not exist.
Custom shelves have IDs greater than 1000. A bookshelf ID is unique for a given user, i.e., two users can have a bookshelf with the same ID that refer to different bookshelves. You can use the API to get the bookshelf ID by making a request that returns a Bookshelf resource; you can find the bookshelf ID in its id field.
User IDs - Unique numeric values assigned to each user. These values are not necessarily the same ID value used in other Google services. Currently, the only way retrieve the user ID is to extract it from the selfLink in a Bookshelf resource retrieved with an authenticated request. Users can also obtain their own user ID from the Books site. A user cannot obtain the user ID for another user via the API or the Books site; the other user would have to share that information explicitly, by email for example.
IDs on Google Books site
The IDs you use with the Books API are the same IDs used on the Google Books site.

Volume ID
When viewing a particular volume on the site, you can find the volume ID in the id URL parameter. Here is an example:

https://books.google.com/ebooks?id=buc0AAAAMAAJ&dq=holmes&as_brr=4&source=webstore_bookcard

Bookshelf ID
When viewing a particular bookshelf on the site, you can find the bookshelf ID in the as_coll URL parameter. Here is an example:

https://books.google.com/books?hl=en&as_coll=0&num=10&uid=11122233344455566778&source=gbs_slider_cls_metadata_0_mylibrary

User ID
When viewing your library on the site, you can find the user ID in the uid URL parameter. Here is an example:

https://books.google.com/books?uid=11122233344455566778&source=gbs_lp_bookshelf_list

Setting User Location
Google Books respects copyright, contract, and other legal restrictions associated with the end user's location. As a result, some users might not be able to access book content from certain countries. For example, certain books are "previewable" only in the United States; we omit such preview links for users in other countries. Therefore, the API results are restricted based on your server or client application's IP address.

## How to use a EJS to template your Node Application 

Introduction
When creating quick on-the-fly Node applications, an easy and fast way to template our application is sometimes necessary.

Jade comes as the view engine for Express by default but Jade syntax can be overly complex for many use cases. EJS is one alternative does that job well and is very easy to set up. Let’s take a look at how we can create a simple application and use EJS to include repeatable parts of our site (partials) and pass data to our views.

Setting up the Demo App
We will be making two pages for our application with one page with full width and the other with a sidebar.

Get the code: You can find a git repo of the complete demo code on GitHub here

File Structure
Here are the files we’ll need for our application. We’ll do our templating inside of the views folder and the rest is pretty standard Node practices.

- views
----- partials
---------- footer.ejs
---------- head.ejs
---------- header.ejs
----- pages
---------- index.ejs
---------- about.ejs
- package.json
- server.js
package.json will hold our Node application information and the dependencies we need (express and EJS). server.js will hold our Express server setup, configuration. We’ll define our routes to our pages here.

Node Setup
Let’s go into our package.json file and set up our project there.

package.json
{
  "name": "node-ejs",
  "main": "server.js",
  "dependencies": {
    "ejs": "^3.1.5",
    "express": "^4.17.1"
  }
}
All we will need is Express and EJS. Now we have to install the dependencies we just defined. Go ahead and run:

npm install
With all of our dependencies installed, let’s configure our application to use EJS and set up our routes for the two pages we need: the index page (full width) and the about page (sidebar). We will do all of this inside our server.js file.

server.js
// load the things we need
var express = require('express');
var app = express();

// set the view engine to ejs
app.set('view engine', 'ejs');

// use res.render to load up an ejs view file

// index page
app.get('/', function(req, res) {
    res.render('pages/index');
});

// about page
app.get('/about', function(req, res) {
    res.render('pages/about');
});

app.listen(8080);
console.log('8080 is the magic port');
Here we define our application and set it to show on port 8080. We also have to set EJS as the view engine for our Express application using app.set('view engine', 'ejs');. Notice how we send a view to the user by using res.render(). It is important to note that res.render() will look in a views folder for the view. So we only have to define pages/index since the full path is views/pages/index.

Start Up our Server
Go ahead and start the server using:

node server.js

## Create the EJs Partials

Like a lot of the applications we build, there will be a lot of code that is reused. We’ll call those partials and define three files we’ll use across all of our site: head.ejs, header.ejs, and footer.ejs. Let’s make those files now.

views/partials/head.ejs
<meta charset="UTF-8">
<title>EJS Is Fun</title>

<!-- CSS (load bootstrap from a CDN) -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.5.2/css/bootstrap.min.css">
<style>
    body { padding-top:50px; }
</style>
views/partials/header.ejs
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="/">EJS Is Fun</a>
  <ul class="navbar-nav mr-auto">
    <li class="nav-item">
      <a class="nav-link" href="/">Home</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="/about">About</a>
    </li>
  </ul>
</nav>
views/partials/footer.ejs
<p class="text-center text-muted">© Copyright 2020 The Awesome People</p>
Add the EJS Partials to Views
We have our partials defined now. All we have to do is include them in our views. Let’s go into index.ejs and about.ejs and use the include syntax to add the partials.

Syntax for including an EJS Partial
Use <%- include('RELATIVE/PATH/TO/FILE') %> to embed an EJS partial in another file.

The hyphen <%- instead of just <% to tell EJS to render raw HTML.
The path to the partial is relative to the current file.
views/pages/index.ejs
<!DOCTYPE html>
<html lang="en">
<head>
    <%- include('../partials/head'); %>
</head>
<body class="container">

<header>
    <%- include('../partials/header'); %>
</header>

<main>
    <div class="jumbotron">
        <h1>This is great</h1>
        <p>Welcome to templating using EJS</p>
    </div>
</main>

<footer>
    <%- include('../partials/footer'); %>
</footer>

</body>
</html>
Now we can see our defined view in the browser at http://localhost:8080.node-ejs-templating-index

For the about page, we also add a bootstrap sidebar to demonstrate how partials can be structured to reuse across different templates and pages.

views/pages/about.ejs
<!DOCTYPE html>
<html lang="en">
<head>
    <%- include('../partials/head'); %>
</head>
<body class="container">

<header>
    <%- include('../partials/header'); %>
</header>

<main>
<div class="row">
    <div class="col-sm-8">
        <div class="jumbotron">
            <h1>This is great</h1>
            <p>Welcome to templating using EJS</p>
        </div>
    </div>

    <div class="col-sm-4">
        <div class="well">
            <h3>Look I'm A Sidebar!</h3>
        </div>
    </div>

</div>
</main>

<footer>
    <%- include('../partials/footer'); %>
</footer>

</body>
</html>
If we visit http://localhost:8080/about, we can see our about page with a sidebar!node-ejs-templating-about

Now we can start using EJS for passing data from our Node application to our views.

Pass Data to Views and Partials
Let’s define some basic variables and a list to pass to our home page. Go back into your server.js file and add the following inside your app.get('/') route.

server.js
// index page
app.get('/', function(req, res) {
    var mascots = [
        { name: 'Sammy', organization: "DigitalOcean", birth_year: 2012},
        { name: 'Tux', organization: "Linux", birth_year: 1996},
        { name: 'Moby Dock', organization: "Docker", birth_year: 2013}
    ];
    var tagline = "No programming concept is complete without a cute animal mascot.";

    res.render('pages/index', {
        mascots: mascots,
        tagline: tagline
    });
});
We have created a list called mascots and a simple string called tagline. Let’s go into our index.ejs file and use them.

Render a Single Variable in EJS
To echo a single variable, we just use <%= tagline %>. Let’s add this to our index.ejs file:

views/pages/index.ejs
...
<h2>Variable</h2>
<p><%= tagline %></p>
...
Loop Over Data in EJS
To loop over our data, we will use .forEach. Let’s add this to our view file:

views/pages/index.ejs
...
<ul>
    <% mascots.forEach(function(mascot) { %>
        <li>
            <strong><%= mascot.name %></strong>
            representing <%= mascot.organization %>, born <%= mascot.birth_year %>
        </li>
    <% }); %>
</ul>
...
Now we can see in our browser the new information we have added!

node-ejs-templating-rendered

Pass Data to a Partial in EJS
The EJS partial has access to all the same data as the parent view. But be careful: If you are referencing a variable in a partial, it needs to be defined in every view that uses the partial or it will throw an error.

You can also define and pass variables to an EJS partial in the include syntax like this:

views/pages/about.ejs
...
<header>
    <%- include('../partials/header', {variant:'compact'}); %>
</header>
...
But you need to again be careful about assuming a variable has been defined.

If you want to reference a variable in a partial that may not always be defined, and give it a default value, you can do so like this:

views/partials/header.ejs
...
<em>Variant: <%= typeof variant != 'undefined' ? variant : 'default' %></em>
...
In the line above, the EJS code is rendering the value of variant if it’s defined, and default if not.


