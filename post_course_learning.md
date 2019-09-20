# Post Course Learning

## TDD and BDD 
Watched [this video](https://www.youtube.com/watch?v=EZ05e7EMOLM&feature=youtu.be)
#### Takeaways:
- We should be testing methods but test a requirement. i.e. what is required of the code
- Sometimes easier to think of it as BDD - drive the code by testing the behaviour of the system
- The behaviour is the requirement - that is what you should be testing not the methods themselves
- Think of you program as a public facing API
- Refactor is the key part of RED-GREEN-REFACTOR
- Test behaviours not implementations

Running through the steps:

1. RED - write a test that doesn't work, and perhaps doesn't even compile at first

2. GREEN - make the test work quickly, commiting whatevers sins necessary in the process. 
- Copying and pasting code from stack overflow fine. 
- i.e. write code that satisfies the behaviour as quickly as possible.
- At this stage you are trying to understand the problem.
- Write sinful code!
- Not sure how to get to green - use a REPL
- Can try some other tests but delete these

3. REFACTOR - when we produce clean code
- Look for code smells. Is there a better way of doing this?
- Safe moves that changes the design of your code
- Still remain covered by your original tests
- Do not write new tests at this step
- e.g. if you are making a new class and extracting from old class - do not write new tests! unless you have realised there is a new bit of behaviour that needs testing
- Eliminate the dependancy between your tests and the code

#### Code smells
- Duplicated code 
- Long Method 
- Large Classs
- Long parameter list
- Switch Statements

### Mocking
- Don't use mocks to isolate classes. 

## Process Review
#### Initial Feedback

- Don't be afraid to take a while refactoring

- RED-GREEN should only take a minute or two - solve the quickest way possible

- Your quality coding is in the refactor stage

- Main issue is with syntax (i.e. understanding ruby better)

- To enable powerful refactors you need to understand the language you are using well

- when lots of ifs statements:
-- identify all the lines that are the same above any lines that are different. These can probably be refactored out
-- Likewise for lines that are the same below any lines that are different. 

- Repeated method calls, e.g. ```sum_as_string.split('')``` can probably be put into it's own variable and called upon where needed

- every time we add a new test there will usually be a new refactor that needs to be done
- If we don't regularly refactor then we have to do a long refactor
- During refactor, ask yourself: is there a better way to code this? Criticise your code - review it.


### Advice from Robert regarding what to do next after bootcamp:
- Have a look at Django framework for python (full stack, bit like rails)
- Java for back end ( a 'C type' language)
- Web - React, Angular, Django, Rails
- IoT - C languages
- Web - exploding! egs: MERN (react) - MEAN (angular)
- backend - python, java, C++
- data science may be of iterest
- BUT MAIN ADVICE: KEEP CODING! And yes do a project.

#### Videos and articles to look at:

- https://hackernoon.com/why-we-chose-angular-over-react-and-django-over-ruby-on-rails-for-atila-ca-77ac03d542cf
- https://blog.hyperiondev.com/index.php/2018/09/10/everything-need-know-mern-stack/
- https://blog.cloudboost.io/mean-and-mern-stacks-eb4cee991390
- https://www.youtube.com/watch?v=SzJ46YA_RaA&feature=youtu.be
- https://www.youtube.com/watch?v=ecIWPzGEbFc
