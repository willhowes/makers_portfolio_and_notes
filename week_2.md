# Week 2 Goals and Notes

[Week 2 Outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-2)

## Goals for the Week:
GIVEN BY MAKERS:
1. Use all of week 1's skills (don't underestimate the importance of this)

2. Break one class into two classes that work together, while maintaining test coverage

3. Unit test classes in isolation using mocking

4. Explain some basic OO principles and tie them to high level concerns (e.g. ease of change)

5. Review another person's code and give them meaningful feedback

PERSONAL
6. Write a blog.

## How did I achieve my goals?

### 1. Use all of week 1's skills (don't underestimate the importance of this)
Achieved by:

### 2. Break one class into two classes that work together, while maintaining test coverage
Achieved by:

### 3. Unit test classes in isolation using mocking
Achieved by:

### 4. Explain some basic OO principles and tie them to high level concerns (e.g. ease of change)
Achieved by:

### 5. Review another person's code and give them meaningful feedback
Achieved by:
* Reviewed [Ritchie's Aiport Challenge](https://github.com/makersacademy/airport_challenge/pull/1465) 


## Daily Goals

### Weekend

### Friday

### Thursday

### Wednesday

### Tuesday

### Monday

1. Try in pair programming to actually use proper driver-navigator process. Previously, this has been a bit ad hoc. 

2. Ask for feedback on my pair programming. Is there anything I can do better?

3. Learn about code reviewing.


## Takeaways & Reflections from the week

### Ruby
* Re MOCKS and DOUBLES - I THINK that you make a mock for the class that you are currently test and you create a double for a class outside of the one you are testing.
 * Use for unit tests only as they isolate testing the class. When mocking is used you will need separate feature tests as unit tests using mocks, etc will not check the program features actually work (as classes might not be interating correctly).
  * Not good practice to use allow(subject)
  Example of doubling and stubbing for a class:
```weather = double :fake_weather```
```allow(weather).to receive(:stormy?).and return(false)```
   
   the first line above effectively creates a blank class and then creates a new instance of it, i.e. 
```class weather```
```end```
```weather.new```

* Pry is a useful tool. Can run features like in irb when you run rspec. 

### READMEs
* Should explain my process better for code reviewers. e.g Airport Challenge did not explain WHY I tought I should have methods on the Plane class.  

### Feedback/Code Reviews
* It is valuable for a number of reasons...
  * uncover common gaps
  * evidence of learning
  * helps to improve
  * find out things you don't already know.
* When reviewing, if you are not sure whether you are right, ask a question. 
* There are many solutions to the same problem. There is no best solution.


