# Week 6
[Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-6)

## Week's Goals

### Main goal for the week
By the end of the week all developers can build tested, easy-to-change software in a team using these processes:

* Break down projects into tasks and allocate them to pairs
* Build to a specificiation (rather than challenges)
* Run stand-ups and retrospectives
* Use a branch/PR/merge git workflow
* Give and receive meaningful code review

### High goals to refer to each day:
1. Can you use the XP values to guide your behaviour?
* Simplicity - small simple steps. 
* Communication - communicate face-to-face daily. Work together on all aspects of the project. Create solutions together.
* Feedback - Actionable, Specific and Kind
* Respect - everyone in team is equally valued and respect
* Courage - do not fear anything because no one works alone. Adapt changes, do not make excuses for failure.

2. Can you follow the full developer workflow? (Creating issues, branching, reviewing, squirrelling, merging.)
  * Try trello to progress goals or github issues
  * use branches and git pull requests. Don't push to master.
  * regular fetches from master branch if you are doing lots commits on your own branch.
  * Standups every morning and retrospective at least once a day but maybe twice (at lunch and end of the day).
  * Organise own retrospective on Friday

3. Can you keep code quality and test coverage high whilst building new features?

### Have I achieved the above goals?

Main goal (build tested, easy-to-change software in a team)

* Our team was effective in breaking the project down into firstly a very basic MVP, and then allocating small tasks to pairs. We achieved this my taking the time to plan the project, made a domain using and ERD (Entity Response Diagram) and a MDV model diagram. This helped us make two very simple user stories to start with and allocate these two stories into pairs. As the user stories were easy to fulfil we were able to achieve these by the end of the first day.  

1. XP Values:

 * Simplicity - this was effectively followed by using small simple steps when test driving building of the app. We started with a very basic MVP and built on this in small steps throughout the week. 
 
 * Communication - 
 
 * Feedback -
 
 * Respect - 
 
 * Courage - 

2. Can I follow the full developer workflow:
* I used ```github issues```, ```git branching```, ```git merging``` from the very first day. Git merging and resolving conflicts was effectively handled with team 'merge parties'.  


## Own Goals
1. excercise weaknesses from previous weeks, e.g. databases, user jquery.
* Achieved by:
 * Worked with databases throughout the week for the MakersBnB challenge. See notes below.

## Daily Goals

### Friday

### Thursday

### Wednesday

### Tuesday

1. Remember to do git fetches from master branch when making lots of commits on a separate branch. 

2. Reflect with Alice and my peer group how I am progressing and if I am recording my progress effectively. 

3. Have a look at Rake for setting up the databases automatically. 

### Monday
1. Understand week's goals

## Takeaways & Notes

### Databases
* On Monday we had a particular issue with setting up the datbases on each of our respective macbook. This could have been avoided by taking time to either:
 * Set up a Rake file so that exact replicas of the databases can be created easily by running the Rake file. 
 * Rather than trying to create a copy of the database in Table Plus, we could have run the SQL code in ```psql```. I spent a short amount of time looking for the correct psql commands but perhaps gave up too easily when it did not work.
 * Another lesson learned was that it is not a good idea rename the serial id columns. Having renamed the ```id``` columns in both the ```users``` and ```spaces``` table to ```user_id``` and ```space_id``` respectively, this caused an issue when one of us tried to reinstall the database on their macbook. It will also cause problems if someone want to clone and use our code on their own computer (as it would not let them create the tables to the databases with the serial ID columns called something other than ```ID```.
 
 ### MVP 
 * Think of it like, if your client is asking for you to build a car for the user to get between A and B quicker, do not start building the components of the car from the outset, try to build the simplest thing possible that can be presented to the client, and then work on the next simplest thing and so on. The steps could be:
 1. Build a skate board.
 2. Add a handle to make scooter
 3. Build a bike
 4. Build a motor-bike
 5. Build a car. 
 
