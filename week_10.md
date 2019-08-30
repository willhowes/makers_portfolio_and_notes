
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

3. Watch this about Hash mapping


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


### Process Review - initial feedback

First test a bit too complex - too large of an array (should start with one item in array)

Second test dealt with both limits - should have been just one limit to start with.

Then would have been good to test for two items in the array - with just one limit.

Then test for the other limit. Then test for both limits. 

Could have written a test for the refactor - i.e. test more than one frequency.

When refactoring, rather than commenting out the old code, build on it using conditionals.

### Tech Interviews Workshop
#### To START doing:
* Take time to clarify problems (and clarify any questions asked)
* Blogging
* Think about good communication (talk out loud)
* Explained core concepts
* If you don't know the answer, be honest, say "I don't know, but..." and explain what you would do to find out the answer
* Big picture about software development
* Do your technical research
* Apply for jobs you are exited about (so that you have good energy at the interview - you are enthusiastic about working there)
* Open posture 
* Research into company's culture
* After Makers, pick one language and get really good at it

#### To STOP doing:
* Firing off things that you've heard about but you do not actually understand (e.g. "REACT is really hot right now...")
* Don't over power your pair and vice-versa.
* Slow down, don't panic.

#### Leo's Interview notes
* Got a bit lost explaining DRY. Remembered towards end.
* Good at taking time and repeating the question
* Although did not state a tech excited about, explained why.
* Enthusiastic about problem solving.
* Perhaps got a little bit lost when describing what found difficult about programming.

What are you learning from your interviewee about good practice?
- OK to take time.
- Try and keep in mind the original question if you get diverted.
Where are you getting lost or drifting off in their answers?
- When long examples are given. 
- It is risky to use s metaphor unless you have used it before perhaps.
Where are you really engaged in the answer? What’s happening?
- Being very specific and concise in your answer.

### Hash Tables and Hash functions (or Hashes v Arrays) 
https://www.youtube.com/watch?v=KyUTuwz_b7Q

#### Summary
* Hash tables are used to index large amounts of data
* Address of each key calculated using the key itself
* Collisions resolved with open or closed addressing 
* Hasing is widely used in database indexing, compilers, caching, password authentication, and more. 
* Insertion, deletion and retrieval occur in 'constant time' but only if there are no collisions.

* With an array, to search for a item in the array there are two posibilities:
1. Iterate over the whole array - this can take a very long time if it is a large array.
2. Find the item by index which is v quick.

* What you can do with arrays is use a formula to decide at what index position an item should go in the array. This can be:
```
index = sum ASCII codes % size of the array
```
i.e. sum up the ASCII codes for each character of the array item, for example:
Tim would T = 84; i = 105, m = 109 total = 279 % size of the array (e.g. 10) = 4 (so we put item 'Tim' in item 4 of the array).

* That key (i.e. 4 for 'Tim') could just be one of many attributes of an object stored in the array.

* A Hash table of key-value pairs is sometimes known as a hash map.

* A Hashing Algorithm or Hash Function
- Calculation applied to a key to transform it into a memory address
- For numeric keys, you would divide the sum of ASCII codes in a key by the number of available addresses, n, and take the remainder. i.e. ```address = key Mod n```
- For aplhanumeric keys, divide the sum of ASCII codes in a key by the number of available addresses, n, and take the remainder (this is what we did with the 'Tim' example below).
- Another method is the 'folding method'. e.g. a tel number could be some of each pair of digits. 

* Collisions 
- Sometimes you might apply a hash function to two different keys and get the same index number. This is known as a collision. 
- There are two methods for resolving collisions 

#### Opening Addressing
- This uses 'liner probing' to find the next available index position in the array. To avoid items bunching together, you could use 'plus 3 rehash' which looks at every third position to see if it is available. 
- How do you find the index if there have been collisions? You would need to use linear searching (i.e. iterate over the array from the index position it should have been in until you find it. And so, if 'Tim' should have been in index position 5 but that slot was taken then you would have to iterate over the other items items from position 5 until you find 'Tim'.
- To help avoid this you could make the size of the array bigger than the number of items to be stored. You may, for example, have 70 items but have an array size of 100 so there is extra space to help avoid collisions. This is know as the 'load factor'
```
Load Factor = Total no of items stored / size of array
```
- You could adjust the size of the array using the load factor as the number of items to be stored increases.

#### Closed Addressing
- AKA 'chaining'. Here the index position points to the first 'node' of a linked list which can have more than one item in. So, say items 'Tim' and 'Sue' index position (given by the hash function) should be 4, by using 'chaining' both these items could be in the linked list at index 4. 
- The look up here is *usually* quicker than 'linear probing'

### Week 10 Retro
* 'Brilliant' is a good computer science app
* Scrum.org for explanation of scrum teams. 

#### SWOT analysis on your process
##### Strengths
- Improving naming of methods/variables
- READMEs

##### Weaknesses
- Class extraction
- Refactoring

##### Opportunities
- Pairing
- Good for Github CV- N.B. V Important to forcus on process (TDD in particular). 
- Having fun
- Learning technologies and learning from each other

##### Threats
- Poor team work and communication
- Taking too long to agree on project direction


#### Final projects
- Important to remember - the project is abstract but the people in your team are real. 
- Distracted by job hunting
- Make sure commits are even
- Get in early Monday morning. 
- Should still make time for own work. 
- Can co-author commits. 
