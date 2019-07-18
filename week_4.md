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

### Thursday 
1. Look into ORM to understand what it is. 
* Achieved by:
* Reading articles and watching videos. Can now explain what ORM is see [takeaways](https://github.com/willhowes/makers_portfolio_and_notes/blob/master/week_4.md#orm-object-relational-mapping)

2. Go through steps 11 and 12 of the bookmark manager challenge again. In order to consolidate my understanding of what we did yesterday.
* Did this and I now understand better how the MVC model interacts with databases.

### Wednesday
1. Go through yesterday's steps (6-10) on the weekly challenge, to reinforce my understanding of databases.
 * Acheieved by going through these steps. It helped to understand how our program interracted with the database.

2. Further my understanding my understanding of databases by going through some more course materials. 
 * Achieved by:
  * Used [CRC (Class-Responsibilty-Collaborator)](http://www.agilemodeling.com/artifacts/crcModel.htm) to further my understanding of how to model a domain that uses a database. 
   * Class - describe the class
   * Responsibilty - what responsiblities does that class have?
   * Collaborator - what other classes does this class communicate with

### Tuesday
N.B. (Loïc and I got up to [step 6](https://github.com/makersacademy/course/blob/master/bookmark_manager/06_manipulating_table_data.md), i.e. completed 5).

1. Re-draft my blog post and send to Haylee.
 * Achieved by:
  * Redrafted, sent to Haylee, and eventually added to the Makers blog.

2. Make a start on a practical to enhance learning about databases.
* Achieved by:
 * Learning about ERD (Entity Relationship Diagrams) and attempted a few diagrams of my own. See [takeaways below](https://github.com/willhowes/makers_portfolio_and_notes/blob/master/week_4.md#takeawaysnotes)

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
* When I attempted the challenge I generally followed good TDD practice. However, I did perhaps rush a little a points, particularly by misnaming a method. If I had taken a bit longer over reading the instructions this could have been avoided. I also should have taken a little more time setting up my environment, e.g. putting the spec file on one side of the view and the code on the other side. 
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
 * When developing a web app with a database, if you have a 'test' environment set up, with a test database (which should be an exact replica of the production database, save that it will be empty), then you will not need to mock or double the test database in your unit or feature tests.
 
 ### ERDs (Entity Relationship Diagrams)
 * [Practical](https://github.com/makersacademy/skills-workshops/blob/master/practicals/databases/entity_relationship_diagrams.md)
 * [Useful video](https://www.youtube.com/watch?v=QpdhBUYk7Kk)
 * Examples of entities: Customer, Order, Product. 
 * Entities have attributes - e.g. customer_id, name, address
 * An ERD shows how the entities interract with each other. 
 * The relationship between them with lines which shows the 'cardinality' (e.g. 'one', 'many', 'zero to one', 'zero to many')
 * I can now draw basic ERDs, e.g. [one for twitter](https://www.lucidchart.com/invitations/accept/c700895e-bd79-4410-8916-1eb441e97449) 
 
 ### Development environments
 * A web project will usuall have three (or more) environments: 
 1. Development
 2. Test 
 3. Production
 * Since the behaviour of the project will be very different depending on what environment it is in, you would want separate databases for each environment.
 * For example, if you had a million users on your website, you would not want to use the main database for testing or development. When in development, you would want to use a database with just a few users. When testing you would want to use a blank database as you will want the database to presume that there is nothing there that was not created explicitly. 

### General
* use cmd-d to change all variables with the same name.

### CRC (Class-Resonsibility-Collaborator)
* It is a way to model a domain.
* [Example](https://github.com/makersacademy/skills-workshops/blob/master/week-4/databases_2/crc_example.md)

### Databases Q&A (Weds)
* A relational databases are in table format with columns and rows (or x and y co-ordinates).
* Main thing for us to learn how to query databases. Unless you want to become a database engineer or database architect.
* SQL is a language but has one sole purpose - querying databases. 
* Will need an escape an inverted comma with another inverted comma. e.g. ```'O''Hara'```.
* An ORM would normally handle where you need escape characters. An ORM handles your SQL queries so you don't have to manually type them. 
* When you use ```Date.now``` on the Chitter challenge, this will be stored in the database as a 'timestamp'.
* When in a session in your controller all that data is stored in the browser.

### ORM (Object-relational Mapping)
* I can explain that this is a technique whereby data which is non-comptable between a relational databases and OOP languages is converted and wrapped in an object that can be read by the OOP language.

### CRUD 
* A CRUD applications is one that CREATES, READS, UPDATES, and DELETES data. Most Web Apps are CRUDs.
* CRUD are the four basic functions of persistent data.

### RESTful routing conventions
* Representational State Transfer
* It is a set of conventions so http request follow a similar format. The idea is that you have a one 'resource' or 'noun' (usually the web page) and verbs, i.e. GET/POST/PATCH/DELETE. These conform with CRUB:
* CREATE - POST 
* READ - GET
* UPDATE - PATCH
* DELETE - DELETE

### Four-phase testing - SETUP/EXERCISE/VERIFY/TEARDOWN
 * SETUP - set up the test, e.g:
 ```
 visit('/bookmarks/new')
 fill_in('url', with: 'www.bbc.co.uk')
 fill_in('title', with: 'BBC')
 ```   
 * EXERCISE - carry out the method/function we are testing. e.g:
 ```
 click_button 'Submit'
 ```
 * VERIFY - check the result of the exercise meets our expectations. e.g:
 ```
 expect(page).to have_link('BBC', href: 'www.bbc.co.uk') 
```
 * TEAR DOWN - system under test is reset to its pre-setup state. This is usually handled implicitly by the database or program. In the example of the bookmarks_manager, we do this in the ```set_up_database``` helper file:
 ```
connection.exec("TRUNCATE bookmarks;")
```
 

