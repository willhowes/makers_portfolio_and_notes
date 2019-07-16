# Week 4

### [Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-4)

## Week's Goals

1. Build a simple web app with a database
2. Follow an effective debugging process for database applications
3. Explain the basics of how databases work (e.g. tables, SQL, basic relationships)

More detail on the learning objectives of the [weekly challenge](https://github.com/makersacademy/course/blob/master/bookmark_manager) [here](https://github.com/makersacademy/course/blob/master/bookmark_manager/learning_objectives.md)

## How have I achieved my goals

### 1. Build a simple web app with a database
### 2. Follow an effective debugging process for database applications
### 3. Explain the basics of how databases work (e.g. tables, SQL, basic relationships)


## Daily Goals

### Tuesday
N.B. (Loïc and I got up to [step 6](https://github.com/makersacademy/course/blob/master/bookmark_manager/06_manipulating_table_data.md), i.e. completed 5).

1. Re-draft my blog post and send to Haylee - done.

2. Make a start on a practical to enhance learning about databases.

### Monday
1. Understand goals for the week and establish how I am going to achieve them.
* It was explained to us that the focus on this week is databases. This is going to be a tough week with a look of new things to learn but we are not expected to learn everything. 
* With this in mind I will take it in small steps and try to understand one or two things only per day. 

2. Have code reviewed and review someone elses code. 
* [My weekend challenge pull request](https://github.com/makersacademy/rps-challenge/pull/1343)
  * Received some helpful feedback - like reducing lines of code where possible, and have less actual code in VIEW files. 
* I reviewed [Kareem's weekend challenge](https://github.com/makersacademy/rps-challenge/pull/1345#pullrequestreview-261696717). I was able to read his code easily, give him feedback, praising him on what I though was good code and also made some suggestions of how it could have be improved.


## Takeaways/Notes
### Week kick-off
* Theme of the week is databases
* A lot to learn this week. There is a risk of feeling overwhelmed. Remember: you will not be able to learn everything and that is OK. 

### [Weekly challenge](https://github.com/makersacademy/course/blob/master/bookmark_manager/00_challenge_map.md)
* Learned how to make a new database using PostgreSQL and set up a table in a database.

### [Process Workshop](https://github.com/makersacademy/skills-workshops/tree/master/process_review)
* In a group of three. The other two first attempted the 'Middle letter' challenge while I monitored. 
* Learned that it is very important to follow proper TDD process.
* I also learned that, when monitoring, not to note down everything, just the points at which correct process not followed. 
* When I attempted the challenge I generally followed good TDD practice. However, I did perhaps rush a little a points, particularly by misnaming a method. If I had taken a bit longer over reading the instructions this could have been avoided. 
* It was generally very good practice to code in front of others with a bit of time pressure. Will definitely try to go to more of these workshops. 

### General database learning
* Every database as a DBMS (Database Management System) which structures how we organise and interact with our stored data. 
* CRUD - is the four fundamental way we interact with our data:
 * Create
 * Read
 * Update
 * Delete
* There are two main types of DBMS:
 1. Relational - highly structured and have strict data types. e.g. Oracle, MySQL, PostgreSQL, MicrosoftSQL
 2. Non-relational - more flexible, less strict on data types. e.g. mongoDB
 
 ### ERDs (Entity Relationship Diagrams)
 * [Useful video](https://www.youtube.com/watch?v=QpdhBUYk7Kk)
 * Examples of entities: Customer, Order, Product. 
 * Entities have attributes - e.g. customer_id, name, address
 * An ERD shows how the entities interract with each other. 
 * The relationship between them with lines which shows the 'cardinality' (e.g. 'one', 'many', 'zero or one', 'zero or many')
 


