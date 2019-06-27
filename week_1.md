# WEEK 1 GOALS & NOTES

[Week 1 Outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/ "WEEK 1")

## Daily Goals

### Thursday
1. Make sure all concepts from previous day's pair programming fully understood, as some of steps were implemented v quickly. - 20-30 mins.
* Achieved by reading through the walkthroughs. 
  * Reinforced my understanding of one-liner rspec syntax (in particular that ```is_expected``` is the same as expect(subject)```. 
  * Remembering to do simplest thing first to pass a unit test. 
  * Recalled that we should feature test (irb) first, then create a Unit Test (in spec) before making changes to the code. 
  * Learned that when an object needs to store something and allow access to something you can use "attributes" or "instance varaibles"

2. [Practice TDD](https://diode.makersacademy.com/students/dearshrewdwit/projects/908) so that I can work towards being able to TDD anything and have a methodical approach - 45-60mins.
- Achieved by creating a Roman Numerals Converter using TDD.
* I used a methodical approach as taught by Makers Coach Sophie. i.e. :
  * Create a user story to ascertain what is required of the program
  * Write first test to fail (using rspec) - make it pass the test by adding the simplest code possible - refactor the code - repeat using further tests


### Wednesday
1. Go through Boris Bikes steps again to understand some of the concepts better - 1hr
  - Achieved by looking the extra resources. e.g. looked at youtube videos for feature test and stack trace to better understand these.
2. Improve on debugging (slow it down, take it step  by step) - 1hr
  - Achieved this by doing a [further debugging exercise](https://github.com/makersacademy/skills-workshops/tree/master/week-1/debugging_1) and making sure I just look at one test at a time and hone in on the failing line, using "p" to look at what each component part does, trying this and repeating the loop if it doesn't work or for further failing tests.

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

## Takeaways & Reflections
### Wednesday
Re Goals: 
- The loop:  (GOALS)-(DO/PRACTICE)-(REFLECT/EVIDENCE/F'BACK)-repeat.
S pecific
M easurable
A chievable
R elevant
T ime-bound

Re TDD:
- Feature test is a test of a program/project feature within irb or other REPL.

Re Debugging:
- Slow, methodical approach to each issue one at a time is best.

Re: Pair programming
- Learned about attr_reader being used for instance variables to be accessed by other classes.
- Learned about Predicates rspec matcher tests: prefix a method with "be_" and remove the "?". 
-- e.g.   ```expect(5).to be_instance_of Fixnum``` 
