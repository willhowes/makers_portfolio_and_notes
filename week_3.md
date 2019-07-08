# Week 3 Goals
[Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-3)

## Goals set by Makers
1. Build a simple web app
2. Follow an effective debugging process for web applications
3. Explain the basics of how the web works (e.g. request/response, HTTP, HTML, CSS)
4. Explain the MVC pattern

## Goal set for myself 
1. Watch the takeaway challenge video https://www.youtube.com/watch?v=mgiJKdH9x8c

2. Write a blog

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
* Achieved by:
 * Being able to draw a diagram to show the MVC design. Can articulate the compenents of MVC and how they interact with each other (or how they DON'T interact with each other in MODEL and VIEW's case). Explain the advantages of using MVC, as opposed to having a direct MODEL to VIEW relationship. See my takeaways notes below. 

## Daily Goals

### Monday
1. Learn about MVC
* Achieved by:
 * See takeaway notes below from the workshop. 
 * Read this [helpful article](https://www.tomdalling.com/blog/software-design/model-view-controller-explained/). See takeaway notes below from this 
 
 2. Review weekend challenges with pair partner.
  * I reviewed Renata's: 
  * Renata reviewed mine: https://github.com/makersacademy/takeaway-challenge/pull/1363#discussion_r301003316

## Takeaways/Notes
### Workshop Monday (10.30 with Sam)
* doubles and stubs are on the whole are great to isolate tests on a class.
* If you have a long list of doubles and stubs and you are getting confused about what they are doing and chaining behaviour, then this is an indication that you might have too many objects (classes).
* Doubling with dependency injection:
 * If in a method you have a call to ```.new``` then this is where you need dependenct injection as you cannot test that method without creating a new instance of the object (with ```.new```).
 
### Meeting weekly goals
* e.g. number 3 - ('Explain the basics of how the web works'). This can be achieved by being able to draw a diagram and explain it someone. 

### Web

### MVC (Model View Controller)
FROM THE [ARTICLE](https://www.tomdalling.com/blog/software-design/model-view-controller-explained/)
* It is a design pattern which sets out the components of a server.
* MODEL - this simply represents the data and it doesn't do anything else. It is independent of the CONTROLLER and the VIEW. N.B. - THIS IS THE GOLDEN RULE OF MVC. 
* VIEW - this is essentially the displaer of the MODEL (i.e. the data). VIEW also sends user actions to the CONTROLLER (e.g. a button click). Whilst the view can be independent of the MODEL and ther CONTROLLER, it can also actually be the CONTROLLER (in which case it would depend on the MODEL). 
* CONTROLLER - this handels the client requests, then provides the data in MODEL to the VIEW and interprets the user actions (e.g. a button click) to send back to the client. 
* Advantages of MVC:
 * Simplicity - it removes unnecessary dependancies in between classes. 
 * MODEL becomes reusable with differnet VIEW classes. For example, if you had a ```user_data``` class (the MODEL), a ```data_controller``` class (the CONTROLLER) and a ```view_data_in_table``` class then you would not need to amend the MODEL (```user_data```) if you wanted to build an additional VIEW class, e.g ```view_data_as_pie_chart```. If you did not use MVC and, say just had a MODEL and a VIEW then the code in MODEL would need to be altered to be able to interract with the VIEW classes. 
 * VIEW becomes reusable. The VIEW will not neccessarily only be useful to the particular MODEL we are working on. Using our previous example, a ```view_data_in_table``` may be useful to other MODELS not just the current one we are using. Since VIEW does not depend on MODEL the VIEW should not need modification to use with another MODEL.
 * In short, the CONTROLLER removes the dependancy between MODEL & VIEW, making them both reusable. 
 * This makes implementing new features easier - a different MODEL class can be brought in which should still work with the current VIEW class, and a different VIEW class can be brought in which will work with the current MODEL class. 

FROM THE WORKSHOP
* MVC process is: client_request-->CONTROLLER-->MODEL-->CONTROLLER-->VIEW-->CONTROLLER-->client.
* Controller will throw a 404 error if it doesn't know what to do with the client request.
* Controller is the only contact with the client essentially. It is the gateway into the server. 
* When you hit ctrl-U on a website to see the source code you only see the VIEW part of the code. 


