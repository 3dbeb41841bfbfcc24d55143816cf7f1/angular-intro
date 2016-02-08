# Intro to AngularJS - Part 1

## What is AngularJS

> It's a library, it's a framework, it's AngularJS!

* AngularJS is The superheroic web development technology from Google!
* AngularJS does for HTML what CoffeeScript does for JavaScript and what SASS does for CSS.
* AngularJS teaches HTML new tricks!

> AngularJS is a lightweight SPA framework for native Web development.

## Why AngularJS?
* It provides everything you need to build a modern SPA
* There are *lots* of available libraries (modules) and a strong community
* Jobs, Jobs, Jobs - It's really *hot* in Atlanta

## What is a SPA?

* A Single Page (browser) App
* Uses AJAX to dynamically update the DOM
* Thus a single HTML page is used to run the entire app, but it appears to be a multi-page app.

## MVC in the Browser

* Both server and client apps can be partitioned into a MVC pattern.
* Rails follows MVC
* AngularJS follows MVC
* If we put them together, we get 2 MVC apps working together

![alt tag](https://raw.github.com/username/projectname/branch/path/to/img.png)

## Some responsibilities move from the server to the client:

* Most of the view and Controller logic
* Most of the routing

## The Server Still Matters

* Database interactions
* Session management
* Security

Typically the Server transforms into a secure RESTful API in front of a database
with session and user management responsibilities.

## The Motivation of AngularJS

A static HTML page:

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <h2>Hello John!</h2>
  </body>
</html>
```

### jQuery Version

```html
<!doctype html>
<html>
  <head>
    <script src="js/jquery-1.7.2.js"></script>
    <script type="text/javascript">
      $(function() {
        var name     = $('#name');
        var greeting = $('#greeting');

        name.keyup(function() {
          greeting.text('Hello ' + name.val() + '!');
        });
      });
    </script>
  </head>
  <body>
    <input id="name" type="text" placeholder="Enter your name">
    <h2 id="greeting"></h2>
  </body>
</html>
```

See: [DOM Updates via jQuery](http://codepen.io/drmikeh/pen/jEKRMj)
or
See: [DOM Updates via jQuery, standalone](http://codepen.io/drmikeh/pen/uhxng)

### AngularJS Version

```html
<!doctype html>
<html ng-app>
  <head>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.3.14/angular.min.js"></script>
  </head>
  <body>
    <div>
      <label>Name:</label>
      <input type="text" ng-model="yourName" placeholder="Enter your name">
      <hr>
      <h2>Hello {{yourName}}!</h2>
    </div>
  </body>
</html>
```

See: [DOM Updates with AngularJS](http://codepen.io/drmikeh/pen/emKogJ)

> NOTE: THERE IS NO JAVASCRIPT!!!
> How is AngularJS doing that?


## Our First AngularJS Directive - ng-app

* `ng-app` bootstraps AngularJS
* We can attach `ng-app` to any HTML Element but usually it is attached to the `<html>` tag.
* Other `directives` to come...


## More about SPAs

Responsibilities include:

* Module Loading
* Routing and View Loading
* DOM Updates and Data Binding
* Browser History
* AJAX and Event Handling
* Object Modeling
* Testing

## AngularJS Basics

* Views, Controllers, and $scope
* See Keynote slide
* Hello World with controller

## LAB

* Create an AngularJS calculator in Codepen / jsBin / jsFiddle
  - 2 numeric inputs with labels
  - 2 buttons: add and subtract
  - A result

See: http://codepen.io/drmikeh/pen/lFnsK


## Quiz

* What does SPA stand for?
* Describe 2-way (bidirectional) data binding.
* What is the role of $scope?
* What do each of these expressions do:
  - angular.module('myApp', [])
  - angular.module('myApp')
* List the Angular directives we have used in class so far.

