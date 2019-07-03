# Week 1 Goals and Notes

[Week 1 Outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/ "WEEK 1")

## Goals for the Week:

1. Test-drive a simple program using objects and methods

2. Pair using the driver-navigator style

3. Follow an effective debugging process

4. Describe some basic OO principles like encapsulation, SRP

## How did I achieve my goals?

### 1. Test-drive a simple program using objects and methods
* Test drove the [birthday practical](https://github.com/makersacademy/birthdays).
* Praciced a lot of TDD during pair programming sessions.
* Used TDD for the [Weekend Challenge](https://github.com/makersacademy/airport_challenge). At times, when solving more difficult/complex logical problems I forgot to test before coding, but on the whole I followed the procedure of RED-GREEN-REFACTOR.

### 2. Pair using the driver-navigator style
- Effective pairing using driver-navigator style on the Week 1 [Boris Bikes exercise](https://diode.makersacademy.com/students/dearshrewdwit/projects/1418)
- Gave and received feedback to pair programming partners after each session.
- Appreciated when not being communicative and/or assertive enough.
- Learned to appreciate to follow the process of building a project step-by-step rather than jumping ahead with additional features before the main objects and their messages/methods are built.

### 3. Follow an effective debugging process
- Used the following method for debugging in the [FizzBuzz debugging exercise](https://github.com/willhowes/skills-workshops/tree/master/week-1/debugging_fizzbuzz):
  - Tighten the loop by reading the error code to find out on what line the code fails.
  - Get visibility using "p" to print to the screen variables and statements to check what the line of code is doing
  - Once the issue is discovered, amend the code so the test passes.

### 4. Describe some basic OO principles like encapsulation, SRP
* Learned about [Encapsulation & Cohesion](https://github.com/makersacademy/skills-workshops/blob/master/practicals/object_oriented_design/encapsulation.md):
  * Each class should have one responsibility. A class has high cohesion if everything it does relates to its purpose.
* SRP - A method or class should do one thing only. If it does more than one, refactor using additional methods. 

## Daily Goals

### Weekend
1. Reinforce what I have learned in week 1 through the [Airport Challenge](https://diode.makersacademy.com/students/neoeno/projects/33).
* Achieved by:
  * Continuing to practice TDD on the weekend challenge.
  
2. Try to understand Mocks and Stubs
* Acheived by:
  * Reading going through the [reference material](https://relishapp.com/rspec/rspec-mocks/docs) and watching some youtube videos also. 
  * Initially I could not get the stubs to work on my program but after further reading and watching youtube videos I realise that a mock needed to be created first. Once a mock was created for the Airport class the stubs also worked. 

### Friday
1. Check concepts from previous day's pair programming understood. 20-30mins
* Achieved by reading through the walkthroughs. In particular this reinforced:
  * That you should commit after every RED-GREEN-REFACTOR cycle
  * That default values can be set to default values can be set to an instance variable. This is done using the following syntax the ```def initialize(capacity=20)```. This can also be used to set default values to parameters for any other method.
  * That in is good practice to WRAP COLLECTIONS (an array being a type of collection) where possible. A collection is wrapped when it has a: 
    * STATE - the array is internal to the class. It will hold things, and we can manipulate it as the program runs.
    * BEHAVIOUR - the methods that interact with the internal array.
  * [Single Responsibility Principal](https://thoughtbot.com/blog/back-to-basics-solid). A method should do one thing only. If it does more than one, refactor using additional methods.

2. ODD - encapsulation and SRP.
* Acheieved by: 
  * Learning about SRP (Single Responsibility Responsibility Principal) understood during Thursday's pair programming (see above)
  * Practiced using applying SRP and encapsulation by refactoring code where a class had a method which did not relate to the main purpose of the class.  

3. Further TDD practice to reinforce following a slow a methodical process. -60mins
* Achieved by: 
  * Test driving the [birthday practical](https://github.com/makersacademy/birthdays).

4. For pair programming, try to not to feel rushed when in the driver role. 
* Achieved by:
  * Initially still felt a bit rushed trying to sort out a new git respository. After this, I was better at taking my time and following the process.

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

### Emotional Itelligence, Wellbeing, etc
* 'I feel the way I feel and that is OK'
* Acknowledging when you are stressed or anxious
* Appreciating that many other people are experiencing the same struggles
* DO NOT compare yourself to others
* It is OK if the program does not work. This is not meant to be easy. 
* If you get stuck on a particular problem time-box it - 20-30mins. 
* Learn to walkaway and take breaks, particularly when stuck. 
* It is expected that we will feel uncomfortable during the course. This is when you are learing. On if your feel overwhelmed then should reach out to a coach. 

* Notes from meditation session:

> Emotional Intelligence 
> 1. Self awareness
> 2. Empathy
> 3. Motivation 
> 4. Self regulation 
> 5. Social skills
>
> 3 competencies of Self Awareness 
> 1. Emotional awareness 
> 2. Accurate self assessment 
> 3. Confidence
>
> Affect labelling
> Stop and take a moment to reflect on your body. Label the sensations in your body.
>
> We Handle emotions in 4 ways
> 1. Suppression (consciously)
> 2. Repression (unconsciously)
> 3. Expression (body language, venting, demonstrating) 
> 4. Escape
>
> Mantra - I feel the way I feel and that's okay.

### Regarding Setting Goals 
- The loop:  (GOALS)-(DO/PRACTICE)-(REFLECT/EVIDENCE/F'BACK)-repeat.
S pecific
M easurable
A chievable
R elevant
T ime-bound

### TDD
* Feature test is a test of a program/project feature within irb or other REPL. Have found that, although it make take longer in the short term, doing a feature test in irb before doing a unit test in rpspec really helps to understand what we want the program to do. 
* Important to take time to make sure the rspec syntax is correct. Regularly got thrown off in pairing when using wrong brackets, e.g. it should be ```expect{subject.method}``` not ```expect(subject.method```.

### Debugging
* Slow, methodical approach to each issue one at a time is best.

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
    end```



