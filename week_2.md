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
* Achieved by:
 * Going back over week 1's goals and my takeaways from the week, it was clear that I have continued to use this skills this week. For example, on a number of challenges this week I have need to use the debugging technique of reading the error message, tightening the loop (using p), making and adjustment and then repeating this process if a further error is raised.  


### 2. Break one class into two classes that work together, while maintaining test coverage
Achieved by:
 * During pair programming working on [the Oystercard challenge](https://github.com/makersacademy/course/tree/master/oystercard), [step 13](https://github.com/makersacademy/course/blob/master/oystercard/13_create_station_class.md), we extracted all elements of the ```Oystercard``` class that related just to the journey (so that the ```Oystercard``` class conforms to SRP) and put these into a ```Journey``` class and putting the unit tests for anything relating to the journey into a new ```journey_spec``` file so that test coverage was maintained. 
### 3. Unit test classes in isolation using mocking
* Achieved by:
 * Used this technique in the oystercard challenge. When testing the ```Station``` class we create a mock station with arbitrary name of a station and zone number which we can test against in the unit tests. This means that when we run the unit tests they will be affected by any issues with other classes and methods. Example:
``` 
 require 'station'                                           
describe Station do

  subject {described_class.new(name: "Old Street", zone: 1)}

  it 'knows its name' do                      
    expect(subject.name).to eq("Old Street")              
  end                                                   

  it 'knows its zone' do                                                     
    expect(subject.zone).to eq(1)                                 
  end
end
```
### 4. Explain some basic OO principles and tie them to high level concerns (e.g. ease of change)
Achieved by:
* SRP (Single Responsibility Principal) - I understand that a class or method should only do one thing. 
* Encapsulation - I can explain that this is the breaking up the codes's objects and methods into classes 
* Private -understood the basics of this concept. See take-aways and notes below.
 * OO Design patterns 
  * Polymorphism - ditto
  * Inheritance - ditto
  * Delegation/Fowarding - ditto
  * Dependancy injection - ditto

### 5. Review another person's code and give them meaningful feedback
Achieved by:
* Reviewed [Ritchie's Aiport Challenge](https://github.com/makersacademy/airport_challenge/pull/1465) 

### 6. Write a blog

## Daily Goals

### Weekend

### Friday
1. Learn about how best to approach giving feedback. 
* Achieved by:
 * Attending the workshop...[INSERT NOTES BELOW]


2. Review week 1's skills to check I still understand these and am able to put them into practice. 
* Achieved by: Going over week 1's goals/skills again. I have been using all these this week.

### Thursday
1. Learn and understand about delegation
* Achieved by:
 * Attended the workshop. Notes [here](https://github.com/willhowes/makers_portfolio_and_notes/blob/master/delegation_workshop_notes).

2. Understand basics of dependancy injenction.
* Achieved by:
 * See takeaways below 
 
### Wednesday
1. Complete and understand the Inheritance skills workshop
* Achieved by:
 * Completed the [inheritance skills workshop](https://github.com/makersacademy/skills-workshops/tree/master/week-2/inheritance). See below in takeaways for understanding of inheritance.

2. Start mocking workshop and enhance understand of this feature in rspec.
* Achieved by:
 * Starting the [mocking workshop](https://github.com/makersacademy/skills-workshops/tree/master/week-2/mocking_2).
 * Understanding the reasons we use mocking (see takeaways below).

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
```
weather = double :fake_weather
allow(weather).to receive(:stormy?).and return(false)
```
   
   the first line above effectively creates a blank class and then creates a new instance of it, i.e. 
```class weather end
weather.new
```

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
* Need to be careful that when coding solo or in pairs, even when good test-first practice is be followed on the whole, not to ahead, skipping steps. Still quite often when trying to make a test pass, one would not try to make the test pass in the simplest way possible, but rush ahead and try to make the code do what we want it to.
* To use the coverage gem: https://docs.google.com/document/d/1iXK7X9_jSphkHUWerEhipTgduB4rlSa7qOZCCEu8kJ4/edit
* Really helpful [Airport challenge walkthrough on youtube](https://www.youtube.com/watch?v=Vg0cFVLH_EM&t=167s). Takeaways from this:
 * It is worth creating a "features" folder under rspec for only feature tests, i.e. ```spec/features/user_stories_spec```. To make things clearer, you can copy and paste the user story into the feature test so you can double check against this to make sure you are fufilling the client's requirements. You can make a feature test that simply doesn't raise an error, e.g. ```expect{ airport.land(plane).not_to raise_error```; then when you get the error message after running it, use the error to make a unit test that will fail in the same we. 
 * Best practice in rspec is to use, e.g. ```subject(:airport) { described_class.new``` at the top under ```describe``` when testing, so then you can test using ```airport``` rather than ```subject```.
 * When using feature tests in rspec, don't use doubles for the classes. You want to check all the classes and methods work together. 
 * Process should be:
  1. RED
   a. Make Feature Test based on user story, read error message
   b. Make Unit Test to fail with the same error message
   
 2. GREEN 
  a. Get the Unit Test to pass
  b. Get the Feature Test to pass too
 
 3. REFACTOR
 
 * You do not need to test anything that is not accessable from outside the class (i.e. instance variables, private methods).
 * If you have an ```it``` that says ```'when...``` then this is a good example of when you should use a ```context``` block. Example from the Airport challenge:
```
describe '#land' do
 context 'when full' do
  before do
   allow(airport).to receive(:full).and_return(true)
  end
  it 'raises an error' do
   capacity.times....
   #etc...
  end
 end
end
```
 * If during TDD you are introducing a method which you are stubbing and is not being used by the public interface then this is a clue that this method should be a private method. 
 * If you want to write a test so you don't forget it but don't want it to run initially use ```xit```
 * if you get an error message like ```#<double :plane> received unexpected message :land``` then you need to allow the double to receive the message (i.e. the method), e.g. ```let(:plane) {double: :plane, land: nil}```

### Mocking
* This is where we create mocks of classes or other objects (e.g. an instance variable) so that when we do unit tests they are not dependant on other classes or other features of the program. Here is an example from the week 1 Boris Bikes challenge. We create doubles of a working_bike, a broken_bike and an instance of the DockingStation class. We also later create a mock bikes array containing the bike doubles:

```
describe DockingStation do
  let(:working_bike)        { double('working bike', working?: true) }
  let(:broken_bike)         { double('broken bike', working?: false) }

  subject(:docking_station) { described_class.new(bikes) }

  describe '#working_bike_count' do
    context '1 working bike' do
      let(:bikes) { [working_bike] }

      it "returns 1" do
        expect(docking_station.working_bike_count).to eq(1)
      end
    end

    context '1 working bike, 1 broken bike' do
      let(:bikes) { [working_bike, broken_bike] }

      it "returns 1" do
        expect(docking_station.working_bike_count).to eq(1)
      end
    end
  end

  describe '#random_bike_working?' do
    let(:bikes) { [working_bike, broken_bike] }

    context 'random bike is working' do
      it 'returns true' do
        srand(1) # this argument may need to change

        expect(docking_station.random_bike_working?).to eq(true)
      end
    end

    context 'random bike is broken' do
      it 'returns false' do
        srand(2) # this argument may need to change

        expect(docking_station.random_bike_working?).to eq(false)
      end
    end
  end
end
```

### Domain Modelling
* There are many ways to do this, in fact a Domain Model can be in any form so long as it correctly represents the program we want to build.
* Should be readable by someone who doesn't read code. 
* User is external to the program, so do not include it in your nouns (i.e. class). Only needed when you have user accounts.
* When you use a sequence diagram where the message arrow ends is usually the class where the method will be.

## OO Principals
* Polymorphism - (poly = many, morph = forms). This is where a class takes many forms. This is also linked to duck-typing (i.e.  if it behaves like a duck then you can rely on it being a duck). For example if the object given as an argument to a method or class has the method we are expecting then you can rely on that object being the object we want. Working example: duck and fake_duck will be treated as the same providing they both have the .quack method. 

* Delegation/Fowarding - my understanding is that, having split classes up so using SRP, forwarding is where by messages are forwarded from the new class to the old class. For example, where you have password checker and you take this out of a profile class then the new password_checker class will need to forward to the profile class a message to confirm if password_checker returns true. Remember that when delegating the functions of one class into a new class, when communicating between the two, you do not want one class to change the 'state' (i.e. a variable) of a class, you only want to ask it something (e.g. in the oystercard challenge, and instance of the ```Oystercard``` class will ask an instance of the ```Journey``` class whether the journey is ```complete?```, it should not tell the instance of the ```Journey``` class to change its ```@complete``` instance variable to true, as this would make the ```Journey``` vulnerable to changes from outside the class.  

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
* Dependency Injection - this is where, for example, class_one depends on the behaviour of class_two, we can inject class_two on the initialization of class_one. For example:
 ```
class Greeter
  def initialize(hello = Hello.new)
    @hello = hello
  end

  def greet
    "#{@hello.get} there!"
  end
end

class Hello
  def get
    "Hello"
  end
end
```
* Private methods - The first thing to understand is that each class has state (variables) and methods (behaviour). A class's state (variables) should ideally only be changed from with the class. Otherwise, this functionality will vulnerable to users or other classes. Therefore, we should (as much as possible) put methods which change a class's state under private which means they can only be called within the class itself (i.e. by other methods inside that class). In this way, private methods are like internal helper methods. However, you can access a private method from outside of the class if you use a public method to access the private method. For example:

```
class Person
  def speak
    puts "Hey, Tj!"
  end
  
  def whisper_louder
    whisper
  end 
  
private 
  def whisper
    puts "His name's not really 'Tj'." 
  end 
end

you = Person.new 
you.speak # "Hey, Tj!"
a_hater = Person.new
a_hater.speak # "Hey, Tj!"
a_hater.whisper # NoMethodError
a_hater.whisper_louder # "His name's not really 'Tj'."
```
 
Here we access the ```whisper``` method by calling the ```whisper_louder``` method from outside the class.


