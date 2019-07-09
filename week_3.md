# Week 3 Goals
[Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-3)

## Goals set by Makers
1. Build a simple web app
2. Follow an effective debugging process for web applications
3. Explain the basics of how the web works (e.g. request/response, HTTP, HTML, CSS)
4. Explain the MVC pattern

## Goals set for myself 
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

### Tuesday
1. Learn about HTTP request response cycles
* Achieved by:
 * Read and understood these articles:
 * https://dev.opera.com/articles/http-basic-introduction/
 * https://dev.opera.com/articles/http-lets-get-it-on/
 * See takeaway notes below. 


### Monday
1. Learn about MVC
* Achieved by:
 * See takeaway notes below from the workshop. 
 * Read this [helpful article](https://www.tomdalling.com/blog/software-design/model-view-controller-explained/). See takeaway notes below from this 
 
 2. Review weekend challenges with pair partner.
  * Achieved by:
   * I reviewed Renata's: https://github.com/renatapop/takeaway-challenge
   * Renata reviewed mine: https://github.com/makersacademy/takeaway-challenge/pull/1363#discussion_r301003316
   * This proved an important exercise in trying to understand someone else's code and also undertanding someone's comments on your own code. Something I want to get better at, with the weekly code reviews on a Monday.

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

### Sinatra
* Sinatra is Gem you can use in ruby to mock a server locally. 
* You can use 'shotgun' when running the sinatra server from the terminal, i.e. ```shotgun app.rb``` this makes the server constantly referesh so you can instantly see the changes. 
* learned how interractions between a MODEL file and a VIEW file work. For example:
```
### app.rb

  get '/cat-form' do
    erb :cat_form
  end

  post '/named-cat' do
    p params
    @name = params[:name]
    erb :index
  end
  
 ### cat_form.erb
 <form action="/named-cat" method="post">
  <input type="text" name="name">
  <input type="submit" value="Submit">
</form>

### index.erb
<% if @name %>
<h1>My name is <%= @name %></h1>
<% end %>
```
With the above, on the ```/cat-form``` web page we submit fill in the name of the cat and submit this; then ```action="/named-cat"``` takes us to the ```"/named-cat"``` page which is linked to ```index.erb``` and prints ```My name is [CAT NAME]```.

### HTTP Client-Server Request-Response Cycle
* HTTP = Hypertext Transfer Protocol
* HTTP is an application protocol that sits above all communications between client and the server. 
* URIs (Uniform Resource Identifyers) are the labels for a web resource (or pieces of information). It it means the server knows where to find the information when a request is recieved. 
* There are 8 HTTP methods for requesting a URI: OPTIONS, GET, HEAD, POST, PUT, DELETE, TRACE, CONNECT. The most common is GET. 
* 200 code - OK 
* 400+ code - can't find server
* 500+ code - problem with server
* Use Dev Tools - Network tab so show what is going on with the request response cycle. 
* On the first GET request the client browser just gets the html, then the browser fires off more requests for the photos, etc.
* When you go to a page with, say a picture on it, it does a second GET request when it gets to ```<img src="cat.jpg'>```. It would be the same for a script. So there are two GET requests in this instance, the first to GET the actual webpage, the second for the picture. N.B. These are seperate GET requests. If you have lots of photos on a page this will generate lots of GET requests all trying run simultaneously. The GET responses are set one at a time but do not wait for the first to get back before sending the second, so they can run concurrently. 
* Can use "preserve log" in Chrome Devs Tools to keep recording the activity. 

### Process Modelling
* A diagram(or anything, a blog post) which helps you understand a process.
* Example of a process model for the HTTP REQUEST-RESPONSE cycle for going to this webpage https://makers-cats.herokuapp.com/cats.html :

1. CLIENT (browser) makes an http GET request using this url: https://makers-cats.herokuapp.com/cats.html)
2. SERVER (in this case a heruko web host) returns to the CLIENT the html of the webpage and sends a '200 OK' message.
3. CLIENT reads the html and sees that there is a photo it needs to get.
4. CLIENT sends a second separate http GET request for the photo using this url: https://makers-cats.herokuapp.com/cat.jpg.
5. SERVER returns the cat.jpg to the CLIENT with a '200 OK' message.




