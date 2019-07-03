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
 * During pair programming working on [the Oystercard challenge](https://github.com/makersacademy/course/tree/master/oystercard), [step 13](https://github.com/makersacademy/course/blob/master/oystercard/13_create_station_class.md), we extracted all elements of the ```Oystercard``` class that related just to the journey (so that the ```Oystercard``` class conforms to SRP) and put these into a ```Journey``` class and putting the unit tests for anything relating to the journey into a new ```journey_spec``` file so that test coverage was maintained. 
### 3. Unit test classes in isolation using mocking
Achieved by:

### 4. Explain some basic OO principles and tie them to high level concerns (e.g. ease of change)
Achieved by:
* SRP (Single Responsibility Principal) - I understand that a class or method should only do one thing. 
* Encapsulation - I can explain that this is the breaking up the codes's objects and methods into classes 
* Private
 
 * OO Design patterns 
  * Polymorphism - understood the basics of this concept. See take-aways and notes below. 
  * Inheritance - ditto
  * Delegation/Fowarding - ditto
  * Dependancy injection

### 5. Review another person's code and give them meaningful feedback
Achieved by:
* Reviewed [Ritchie's Aiport Challenge](https://github.com/makersacademy/airport_challenge/pull/1465) 

### 6. Write a blog

## Daily Goals

### Weekend

### Friday

### Thursday

### Wednesday
1. Complete and understand the Inheritance skills workshop
* Achieved by:
 * Completed the [inheritance skills workshop](https://github.com/makersacademy/skills-workshops/tree/master/week-2/inheritance)

2. Start mocking workshop and enhance understand of this feature in rspec.

### Tuesday
1. Learn about Polymorphism. Attempt the skills workshop.
* Achieved by:
 * Read up about the subject and having it explained by a coach and discussing with peers. An excellent example provided by a peer https://github.com/willhowes/animal_polymorphism


2. Learn more about Domain Modelling
* Achieved by:
 * Attending and learning at the skills workshop and putting this into practice on these praticals: https://github.com/makersacademy/skills-workshops/blob/master/week-2/domain_model_diagramming/README.md

 * See below for my takeaways from the skills workshop

BONUS: Gave and received feedback on pairing session in the afternoon. 

* My feedback on my pairing partner:

> Great pair programming earlier. I thought it went well.
>
> I think we went at a good pace but didn't skim over things. Swapping roughly every hour seemed like the right amount of time.
>
> You were great at stopping me in my tracks when I went off on a bit tangent. I think that's really important to stop getting stuck in a rut.
>
> You were also great at coming up with workable solutions v quickly and explained them well to me.  Something I need to get better at I think. I've never been great at explaining myself!
>
> Hope that's enough for feedback but let me know if you've got a questions.

* My pair's feedback on me

> I personally thought that this was the most efficient pairing session I have had on this course so far. You were really good at implementing the driver, navigator roles as intended. Really good at being open to solutions and listening to my opinions as well.
>
> I felt that the approaches you were taking to solving the problems showed that you had a good grasp of the OOP principles and TDD methods we have been given so far on the course as well.


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
* Re MOCKS and DOUBLES - I THINK that you make a mock for the class that you are currently testing and you create a double for a class outside of the one you are testing.
 * Use for unit tests only as they isolate testing the class. When mocking is used you will need separate feature tests because the unit tests using mocks, etc will not check the program features actually work (as classes might not be interating correctly).
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
* To use the coverage gem: https://docs.google.com/document/d/1iXK7X9_jSphkHUWerEhipTgduB4rlSa7qOZCCEu8kJ4/edit

### Domain Modelling
* There are many ways to do this, in fact a Domain Model can be in any form so long as it correctly represents the program we want to build.
* Should be readable by someone who doesn't read code. 
* User is external to the program, so do not include it in your nouns (i.e. class). Only needed when you have user accounts.
* When you use a sequence diagram where the message arrow ends is usually the class where the method will be.

## OO Principals
* Polymorphism - (poly = many, morph = forms). This is where a class takes many forms. This is also linked to duck-typing (i.e.  if it behaves like a duck then you can rely on it being a duck). For example if the object given as an argument to a method or class has the method we are expecting then you can rely on that object being the object we want. Working example: duck and fake_duck will be treated as the same providing they both have the .quack method. 

* Delegation/Fowarding - my understanding is that, having split classes up so using SRP, forwarding is where by messages are forwarded from the new class to the old class. For example, where you have password checker and you take this out of a profile class then the new password_checker class will need to forward to the profile class a message to confirm if password_checker returns true.

* Inheritance - where by one class inherits all the features of a parent. Warning - it will copy over all the parent's classes methods, even if you don't want them allow. Therefore, if you want a feature that will only apply to some of the child classes, then you will need to create another class and use compostion, for example:

```ruby
class Engine
  def start
    "vroooom!"
  end
end

class Car < Vehicle
  attr_reader :engine

  def initialize(top_speed, engine = Engine.new)
    super(top_speed)
    @engine = engine
  end

  def start_engine
    engine.start
  end
end
```
