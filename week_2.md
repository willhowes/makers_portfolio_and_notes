# Week 2 Goals and Notes

[Week 2 Outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-2)
N.B. This week is a continuation of Week 1. So fine to go back and go over things again.

## Goals for the Week:
GIVEN BY MAKERS:
1. Use all of week 1's skills (don't underestimate the importance of this). Just check that using these in this week's exercises...

2. Break one class into two classes that work together, while maintaining test coverage

3. Unit test classes in isolation using mocking

4. Explain some basic OO principles and tie them to high level concerns (e.g. ease of change). i.e. explain why you would use these basic OO principals.
 e.g.s of basic principals:
  * SRP
  * Encapsulation
  * Private
  
  
  * OO Design patterns
   * Polymorphism ([examples](https://github.com/makersacademy/skills-workshops/blob/master/practicals/object_oriented_design/oo_relationships.md#polymorphism))
   * Inheritance
   * Delegation/Forwarding - ([examples](https://github.com/makersacademy/skills-workshops/blob/master/practicals/object_oriented_design/oo_relationships.md#forwarding))
   * Dependancy injection
 

5. Review another person's code and give them meaningful feedback

PERSONAL
1. Write a blog.

## How did I achieve my goals?

### 1. Use all of week 1's skills (don't underestimate the importance of this)
Achieved by:

### 2. Break one class into two classes that work together, while maintaining test coverage
Achieved by:

### 3. Unit test classes in isolation using mocking
Achieved by:

### 4. Explain some basic OO principles and tie them to high level concerns (e.g. ease of change)
Achieved by:
* SRP (Single Responsibility Principal) - I understand that a class or method should only do one thing. 
* Encapsulation - I can explain that this is the breaking up the codes's objects and methods into classes 
* Private
 
 * OO Design patterns 
  * Polymorphism - (poly = many, morph = forms). This is where a class takes many forms. This is also linked to duck-typing (i.e.  if it behaves like a duck then you can rely on it being a duck). For example if the object given as an argument to a method or class has the method we are expecting then you can rely on that object being the object we want. Working example: duck and fake_duck will be treated as the same providing they both have the .quack method. 
  * Inheritance
  * Delagation/Fowarding - my understanding is that, having split classes up so using SRP, forwarding is where by messages are forwarded from the new class to the old class. For example, where you have password checker and you take this out of a profile class then the new password_checker class will need to forward to the profile class a message to confirm if password_checker returns true.
  * Dependancy injection

### 5. Review another person's code and give them meaningful feedback
Achieved by:
* Reviewed [Ritchie's Aiport Challenge](https://github.com/makersacademy/airport_challenge/pull/1465) 


## Daily Goals

### Weekend

### Friday

### Thursday

### Wednesday

### Tuesday
1. Learn about Polymorphism. Attempt the skills workshop

2. Learn more about Domain Modelling

### Monday

1. Try in pair programming to actually use proper driver-navigator process. Previously, this has been a bit ad hoc. 
* Achieved by:
 * Before pairing I had a chat with my pair partner about the the driver-navigator roles. We agrees that it was fine for both driver and navigator to be thinking about what tests and code to test but that navigator should take precedence and lead the way somewhat. This worked well during our pairing session. I occassionally forgot that the navigator should take precedence but on the whole the navigator fairly naturally led the way.

2. Ask for feedback on my pair programming. Is there anything I can do better?
* Achieved by:
 * My pair partner and I had a chat after the session to discuss how we thought it went. We both agreed that it went well but that sometimes we did jump ahead with making more complicated tests rather than basic/simple tests first. 

3. Learn about code reviewing.
* Achieved by:
 * Attended the workshop about code reviews at the start of the day (see takeaways below). 
 * Reviewed [Ritchie's Aiport Challenge](https://github.com/makersacademy/airport_challenge/pull/1465). 


## Takeaways & Reflections from the week

### Ruby
* Re MOCKS and DOUBLES - I THINK that you make a mock for the class that you are currently test and you create a double for a class outside of the one you are testing.
 * Use for unit tests only as they isolate testing the class. When mocking is used you will need separate feature tests as unit tests using mocks, etc will not check the program features actually work (as classes might not be interating correctly).
  * Not good practice to use allow(subject)
  Example of doubling and stubbing for a class:
```weather = double :fake_weather```
```allow(weather).to receive(:stormy?).and return(false)```
   
   the first line above effectively creates a blank class and then creates a new instance of it, i.e. 
```class weather end```
```weather.new```

* Pry is a useful tool. Can run features like in irb when you run rspec. 

### READMEs
* Should explain my process better for code reviewers. e.g Airport Challenge did not explain WHY I tought I should have methods on the Plane class.  

### Feedback/Code Reviews
* It is valuable for a number of reasons:
  * uncover common gaps
  * evidence of learning
  * helps to improve
  * find out things you don't already know.
* When reviewing, if you are not sure whether you are right when making a suggestion, just ask a question about the code. 
* There are many solutions to the same problem. There is no best solution.

### TDD
* Need to be careful that when coding solo or in pairs, even when good test-first practice is be followed on the whole, not to ahead, skipping steps.

### Domain Modelling
* There are many ways to do this, in fact a Domain Model can be in any form so long as it correctly represents the program we want to build.
* Should be readable by someone who doesn't read code. 
* User is external to the program, so do not include it in your nouns (i.e. class). Only needed when you have user accounts.
