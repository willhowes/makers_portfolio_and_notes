# Week 7
[Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-7)

## Week's Goals

1. Can you write a frontend, single page app using only pure JavaScript?

### Have I achieved the above goals?

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

