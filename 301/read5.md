# HEROKU

## what it is
We will use Node.js for our project. Node.js is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications. It's written in JavaScript and can be run within the Node.js runtime on any platform. First of all, of course, you need to install it. You'd better check the download page for more details. I'll wait until you finish, so don't worry. Is it done? Great! Now you can create your first web server. And it will be one of the easiest tasks in your life.

## refrence for how to do it 

Now, the creation. It will be a simple blog with basic functionality. It will show you requested web pages and the error page in case of an error.

Create your project directory. And then create the server.js file inside of it.

First of all, let's declare some variables:

var http = require("http");
var fs = require("fs");
var path = require("path");
var mime = require("mime");
The first one will give you the key to Node's HTTP functionality. The second one is for possibility to interact with the file system. The third one allows you to handle file paths. The last one allows you to determine a file's MIME-type. And it's not a part of Node.js, so we need to install third-party dependencies before using it. We need to create the package.json file for that purpose. It will contain project related information, such as name, version, description, and so on. For our project we will use MIME-types recognition, because it's not enough to just send the contents of a file when you use HTTP. You also need to set the Content-Type header with proper MIME-type. That's why we need this plug-in.

Create the package.json file and fill it with proper information. Here's

## sample HTML 

<html>
    <head>
        <title>Blog</title>
        <link rel="stylesheet" type="text/css" href="stylesheets/style.css">
    </head>
    <body>
        <div id="header">
            <span>My Simple Blog</span>
            <ul id="menu">
                <li>ABOUT</li>
                <li>ARTICLES</li>
                <li>VIDEOS</li>
                <li>SUBSCRIBE</li>
            </ul>
        </div>
        <div id="content">
            <h2><a href="ui_libraries_comparison.html">JavaScript UI libraries comparison</a></h2>
            <p>It seems to be pretty easy to create a good-looking web page. Even your neighbor has one or two of them. It's for sure! For approximately two decades of World Wide Web existence hordes of web developers are trying to improve the way of how you interact with the Global Network. And how it interacts with you through different technologies such as JavaScript, for example... <a class="article" href="ui_libraries_comparison.html">Read more</a></p>
            <h2><a href="">Node.js for beginners. Building your own web server</a></h2>
            <p>We will use Node.js for our project. Node.js is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications. It's written in JavaScript and can be run within the Node.js runtime on any platform. First of all, of course, you need to install it... <a class="article" href="hode.html">Read more</a></p>
        </div>
    </body>
</html>


you can combine Node.js with different technologies, such as CSS3 and HTML5, then spice it with some JavaScript functionality. There is really a lot of libraries and frameworks to take a look at. Personally I started to dig into Webix, it's a relatively new library and is developed by a small software company from Eastern Europe. Samples of apps made with the library and Node.js: CRM and task planner. Seems like you can create anything with the right client-side framework and Node.js.