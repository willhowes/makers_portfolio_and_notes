# Week 5
[Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-5)

## Week's Goals
* Test drive a simple front-end web app with Javascript
* Follow an effective process for learning a new language

## Own Goals
* Can explain what Ruby is good for and what Javascript is good for. Maybe a blog post on this. 

## Daily Goals
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
 
 ### Javascript 
 * Objects inherit all methods and properties from the prototype object, e.g:
 ```Person``` inherits all methods and properties from ```Person.prototype```
 * New properties or method cans be added to the object prototype, e.g:
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
