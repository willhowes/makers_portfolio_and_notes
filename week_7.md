# Week 7
[Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-7)

## Week's Goals

1. Can you write a frontend, single page app using only pure JavaScript?

### Have I achieved the above goals?

* Built the [note app](https://github.com/willhowes/Seton2) with my group using only pure JS. 
* We also built a our own testing framework ('Dave') so we could test drive the build. 

## Own Goals for the Week

1. Go to a Process Workshop.
* I went to one on Monday.

2. Have a deeper understanding of JS

3. Look at and understand: https://github.com/makersacademy/course/blob/master/pills/javascript_module_pattern.md

## Takeaways & Notes

### For reviews
Ask the reviewer: 
1. What input I am getting?
2. What output are you expecting?
3. How will the user interact with the program?
4. Any edgecases

### Testing without a framework
1. Produced our own JS testing framework 'Dave' which made constance functions ```describe```, ```it```, ```expect``` and one matcher ```toBe``` which we could then use for our own project.

### Process Workshop on Monday
* What I learned:
1. If I am going to use Ruby I need to keep my hand in with it to make sure I do not waste time having to look up how to write a new class or a new test, for example. Also need to remember to set up folders correctly - ```lib``` and ```spec``` folders.
2. Debug a bit quicker using ```p``` or ```console.log```. 
3. Don't go into doing major logic for the problem until necessary. 

### Module Patterns Workshops
1. Whether to use multi-page app or single page app is really a UX design decision rather than a developer one. 
2. It is way of encapsulating behaviour. Iife's are essentially private methods.
3. This is one pattern. If you are using this pattern should be consistent throughout your code. 
4. If using static typing (like with ```sctrict```) you should declare a variable using ```var``` and then access it without the ```var``` later. This will mean that if you make a typo when you try to access it later it will through an error, e.g.:

```var name = will```
and then later:
```namee = will```
this will through an error but wouldn't do if you were not using static typing (for example with ruby) which would just declare a new variable ```namee```.

### IIFE ('iffy') = Immediately Invoked Function Expression
- Example:
```
(function() {
  console.log("hi");
})();
```
- broken down this is:
1. An annonymous function, i.e the 
```
function() {
  console.log("hi");
}
```
2. The parentesis that wrap this annonymous function.
3. The final set of parentheis after the wrapping parenthesis which runs the annonymous function.

* IIFEs are used to hide variable and function declarations. So in reality the above example is pointless as the is no reason to hide ```console.log```. 

* A better example:
```
(function () {
  var EXCLAMATION_MARK_COUNT = 5

  function exclaim(string) {
    return string + "!".repeat(EXCLAMATION_MARK_COUNT);
  };

  console.log(exclaim("hi"));
})();
```
In the above code the the ```exclaim``` function and the ```EXCLAMATION_MARK_COUNT``` are hidden and cannot be accessed.

* When we are using the 'module pattern' we are basically just using an IIFE, but with the ```export``` keyword which makes the functions and variables to the public interface. 
 * With the below example, the same IIFE above is exported to the public interface so calling ```explain("Hello")``` will not throw an error:
 
```
(function(exports) {
  var EXCLAMATION_MARK_COUNT = 5

  function exclaim(string) {
    return string + "!".repeat(EXCLAMATION_MARK_COUNT);
  };

  exports.exclaim = exclaim;
})(this);
```
However, we will not be able to access ```EXCLAMATION_MARK_COUNT```. So the function is available but not the variables inside of that function. This means that our variables will not clash with the variable in the reset of the program. 

### Careers Workshop
* Becks, Hannah and Nick.
* Pathway - in contract with Makers for a year. Idea is that you become permanent after a years.
- Support from Will and Lauren with career progression. 
- Makers provide the necessary tech coaching.
* Meetups:
- e.g. Ruby User Groups.
* blog
* tweet
* message Hannah or Nick to say want to work in Brighton.
* process in final project v important

* 3-5 projects on CV (inc. final project). 
* quite often have to talk about the final project in the interview.
* READMEs important.

### REACT
* It is a single page application framework.
* The main app outputs to the ```id="root"``` element.
* Only for the View part of the MVC model. 
* COMPONENTS - e.g. on a Todo web app you might have:
- a "Search" component for the search bar section of the page
- a "TodoList" component for listing the all the todos. 
- a "Todo" component for each individual Todo item
- an "AddTodo" component for adding a new Todo item

* STATE:
- components have a "state" which is an object which determines how the components renders and behaves.

* Uses ```jsx``` and this means you cannot use ```class``` in the html file but need to use ```className``` instead. 

### Retrospective
* The Note App is not a good example of single page web app. It is far common that you make HTTP requests to different API end points. 
* Facebook, for example is not completely single page - log in, register pages, profile pages are separate, but the 'feed' is only on one page. 
* Might want to isolate the Ajax requests - so you hard code what you get back from the request.

### My end of week reflection:

Overall, you rated this week: 7
You felt it was because of this: I am very much enjoying the course but at times I feel like I am not keeping up. I also feel like some of the ruby, TDD with rspec we learned at the start of the course which was second nature to me is not any longer.
You decided these resources and/or strategies could be useful: I am going to continue going to process workshops and do the odd kata to practice TDD and ruby.
Send a coach a message on Slack and we can have a chat anytime!

----------------------------
Week Objectives: 7
Your objectives this week were: Build a front-end app in Javascript Work competently in Javascript Reason about asynchronous behaviour in Javascript
You felt the primary reason for your score was: I feel pretty confident at building a front end app in JS. In terms of working competently in Javascript I feel I have to do a lot of googling other than the very basics. I think i understand what asynchronous behaviour is in JS but I am not to confident about this from a practical perspective.
You decided these resources and/or strategies could be useful: A workshop on asyncrhonous behaviour would have been helpful perhaps or some practicals.
----------------------------
Personal Objectives: 7
Your objectives this week were: Go to a process workshop. Understand the module pattern.
You felt the primary reason for your score was: I went to a process workshop and this was really helpful practice for a review. Whilst I have a basic understanding of the module pattern I would like to understand when this might be useful.
You decided these resources and/or strategies could be useful: A youtube tutorial or an example project when module is used.
----------------------------

### Asychronous JS
* Unlike syncronous JS which waits for 1 action to complete before moving onto the next, asychronous JS can make a request in one line of code and then the rest of the code gets read whilst we are waiting for the request to be handled. 

* Diagram to explain this:
```
- Code line
- Code line
- Code line (a request) --------------------------------
- Code line                                             |
- Code line                                             |
- Code line                                         ( DATA )
- Code line                                             |
- Code line                                             |
- Callback (executed when response to request rec'd) --- 
```
* Above is just one way to handle a asynchronous request (i.e. using a callback). You can also use:
- Promises (better)
- Generators (even better but only ES6)

### Ajax requests
* An Ajax get request using jQuery looks like this: 
```
$.get("address/of/where/we/want/to/get/the/data/from", theCallbackFunction(dataWeAreGettngBack) {
  console.log(data) // <--what gets executed when the data comes back;
});
```
