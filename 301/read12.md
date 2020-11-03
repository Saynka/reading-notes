# Ejs Partials 

Partials come in handy when you want to reuse the same HTML across multiple views. Think of partials as functions, they make large websites easier to maintain as you don’t have to go and change a piece of text in every page it appears in. Instead, you define that reusable bundle of code in a file andinclude it wherever you need it.
Our blog will consist of a home page which lists all the blog posts and a post page which will display a single post. Our home page will look like so:
Image for post
and the post page:
Image for post
As you can see from the screenshots above, the same navigation bar and footer appear in both the home and post view. This makes them perfect candidates for partials!
Let’s go ahead and create those partials. Under the views/partials/ directory create a file callednavbar.ejs which will contain only the HTML for the navigation bar at the top of the home and post pages:
<!-- views/partials/navbar.ejs -->
    <div class="header clearfix">
        <nav>
            <ul class="nav nav-pills pull-right">
                <li role="presentation"><a href="/">Home</a></li>
            </ul>
            <h3 class="text-muted">Node.js Blog</h3>
        </nav>
    </div>
and a file called footer.ejs in that same directory:
<!-- views/partials/footer.ejs -->
    <footer class="footer">
        <p>© 90210 Lawyer Stuff.</p>
    </footer>
Now that we have our partials defined, we can use them in our home.ejs and post.ejs templates! In EJS, any JavaScript or non-HTML syntax you include in your templates is always surrounded by <% %> delimiters (you could change these delimiters if you really wanted to).
Including a partial in EJS is quite straightforward. You use <%- include( PARTIAL_FILE ) %> where the partial file is relative to the template you use it in.
Note: The <%- %> tags allow us to output the unescaped content onto the page (notice the -). This is important when using the include() statement since you don’t want EJS to escape your HTML characters like ‘<’, ‘>’, etc…
Let’s create the homepage template in views/home.ejs and include the navbar and footer partial we just created:
<!-- views/home.ejs -->
    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8">
        <title>Node.js Blog</title>
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css">
        <style>
            body {
                padding-top: 20px;
                padding-bottom: 20px;
            }
            .jumbotron {
              margin-top: 10px;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <%- include('partials/navbar') %>
            <div class="jumbotron">
                <h1>All about Node</h1>
                <p class="lead">Check out our articles below!</p>
            </div>
            <div class="row">
                <div class="col-lg-12">
                    <div class="list-group">
                      <!-- loop over blog posts and render them -->
                      LIST_OF_POSTS
                    </div>
                </div>
            </div>
            <%- include('partials/footer') %>
        </div>
    </body>
    </html>
and for the post page in views/post.ejs:
<!-- views/post.ejs -->
    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8">
        <title>POST_TITLE | Node.js Blog</title>
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css">
        <style>
            body {
                padding-top: 20px;
                padding-bottom: 20px;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <%- include('partials/navbar') %>
            <div>
                <h2>POST_TITLE</h2>
                <p>by <a href="#">POST_AUTHOR</a></p>
                <p>POST_CONTENT</p>
                <hr>
            </div>
            <%- include('partials/footer') %>
        </div>
    </body>
    </html>
As you can see creating and including partials is very straightforward with EJS. I’ve intentionally left in some placeholders such as LIST_OF_POSTS, POST_TITLE, POST_AUTHOR, and POST_CONTENT so that we can take a look at how we can pass data from our Node + Express application to our views in the next section.
WRITTEN BY

Hensle Joseph
Follow
261

1
261 

1

Web Development
JavaScript
More from Hensle Joseph
Follow
Aug 3, 2016
FREQUENTLY ASKED QUESTIONS ANGULAR 2 COURSE
1- Do I need to know Angular 1 before taking this course?
No! Angular 2 is an entirely new framework and this course assumes no prior knowledge of Angular.
2- Angular 2 is in beta. Will this course be updated?
Certainly, This course will be updated continuously until final version of Angular 2. You’ll find updates from beta to final release in the last section of the course.
3- Why is the course with TypeScript? Why not Javascript?
TypeScript is a superset of Javascript, meaning any valid Javascript code is valid TypeScript. If you can write Javascript code, you can write TypeScript code! So you don’t have to learn a new programming language. TypeScript brings many useful features to Javascript that are missing in the current version of Javascript. We get classes, modules, interfaces, properties, constructors, access modifiers (e.g. …
Read more · 2 min read


Aug 2, 2016
Angular 2 Tutorial: HTTP Requests with Observables
Making HTTP requests is a vital operation in the life of most front-end applications. Angular 2, which is the hottest thing right now has a really cool way of doing that. Actually that is what we are going to cover together today in this tutorial. We will learn how how to make HTTP requests using RxJs Observable library.
What are Observables?
Observables are similar to promises but with major differences that make them better.
Observables are a new primitive coming with ES7 (ES2016) that helps handle asynchronous actions and events. …
Read more · 13 min read


Aug 2, 2016
Routing Angular 2 Single Page Apps with the Component Router
Getting Started: App Setup
Angular 2 uses TypeScript, so if you need a refresher on that, take a look at why TypeScript is your friend and our TypeScript tutorial series.
Before we get started and to save us some setup time, clone the Angular 2 QuickStart then we can build on top of that.
git clone https://github.com/angular/quickstart scotch-ng-router
The seed already has end to end tools to enable you start building Angular 2 apps. It also comes with all Angular 2 dependencies including angular/router so we can just pull the packages from npm:
npm install
We are more concerned with the app folder of our new project which is…
Read more · 12 min read


Aug 1, 2016
Facebook Incubator: Facebook’s Open Source Gift To Programmers
Introducing a new way of thinking (that should be adopted by other tech giants) while working with open source projects, Facebook has launched Incubator on GitHub. The social network aims to release its internal open source projects via this central channel and observe their adoption in the open source community. If a project does well and gains popularity, it’ll graduate to its own repo.
GitHub is the most popular web-based GIT repository hosting service. …
Read more · 2 min read


Jul 31, 2016
Create a Globally Available Custom Pipe in Angular 2
In this tutorial, we will learn about what is pipe, how to build a custom pipe, how to make the pipe available application wide. Live example here in plunkr.
Introduction
Angular 2 comes with a stock of pipes such as DatePipe, UpperCasePipe, LowerCasePipe, CurrencyPipe, and PercentPipe. They are all immediately available for use in any template.
For example, utilize the uppercase pipe to display a person name in capital letter.
import { Component } from '@angular/core';
@Component({
  selector: 'my-app',
  template: '<p>My name is <strong>{{ name | uppercase }}</strong>.</p>',
})
export class AppComponent {
  name = 'john doe';
}
The output of the example above is My name is JOHN DOE. …

## tutorial video 
https://www.youtube.com/watch?v=3_xEEH4fTEk&t=0s&index=7&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt
