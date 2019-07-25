# Week 5
[Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-5)

## Week's Goals
* Test drive a simple front-end web app with Javascript
* Follow an effective process for learning a new language

## Own Goals
* Can explain what Ruby is good for and what Javascript is good for. Maybe a blog post on this. 
 * Some notes on this:
 - Javascript can be run directly in the browser. This has the benefits of being able to create web pages/web apps which are fully interactive but do not require GET, POST,etc requests each time the page needs updating. 
 - Javascript is not an Object Orientated language. However, it can be used as such but has not been designed with Object Orientated design like Ruby has. 
 - In Ruby everything is an object. *Nearly* everything is an object, however, strings, numbers and booleans are 'primitive values' rather than objects. This has the benefit of faster code since primative values can be called faster than objects which may have lots of methods and attributes. 
 - However, Javascript treats primitive values as objects when calling methods on them. Examples:
 ```
 true.toString()
 => "true"
 "name".length()
 =>
 x = 1
 x.toString()
 => "1"
 y = 9.99
 y.toFixed()
 => 10
 ```
 

## Daily Goals

### Thursday
1. Go through yesterday afternoon's steps on the Thermostat challenge to reinforce what I learned.

2. Learn about callbacks and control flow in Javascript. 
 * [Skills workshop](https://github.com/makersacademy/skills-workshops/tree/master/week-5/callbacks_following_the_flow_of_control)

### Wednesday
1. Understand how encapsulation works in Javascript
 * Achieved by:
  * Attended the [skills workshop](https://github.com/makersacademy/skills-workshops/tree/master/week-5/encapsulation_with_constructor_and_prototype_pattern) 
  * I can explain that in Javascript we can encapsulate code by using contructor functions and the prototype object.
  * A constructor function is a way of creating an object in Javascript which can then be used as template object which other new objects can reference all the methods and attributes of. 
  * I can explain that every object in Javascript has a prototype object which contains all the methods available to that object. The methods in the prototype object can then be reference by new objects which are created as ```new``` instances of the parent object. See more notes on prototypes [below](https://github.com/willhowes/makers_portfolio_and_notes/blob/master/week_5.md#prototype-in-javascript)

2. Have a look at closures
 * Achieved by watching [this youtube video](https://www.youtube.com/watch?v=-jysK0nlz7A) and doing some research. 
 * I can explain that in Javascript, when you have a function nested within another function you cannot call that function from outside the parent function. See [example below](https://github.com/willhowes/makers_portfolio_and_notes/blob/master/week_5.md#javascript-closures).


### Tuesday
1. Understand Javascript objects and prototypes and how these differ from using classes in Ruby.
* Achieved by:
 * I can explain that, unlike Ruby, Javascript does not have classes. Although Javascript ES6 does have the keyword ```class``` which can create something which is like a class, it is not the same thing. The class keyword just creates a constructor object which you can use to create new instance objects with the same methods and attributes of the original consructor object. See [my example](https://github.com/willhowes/makers_portfolio_and_notes/blob/master/week_5.md#javascript-objects-and-classes).
 * I can explain that every object in Javascript has a prototype property which contains all the methods of that object. [See my example](https://github.com/willhowes/makers_portfolio_and_notes/blob/master/week_5.md#prototype-in-javascript). If you want an object to have a method then you should add it using objectName.prototype.methodName = function() {}

### Monday
1. Review someone else code and get my code reviewed. 
* Achieved by:
  * Reviewed [Rhianne's code](https://github.com/makersacademy/chitter-challenge/pull/1293#pullrequestreview-264690393)
  * Was able to give feedback on what was done well and what could have been improved.
  * Had [my weekend challenge](https://github.com/makersacademy/chitter-challenge/pull/1283#discussion_r305734636) reviewed by Rhianne. Took on board that there was some repeated code I could have refactored out becuase of failing the DRY test. Need to be careful to get database set up instructions correct. Also took on board the praise for my detailed README file and for my code generally. 
  * GENERAL OTHER POINT: when using databases need to set up a suitable RAKE file, e.g. https://github.com/samover/chitter/blob/master/Rakefile

2. Understand this weeks goals and set my own additional goals if appropriate. 
 * Achieved by:
  * I attended the workshop for setting up the week's ouline and goals see [takeaways](https://github.com/willhowes/makers_portfolio_and_notes/blob/master/week_5.md#weeks-goals-etc)

## Takeaways & Notes

### Monday's code review
* What tools to use? e.g Ruby gems, like BCrypt - how secure are they? It is worth looking at how many downloads the gem has had. e.g. BCrypt has had 62 million downloads. Look at how often it is updated. How good is the documenation on git hub (or elsewhere). It is not necessarily a concern that it is failing Travis. 
* Primary Keys - unique identifiers for a row in a database table. You can have more than one per row. Not a good idea for anything that might need changing - e.g. emails, as user would not be able to change it.  Useful article: https://www.itprotoday.com/sql-server/sql-design-how-choose-primary-key. Usually you would just use the Primary Serial Key as the only primary key for a row of data.
* When to use class methods and when to use instance methods:
 * ```.all``` on, for example, the Peep class you would want to be a class method as it needs to refer to all instances of the Peep class. 
* ORMs (e.g. Active Record, Data Mapper) take out the need to think about class methods, as they have these methods as default. 
* ```require``` at top of Ruby file means you can all use the methods available in the module you are requiring. 
* Inheritance just allow the class that is inheriting to use all the attributes and methods in the class it is inheriting. 
* Many-to-many:
 * e.g. Tags and Posts (in Twitter)
  * Make a join table of the tag_id and the post_id. 
  * Get the tag_id by searching for the name of the tag
  * Search for the tag_id in the joint table and return an array of the post_ids that have the tag_id we have searched for. 
  * Convert that array of post_ids into an array of posts which we can then use.
   
### Weeks goals, etc
 * Main goal is learning a new language. Javascript is just a tool for learning a new language.
 * Key: can you learn a new language and its patterns. 
 * Make sure you are making your own goals - relate these to the goals for the whole course. 
 * The ```this``` keyword in javascript is v important. Do I understand this?
 * Remember: Javascript is not an OO language, so you have to adapt it accordingly. 
 * V Important - Javascript runs IN THE BROWSER
 * 'The Count' practical is good to get an overview of a javasript project.
 * Javascript is the only language that can be run directly in the browser.
 * Javascript can change the html without a new request-response cycle (i.e without a client call to the server). 
 * Javascript is a-syncranous (it does not need to run in order), unlike Ruby. 
 * Can run javascript in chrome-dev tools in the Console. 
 * We will be using version ES5 of Javascript. ES6 has extra features but can create bad-habits. 
 
 ### Javascript general notes
 * Most things in Javascript are an object, but not everthing is. For example, ```null``` is not an object, neither are strings, numbers and booleans and so they do not have methods. However, if you try to call a method on a string, for example, Javascript will wrap the string into an object temporarily so the method can be called. For example:
 ```
 "hello".length
 => 5
 ``` 
 or you can do this: 
 ```
 var hello = new String("Hello")
 ```
 The above will have all the methods of a String object. 
 
 * Objects inherit all methods and properties from the prototype object, e.g:
 ```Person``` inherits all methods and properties from ```Person.prototype```
 * New properties or methods can be added to the object prototype, e.g:
 ```
 function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
}

Person.prototype.nationality = "English";

Person.prototype.name = function() {
  return this.firstName + " " + this.lastName;
};
```
Using the above example you can call the ```.name``` function on the new Person object as follows:
```
var joe = new Person("Joe", "Bloggs", "40", "Brown")

joe.name()
=> "Joe Bloggs"
```
```
joe.nationality
=> "English"
```
* You can set a function on an object to be an already created function, e.g. 
```
var sayHello = function() { return "Hello" };
var person = { legs: 2 };
person.englishGreeting = sayHello;
person.englishGreeting();
=> "Hello"
```

* You can set an object's function using a key: value pair, e.g:
```
var dog = {
 speak: function() { return "bark!" }
 };
dog.bark()
=> "bark!"
```
```var rainbow = function() {}``` and ```function rainbow() {}``` do the same thing.
* ```use strict``` means you cannot access a variable before it has been defined in the code. 
* Probably advisable to use ```strict``` all the time. 
* underscores for private variables is only a convention ```._leaveAlone``` will do the same thing as ```.leavealone```. It is just to sell someone else reading the code that it should not be accessed from out of its function. 
* If you have a private variable, e.g. ```_name``` it is good practice to have a getter method to access this, e.g. ```Sheep.prototype.getName  = function() { return this._name }```. Even though you could actually access it using ```Sheep._name```.
* when you are using a method like ```.map``` need to make sure something is returned on each iteration, otherwise ```undefined``` will be returned. 

### Javascript objects and 'classes'
* Javascript doesn't really have classes, it only has 'pretend classes' in ES6 (the ```class``` keyword is not available in ES5 but, in any case, the ```class``` keyword is doing the same thing as setting up a constructer function. Example:
```
function User(email, name) {
 this.email = email
 this.name = name
 this.login = function() {
 console.log(this.email, 'has logged in');
 }
}

var userOne = new User('test@example.com', 'test_user');
userOne
=> User {email: "test@example.com", name: "test_user", login: ƒ}

userOne.login()
=> test@example.com has logged in
```

### Prototype in Javascript
* Usually you will want to use the 'prototype property' to add a method to an object
* Every object has a ```__proto__```  property which lists all the methods for that object. You can see this when you return an object to the console. 
* In the above example the ```this.login``` method is not part of the prototype property. It was not attached to the ```__proto__``` property.
* In the ```User``` object above, the ```User``` object has the prototype property, but the instances of the ```User``` object do not. The instances of that object, e.g. ```userOne``` have the ```__proto__``` property which points to the prototype property of the object (the contructor function)
* We can attach methods to the prototype property. Example using the ```User``` object above:
```
User.prototype.login = function() {
 this.online = true;
 console.log(this.email, 'has logged in')
}
userOne.login
=>  test@example.com has logged in
```
* Adding methods to an object using the ```prototype``` property also means that we can use inheritance. 
* If you add a method to an instance of an object e.g. ```userOne.login = function() {}``` then this would override the function of the same name (```.login```) under the prototype object. 

### 'this' - the Javascript keyword
* ```this``` references the object that is executing the current function
* We need to think of functions on objects as 'methods' and functions outside objects (i.e. global functions) as 'functions'
* Example of ```this``` in a method (i.e. a function in a class):
```
var cat = {
 legs: 4,
 printObject: function() {
  console.log(this)
 }
};
cat.printObject()
=> {legs: 4, printObject: ƒ}
```
* In a function (i.e. a function on the global object, not with another object) ```this``` will just return the global object (which, for javascript, is the ```window```).Example with a normal global function:
```
function globalFunc(param) { console.log(this) }
globalFunc("a")
=> Window {postMessage: ƒ, blur: ƒ, focus: ƒ, close: ƒ, parent: Window, …}
```
Example with constructor function:
```
function Func(title) { console.log(this) }
Func("a")
=> Window {postMessage: ƒ, blur: ƒ, focus: ƒ, close: ƒ, parent: Window, …}
```
However, if you call a constructor function using the ```new``` operator this creates a new empty object and ```this``` will return the object it is being called on rather than the global object, e.g":
```
function Video(title) {
    this.title = title;
    console.log(this)
}
const v = new Video('b');
=> Video {title: "b"}
```

### Javascript closures
* Example scope of a local:
``` 
function rainbow() {
 unicorn() // this will work as we are within the rainbow function 
 function unicorn() {
 }
}
unicorn() //this would not work as unicorn is local to the rainbow function.
```
* Because the ```unicorn()``` function is an 'inner function' it has access to all the variables in the parent function (in this case the ```rainbow()```.
* Every time the ```rainbow()``` function is called a new ```unicorn()``` function is created in the computer's memory. However, you cannot access the ```unicorn()``` function from outside of the ```rainbow()``` function.   

### Softwire Tech Talk
* When looking for work - do the employers actually mention working hours? Do they mention career path you can take there?

### Wednesday's Encapsulation Workshop
* getting visibility - ```console.log()``` it is the equivalent of ```puts``` in ruby (not ```p```). It will always return ```undefined```.



