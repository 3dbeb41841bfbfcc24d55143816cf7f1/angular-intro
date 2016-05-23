# Introduction to AngularJS

![#  Help Me Angular, Help ...]
(https://raw.githubusercontent.com/ATL-WDI-Curriculum/angular-intro/master/images/framesworks.jpg)

## Lesson Objectives
- Describe the benefits of using a front end framework
- Explain how libraries differ from frameworks.
- Build a controller with hard coded data.
- Render and bind controller data in the view.
- Explain what angular directives do and how they are leveraged to execute JS.
- Use `ng-repeat` to iterate over data.
- use `ng-hide`/`ng-show` to hide and show elements.


## Opening Framing (5/5)

How we got here:

1. Vanilla JS
  - a lot of code to write

2. jQuery
  - easier to do more
  - easier to write more bad code

3. OOJS
  - more structured but a royal pain to write

4. Frameworks
  - provides code to structure and relate front-end components

What's the purpose of a front end framework? JS and all of it's many libraries are great, but you can start building and building your application and all of a sudden there's no structure and everything's soup.

### Libraries (2.5/7.5)

- libraries gives us tools to utilize.
- abstracts behaviors and allows us to write our code more succinctly
- allows us to write applications faster and easier
- lots of options, very few rules (jQuery)

### Frameworks (2.5/10)

- like libraries in that it gives us tools to utilize
- additionally they abstract structure and provide conventions for users to write code into that structure.
- Lots of rules (convention), fewer options (Express)
- What parts of your front-end from project3 could have been generically abstracted?

## What is a Front End Framework? (5/15)
- a library that attempts to move some or all application logic to the browser, while providing a simple interface for keeping the front-end in sync with the back-end
- applications can run completely in the browser, minimizing server load since the server is only accessed when the front end needs to synchronize data with the backend
- server sends over the app in the initial request (HTML/CSS/JS) then JS makes all subsequent requests with AJAX
- provides more fluid user experience
- loads everything from the database on page load (data and templates) then renders/updates the page content based on user interaction.

#  Help Me Angular, Help ...

![#  Help Me Angular, Help ...](https://raw.githubusercontent.com/ATL-WDI-Curriculum/angular-intro/master/images/helpmeangular.jpg)


* [Angular Super Powers](https://github.com/ATL-WDI-Curriculum/angular-intro/blob/master/Best_Of_Angular.MD)



## What is Angular? (15/30)

Take a look at [this quick overview of angular](http://www.tutorialspoint.com/angularjs/angularjs_overview.htm)(10)

T&T - Some points to think about (5)
- What are some features or characteristics of Angular?
- What are some of the advantages of Angular? Disadvantages?

## Angular (5/35)
- structural front end framework for dynamic web apps
- uses HTML as your template language and lets you extend HTML's syntax to express your application's functionality
- allows you to utilize html attributes to add behavior through JS. (directives)
- changes are reflected in various areas and persisted immediately without page refresh
- it's interesting, there'll be a lot of logic in the dom.


(http://www.sitepoint.com/top-javascript-frameworks-libraries-tools-use/)


* [Part 1](https://github.com/ATL-WDI-Curriculum/angular-intro/blob/master/part-1.md)
  - SPA
  - MVC in the browser
  - 2-way data binding for DOM Updates
  - Compares jQuery DOM Updates with AngularJS DOM Updates
  - Some simple Angular directives: ngApp, ngModel, ngInit, ngClick, ngController

* [Part 2](https://github.com/ATL-WDI-Curriculum/angular-intro/blob/master/part-2.md)
  - More on Angular Controllers with examples
  - ngRepeat and orderBy filter
  - ngRepeatStart and ngRepeatEnd
  - Angular Modules
  - More Angular directives: gDisabled, ngClass, ngShow, ngHide

* [Addtional Resources]
  - Angular style guide
      https://github.com/johnpapa/angular-styleguide
  - John Pappa 10 Angular patterns
      https://www.youtube.com/watch?v=UlvCbnKAH3g&list=PLkEzuuIN6SCAS6rXmwi0v6AsKJuuBbIB4
  - Dan Whalin
      https://www.youtube.com/watch?v=i9MHigUZKEM
  - Atlanta Angular Meeting * Created by WDI alumns.
    http://www.meetup.com/ATL-AngularJS/events/227610704/

