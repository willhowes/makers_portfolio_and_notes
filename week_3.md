# Week 3 Goals
[Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-3)

## Goals set by Makers
1. Build a simple web app
2. Follow an effective debugging process for web applications
3. Explain the basics of how the web works (e.g. request/response, HTTP, HTML, CSS)
4. Explain the MVC pattern

## Goal set for myself 
1. Watch the takeaway challenge video https://www.youtube.com/watch?v=mgiJKdH9x8c

### My daily goal for this week, after Week 2 Retrospective
1. Draw more diagrams.  

## How have I acheieved my goals?
### 1. Build a simple web app (and understood it)
* Acheived by:
  * Pair programming on the [week's challenge](https://github.com/makersacademy/course/tree/master/intro_to_the_web)

### 2. Follow an effective debugging process for web applications
* I am going to try to debug someone else's code (or do a practical if there is one)

### 3. Explain the basics of how the web works (e.g. request/response, HTTP, HTML, CSS)
* Perhaps write a blog to try and articulate this (with a diagram?)

### 4. Explain the MVC (Model View Controller) pattern

## Daily Goals

1. Learn about MVC
* Achieved by:
 * See take away notes below. 

2. Have a go at the [servers practical](https://github.com/makersacademy/skills-workshops/blob/master/practicals/servers_and_clients/servers.md)

## Takeaways/Notes
### Workshop Monday (10.30 with Sam)
* doubles and stubs are on the whole are great to isolate tests on a class.
* If you have a long list of doubles and stubs and you are getting confused about what they are doing and chaining behaviour, then this is an indication that you might have too many objects (classes).
* Doubling with dependency injection:
 * If in a method you have a call to ```.new``` then this is where you need dependenct injection as you cannot test that method without creating a new instance of the object (with ```.new```).
 
### Meeting weekly goals
* e.g. number 3 - ('Explain the basics of how the web works'). This can be achieved by being able to draw a diagram and explain it someone. 

### Web

### MVC
* The MVC will live on a server somewhere.
* MVC process is: client_request-->controller-->model-->controller-->view(convert to html)-->controler-->client.
* Controller will throw a 404 error if it doesn't know  what to do with the client request.
* Controller is the only contact with the client essentially. It is the way into the server. 
* Model is usually where all the classes and methods are. 
* When you hit ctrl-U on a website to see the source code you only see the "View" part of the code. 
* We will be using Sinatra rather than Rails as it is simpler. They are both web frameworks for Ruby.


