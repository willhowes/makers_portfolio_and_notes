# Week 1 Goals and Notes

[Week 1 Outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/ "WEEK 1")

## Goals for the Week:

1. Test-drive a simple program using objects and methods

2. Pair using the driver-navigator style

3. Follow an effective debugging process

4. Describe some basic OO principles like encapsulation, SRP

## How did I achieve my goals?

### 1. Test-drive a simple program using objects and methods

### 2. Pair using the driver-navigator style
- Effective pairing using driver-navigator style on the Week 1 [Boris Bikes exercise](https://diode.makersacademy.com/students/dearshrewdwit/projects/1418)
- Gave and received feedback to pair programming partners after each session.
- Appreciated when not being communicative and/or assertive enough.
- Learned to appreciate to follow the process of building a project step-by-step rather than jumping ahead with additional features before the main objects and their messages/methods are built.

### 3. Follow an effective debugging process
- Used the following method for debugging in the [FizzBuzz debugging exercise] (https://github.com/willhowes/skills-workshops/tree/master/week-1/debugging_fizzbuzz):
  - Tighten the loop by reading the error code to find out on what line the code fails.
  - Get visibility using "p" to print to the screen variables and statements to check what the line of code is doing
  - Once the issue is discovered, amend the code so the test passes.

### 4. Describe some basic OO principles like encapsulation, SRP



## Daily Goals

### Friday
1. Check concepts from previous day's pair programming understood. 20-30mins
* Achieved by reading through the walkthroughs. In particular this reinforced:
  * That you should commit after every RED-GREEN-REFACTOR cycle
  * That default values can be set to default values can be set to an instance variable. This is done using the following syntax the ```def initialize(capacity=20)```. This can also be used to set default values to parameters for any other method.
  * That in is good practice to wrap collections (an array being a type of collection) where possible. A collection is wrapped when it has a: 
    * STATE - the array is internal to the class. It will hold things, and we can manipulate it as the program runs.
    * BEHAVIOUR - the methods that interact with the internal array.

2. Further TDD practice to reinforce following a slow a methodical process. -60mins

3. If more time have a look again at debugging_1. 

4. For pair programming, try to not to feel rushed when in the driver role. 

### Thursday
1. Make sure all concepts from previous day's pair programming fully understood, as some of steps were implemented v quickly. - 20-30 mins.
* Achieved by reading through the walkthroughs. 
  * Reinforced my understanding of one-liner rspec syntax (in particular that ```is_expected``` is the same as ```expect(subject)```. 
  * Remembering to do simplest thing first to pass a unit test. 
  * Recalled that we should feature test (irb) first, then create a Unit Test (in spec) before making changes to the code. 
  * Learned that when an object needs to store something and allow access to something you can use "attributes" or "instance varaibles"

2. [Practice TDD](https://diode.makersacademy.com/students/dearshrewdwit/projects/908) so that I can work towards being able to TDD anything and have a methodical approach - 45-60mins.
- Achieved by creating a Roman Numerals Converter using TDD. I also made a start on the Birthdays practical.
* I used a methodical approach as taught by Makers Coach Sophie. i.e. :
  * Create a user story to ascertain what is required of the program
  * Write first test to fail (using rspec) - make it pass the test by adding the simplest code possible - refactor the code - repeat using further tests


### Wednesday
1. Go through Boris Bikes steps again to understand some of the concepts better - 1hr
  - Achieved by looking the extra resources. e.g. looked at youtube videos for feature test and stack trace to better understand these.
2. Improve on debugging (slow it down, take it step  by step) - 1hr
  - Achieved this by doing a [further debugging exercise](https://github.com/makersacademy/skills-workshops/tree/master/week-1/debugging_1) and making sure I just look at one test at a time and hone in on the failing line, using "p" to look at what each component part does, trying this and repeating the loop if it doesn't work or for further failing tests.


## Takeaways & Reflections from the week

### Regarding Setting Goals 
- The loop:  (GOALS)-(DO/PRACTICE)-(REFLECT/EVIDENCE/F'BACK)-repeat.
S pecific
M easurable
A chievable
R elevant
T ime-bound

### TDD
- Feature test is a test of a program/project feature within irb or other REPL.

### Debugging
- Slow, methodical approach to each issue one at a time is best.

### Pair programming
* ```attr_reader``` can be used for instance variables to be accessed by other classes.
* You can use Predicates rspec matcher tests: prefix a method with ```be_``` and remove the ```?```. 
 * e.g.   ```expect(5).to be_instance_of Fixnum``` 
* Single Responsibility Principal - i.e. that a method should do one thing only. e.g. In our Week 1 Pair Programming Project to create a replica of the Boris Bikes system, instead of having the method ```receive_bike``` check if the docking station is full and also add a Bike class to the Docking Station (i.e. it does two things), this can be split into two methods:   

```  def full?
    if @available_bikes.length >= @capacity
      true
    end
  end

    def receive_bike(bike)
      if full?
        raise "Docking Station full"
      else
        @available_bikes << bike
      end
    end

