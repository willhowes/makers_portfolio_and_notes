# Week 3 Goals
[Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-3)

## Goals set by Makers
1. Build a simple web app
2. Follow an effective debugging process for web applications
3. Explain the basics of how the web works (e.g. request/response, HTTP, HTML, CSS)
4. Explain the MVC pattern

## Goals set for myself 
1. Watch the takeaway challenge video https://www.youtube.com/watch?v=mgiJKdH9x8c

### My daily goal for this week, after Week 2 Retrospective
1. Draw more diagrams.
 * Achieved by:
  * Attended workshop about process modelling. Made a model of the request-response for HTTP requests between client and server. (See takeaways below). 
  * I started to get in the habit of drawing a diagram as a domain model before starting to build anything. I also used diagrams to reinforce my understanding of concepts such as the MVC (Model-View-Controller) Model.

## How have I acheieved my goals?
### 1. Build a simple web app (and understood it)
* Acheived by:
  * Pair programming on the [week's challenge](https://github.com/makersacademy/course/tree/master/intro_to_the_web). A basic battle app, like Pokemon. [Last repositorty worked on](https://github.com/willhowes/battle-challenge)
  * Also built a [Rock-Paper-Scissors](https://github.com/willhowes/rps-challenge). This was the weekend challenge.

### 2. Follow an effective debugging process for web applications
* I am going to try to debug someone else's code (or do a practical if there is one)

### 3. Explain the basics of how the web works (e.g. request/response, HTTP, HTML, CSS)
* Perhaps write a blog to try and articulate this (with a diagram?)

### 4. Explain the MVC (Model View Controller) pattern
* Achieved by:
 * Being able to draw a diagram to show the MVC design. Can articulate the compenents of MVC and how they interact with each other (or how they DON'T interact with each other in MODEL and VIEW's case). Explain the advantages of using MVC, as opposed to having a direct MODEL to VIEW relationship. See my takeaways notes below. 

## Daily Goals

### Friday
1. Debug the [Birthday Challenge](https://diode.makersacademy.com/students/alicelieutier/projects/439)

### Thursday
1. Continue with the [Birthday Challenge](https://diode.makersacademy.com/students/alicelieutier/projects/439)
* Achieved by:
 * Getting close to completing this challenge. It is only a question of getting the our ```birthday_helper.rb``` module to correctly work out the days between today and the birthday, and making it look nice with css, and then we will be done. I have learned about how is best to keep anything other than very basic logic (perhaps one if statement) out of a ```view```, and into the controller file. 

2. Understand Debugging basics for web apps:
 * Achieved by:
  * Attending the debugging workshop and attempting the exercise. 
  * See my takeaway notes below. 

### Wednesday
1. Finish the takeaway video and make some notes on TDD.
 * Achieved by:
  * Watching the video and learning a few extra pointers on TDD and rspec (see takeaways below).

2. Try to understand more of what is going on between the controller file (i.e. where you have ```get...``` and the view file (where the html is).
 * Achieved by:
  * I now understand how the GET and POST created in the controller file (usually ```app.rb```) makes a get request and then tells what view should do. For example:
```
get '/' do
    erb :index
  end

  post '/names' do
    session[:player_1_name] = params[:player_1_name]
    session[:player_2_name] = params[:player_2_name]
    redirect '/play'
  end

  get '/play' do 
    erb :play
  end
```
The above works like so:
* On receipt of the first ```get``` request from the client (the browser) our server (run with sinatra) returns the ```index.erb``` view file.
* The ```index.erb``` file (not shown above) has a form which generates a ```post``` of the ```/names``` page when the submit button is pressed.
* On receipt of the ```post``` request from the client (which is  (posting ```player_1_name``` and ```player_2_name```, we our server re-directs the client to the ```/play``` page (this invokes an automatic ```get``` request)
* On receipt of this automatic ```get``` request the client is directed to the ```play.erb``` view file.
  

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

### Notes from the Takeaway challenge [youtube video](https://www.youtube.com/watch?v=mgiJKdH9x8c&t=2477s)
 * Can use intance doubles if you want your doubles of object to actually verifies whether that class actually has those doubles or not. For example: ```let(:order) { instance_double "Order", total: 15:50 }``` will actually check that the ```Order``` class actually has a method called ```total```.
 * When you have something like Twilio where you are relying on all the redentials etc from it to be able to send the text, rather than have this in the class that sends the text, you can pass it into that class as an argument, e.g.
 ```
 class SMS 
  def initialize(config, client)
   @client = client. 
  end
 end
 ```
 * So in the above, the SMS class needs the configeration details from Twilio, and details of the client for it to be able to send the text, but those credidentials do not need to be put into the class itself. 
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
* What the different type of response codes the client receives from the server are:
 * 1xx (Informational): Request received, continuing process.
 * 2xx (Successful): The action was successfully received, understood, and accepted.
 * 3xx (Redirection): Further action needs to be taken in order to complete the request.
 * 4xx (Client Error): The request contains bad syntax or cannot be fulfilled.
 * 5xx (Server Error): The server failed to fulfil an apparently valid request.

* Use Dev Tools - Network tab so show what is going on with the request response cycle. 
* On the first GET request the client browser just gets the html, then the browser fires off more requests for the photos, etc.
* When you go to a page with, say a picture on it, it does a second GET request when it gets to ```<img src="cat.jpg'>```. It would be the same for a script. So there are two GET requests in this instance, the first to GET the actual webpage, the second for the picture. N.B. These are seperate GET requests. If you have lots of photos on a page this will generate lots of GET requests all trying run simultaneously. The GET responses are set one at a time but do not wait for the first to get back before sending the second, so they can run concurrently. 
* Can use "preserve log" in Chrome Devs Tools to keep recording the activity. 

### Process Modelling
* A diagram(or anything, a blog post) which helps you understand a process.
* Example of a process model for the HTTP REQUEST-RESPONSE cycle for going to this webpage https://makers-cats.herokuapp.com/cats.html :

1. CLIENT (browser) makes an http GET request using this url: https://makers-cats.herokuapp.com/cats.html)
2. SERVER (in this case a heruko web host) returns to the CLIENT the html of the webpage and sends a '200' response code.
3. CLIENT reads the html and sees that there is a photo it needs to get.
4. CLIENT sends a second separate http GET request for the photo using this url: https://makers-cats.herokuapp.com/cat.jpg.
5. SERVER returns the cat.jpg to the CLIENT with a '200' response code.

### Chat with Bobby (Senior Developer friend) about the [Takeaway Challenge](https://github.com/willhowes/takeaway-challenge)
* Very important to go through all user stories before writing any tests and try a domain model. If it doesn't seem right, try different models. 
* Whilst there's many ways to build a project, it is important to be clear on what classes you will need from the outset. It may have been better in this project, to have had a Takeaway class, a Dish class, an Order class, and a Customer class (needed for sending the confirm test).
* For creating the order to do a hash (rather than an array of hashes) and then update the value of each key when duplicate orders of the same item are made. Like so:

```
class Order

  attr_reader :current_order

  def initialize
    @current_order = {}
  end

  def add(dish, quantity)
    if @current_order.include?(dish)
      new_quantity = @current_order[dish] + quantity
      @current_order.update(@current_order) { |key, quantity| new_quantity}
    else
      @current_order[dish] = quantity
    end
  end
end
```

### Empathy workshop
* To image what someone else is thinking. 
* Important to understand teammates, clients, colleagues who aren't developers, for example. 
* "Just like me...", i.e. we all have similarities. E.g. "Just like me, this person is seeking happiness in their like." Worth thinking of before pairing - do not pre-judge; remember you have things in common. 
* Metta Bhavana - wish someone else that they are happy. For example, before an interview (even though you may not have met them before), wish them well (actually think "I wish this person to be happy").
* Empathic listening - listen as if you are going to be receiving a test on what they said the next day

### Gem files
* To create gemfile use ```bundle init```

### Debugging workshop - web apps
* There a few more areas to consider with web apps. We do not have just the ruby code to consider, as we did in weeks 3 and 4. We have the MODEL, CONTROLLER and VIEW which can all throw errors, as can the framework we are using for these (Sinatra, Capybara, etc). Therefore, there arte considerably possiblilities for where an error might occur. 
* TOOLS WE CAN USE TO FIND THE ISSUE WITH THE CODE:
 * Stack trace (and their error messages)
 * p/print/puts (to ascertain what each of part of the code is actually doing. 
 * rspec
 * running the code in browser to feature test. Generally speaking, this is where you should feature test for web apps, rather than in a REPL (e.g. irb or pry). 
* You should NOT change the code or the tests until we are sure of where the issue with the code is. It is dangerous to change the code on pure guess work. You may forget to revert code back to how it was and take yourself further away from finding a solution. 
* If after changing the code you get the same error message that is a red flag that you have done something wrong and should put the code back to how it was. A different error message is generally good.
* In cabybara it is worth trying ```save_and_open_page``` in the failing test at the point where you would like to pause the program.  It will show you what is on the page at that particular moment. So you can run the program in the browser and see what the view is producing at that point. 
* Worth noting that the way Capybara works is it runs the tests on a pretend browser under the hood and so you cannot see it. 
* Even if all your tests are passing, you should still test the code in the browser as some tests might pass when they shouldn't. In particular Sinatra can cause this to happen - when an error message is thrown by sinatra, the page might actually have the test written on the web page (as part of the errror message that Sinatra throws) and therefore if the test is searching for content on the web page it may be found by the test in the error message on the page. 

### Retrospective
* LACKED - Testing web apps. There is a lot of extra files when testing compared to what we are used to. The initial setup with capybara, sinatra, using spec_helper, etc. Main thing is to know why you are installing those tools (like capybara). 
* Feature tests cover the application as a whole and how user interracts with it. You should begin creating unit tests as soon as you start to introduce a MODEL. 
* MVC is a key outcome of this week. It is a very common achitecture pattern.
* CONTROLLER should only have variable assignments and method calls, in terms of actual logic.

### Weekend challenge - things I learned
* If you need to stub out a random element, seems to be easier to put this random element in a separate class so that you can mock it and stub the ```rand``` method.
* In Capybara feature tests, if you want to only check part of the page, then you will need to give that element of the page (in the VIEW file) an ID (using CSS) so that you can just check that element in your Capybara test. 

### Singleton Pattern
* This is where you want to restrict a class (or object) to only creating one instance of itself.
* An example of when you might want to use this is a an object for the game Scrabble that contains all the letters available for the game. The two players should us the same class so that they both share the same pool of letters. 
* To acheieve this you can have a class variable that is set to true or false depending on whether an instance of the class has been created.
* IN ruby you can just use: 
```
class Shop 
 include Singleton
end
```
```Singleton``` is a module in Ruby. To create the instance you will call ```shop.instance``` as ```shop.new``` will create an error as it is a private method to provent multiple instances. 

* WARNING - Singleton classes should be avoided in Ruby if possible. The reason being, it creates a global variable which can then be changed by any outside file and it would be very difficult to trace where it has been changed if it is a big project. 

 
