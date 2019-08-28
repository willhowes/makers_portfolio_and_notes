
# Weeks 10
[Week outline](https://github.com/makersacademy/course/tree/master/individual_challenges)

## Useful resources
* https://github.com/makersacademy/jobhunters/tree/master/pills/tech_tests
* https://airtable.com/shrpBfX9gP7pEiW9r/tblTo9xUR2Fdb1of6?blocks=hide
* https://www.chris-granger.com/2015/01/26/coding-is-not-the-new-literacy/ 

## Week's Goals

* Can you solve a challenging technical problem by writing well crafted code?
By "well crafted code", we mean code that is well tested, easy to read and easy to change.

### Have I achieved the above goals?

* Yes, in my team throughout the week, we used high-quality process to build our ['Acebook' project](https://github.com/Kaymo1990/acebook---CharliesAngels).

## Own Goals for the Week

1. Have a my process reviewed
a) With an official process review
b) By recording my screen and sending to a coach

2. Complete 2 tech tests
- Start by trying to solve the problem
- Then look at the form
- Then approve the code and repeat until you happy with the code quality. 


## Takeaways & Notes

### Week kick off
* The Feedback loop:

Receive F'back => reflect/plan => improvement

* Why is process important?
- helps to solve any problem
- employers will look at it
- a repeatable toolset
- gives you an approach to solving a problem

* Processes we have learned at Makers:
- TDD
- Debugging
- Self-led learning
- Pairing
- Working in teams (agile, communication)
- Refacting
- Modelling (inc. Domain Modelling)
- Organising work (inc. Version Control)
- Problem solving (which itself uses some of the above processes)

* Code Quality
- DRY
- SRP
- Readable
- Maintainable
- Has high test coverage
- Decoupling (for which you could use, for example, Dependancy injection for) 

N.B. Quality (in engineering terms) means solving user needs

- Why do you write code?
1. To solve user needs - does it work?
2. For your team/other developers - is it readable, understandable, maintainable?

* Naming conventions
- descriptive
- variable names should describe what data it holds. This should come from the domain (i.e. what we are trying to work with, the topic).

* Comments 
- Should not say HOW the code works.
- Instead of using comments, properly named variables, methods etc should do this for you. 
- However, a comment to say WHY the code was done a certain way is a valid comment (e.g. to explain that is sends error message due to an issue with an API) 

* Testing your code quality:
- Get someone else to read it. Maybe someone with less experience (in the junior cohort, maybe?).
- Is the code easy to change?
- Can I easily add a feature? If I have to add a feature, how much of the code do I need to change?


### Algorithm Design
* Algorithm is: A sequence of instructions that produces an output for a given input
* Not necessarily for a computer - could be for a maths equation or to solve a rubix cube
* Solves a problem
* Accepts different initial states???
* Repeatable:
- Given the same 'input', an algorithm should always give the 'same' output. 
* Examples:

#### Boiled food Recipe
* Inputs
- Food item
- Boiling time
- Tools (oven, pan, water, etc)
* Algorithm
- pour water in pan
- boil the water
- if food item = pasta: add salt
- insert food item into pan
- wait for (food time)
- Take food item out
* Output
- Boiled egg

* It is important to know the given input and desired output before deciding on algortihm

* Can have multiple inputs, e.g.
- "["Charlie", "Will", "Leo"] (persons to be split into groups and 2 (number of groups)
- Can have different outputs from this but solve the problem. i.e. Charlie could be put on his own, or Will or Leo. 

* Where there are multiple different outputs, ask the client what you want to happen in that instance

* When you are handling edge cases, only handle one at the time. i.e. ["Charlie", "Charlie"] and -2 (for no of groups) should be handled separately - once for the two Charlies, and another time for minus numbers. 

* Testing for edge cases: push each inputs to their limits, i.e. :
- limit of array as an input would be an empty array
- 0 the limit of an integer as an input

* Before writing an algorithm think about what inputs you expect and what outputs you expect, and any edge cases

* Planning a algorithm and thinking about possible inputs and outputs and edge cases makes it easier to write your tests.

#### Function Signature
* Name of the function
* Name of the parameters
* Types of each argument
* Types of output

* e.g. for a group divider:
- function name: equal_groups
- param_1 name: names
- param_1 type: string[]
- param_2 name: no_of_groups
- param_2 type: int
- output type: string[][]

* For pure functions use nouns for naming
* For non-pure functions (i.e. something that changes state) use a verb

#### Pure function
- No side effects
- It does not change state
- e.g. 
```
def add(a, b)
  a + b
end
```
- the above doesn't change state of anything at all

- the below example is not a pure function:
```
a = 6
def add(b)
  a = a + b
end
```
- The above changes something


* Q's to ask yourself when planning algorithm:
1. Can I do it on paper?
- No? Think about it.
- Yes? How to translate this into code.
-- Write it out in plain english
-- copy and paste it into the function and comment it out
-- translate into code line by line
-- if you cannot do in one line, split the line up into more lines again using plain english and comment out


### Tech Interview Lunchtime Talk
* Key when looking for companies - where can you optimise your learning
* Teach good practices
* Avoid small teams that are v busy (how they handled the interview process?)
* Fast-growing companies are a good option as you can grow with the company
* Look at this years or last years top start-ups and look at their CEO's backgrounds are
* Large agents with strong reputations (e.g. Deloitte Digital)
* Referels:
- Get to know someone in the company (they may get a fee for referring you)
- Go to meetups
- Network
* Even 'Anyone give me a referel for this company?" on social media
* Work on LinkedIn profile - developer experience
* Don't worry about what tech they say they require
* On LinkedIn, try and work out the management structure and find someone to message saying you are interested in working for them.
* Ask about what they do to encourage learning (pairing with seniors, tech talks, etc)

* If you are found by a sourcer, try and get to the actual recruiter. 

* First step after this is a non-technical phone screen. Sell yourself and ask questions. Don't worry about salary at that stage.
* Next is technical phone screen or tech test

* Some companies might put you with a pair for half a day. This is sign of a good co to work for.

* TECH CHALLENGE ROUND
* Strings and hash map v common in tech interviews
* Also some computer science concepts: stacks, queues...etc

* Most common 
- FizzBuzz
- Reverse a string
- Fibonacci numbers

* Know a bit about Big O Notation (how efficient an algorithm)

* If not enough time for TDDing or writing clean code then that's fine as long as you explain that to the interviewer. 
- "I would probably be writing a test for this..."
- "I would probably have named this function/variable better if I had more time..."

* If you are not sure how to solve the problem then maybe suggest to them a way to solve it and ask if you can google it or work it out with the interviewer.

* Ask at the start "What are your priorities? Do you want me to write tests?"

* Could start with writing something on a whiteboard and ask the interviewer "Does this look good?"

* SYSTEM DESIGN ROUND
- basic design on a white board to map out a system
- drawing the system - browser, server, database, etc
- load balancer
- relational databses, non-relational databases
- what happens when things fails
- how you scale things
- Look at Martin Fowler for the above
- Youtube (e.g. MIT) good for computer science basics

* BEHAVIOURAL ROUND
- Curiosity
- Self-improvement (always learning)
- Reflection (i.e. learning from mistakes - think of a time you messed up and what you learned from it)
- Conflict resolution 
- Difference between shipping product early with poor quality code and shipping later with better quality code



