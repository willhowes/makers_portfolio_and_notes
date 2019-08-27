# Weeks 8 & 9
[Week outline](https://github.com/makersacademy/course/blob/master/week_outlines.md/#week-8-9)

Resources for the Project:
* [Project criteria](https://github.com/makersacademy/course/blob/master/final_projects/project_criteria.md)
* [Engineering Projects Guide](https://github.com/makersacademy/course/tree/master/engineering_projects)
* [Rails Engineering Project](https://github.com/makersacademy/course/tree/master/engineering_projects/rails)
* [Two day sprints](https://github.com/makersacademy/acebook-rails-template/blob/master/CONTRIBUTING.md) 

## Week's Goals

* Can you use high-quality processes to build a project in a team?


### Have I achieved the above goals?

* Yes, in my team throughout the week, we used high-quality process to build our ['Acebook' project](https://github.com/Kaymo1990/acebook---CharliesAngels).

## Own Goals for the Week

1. Have a my process reviewed
* Attended a process review on the Wednesday of week 9.

2. Get an understanding of rails
* Achieved by:
- A lot of research and following tutorials.
- In our group project we built [a copy of Facebook](https://github.com/Kaymo1990/acebook---CharliesAngels)
- Working on my own, I built a copy of Instagram (['Instadamn'](https://github.com/willhowes/instagram-challenge))

## Takeaways & Notes

### Week kick off
* What does high-quality processes mean:
- Standups/Retros
- TDD
- XP Values
- Agile
- Planning
- Git workflow
- Pairing

* N.B. Standups are not the same as planning.
- Standups: what you did yesterday? what your goals for the day? Mood check-ins.

* These two weeks are all about the process.

* Rota for planning session?

* Use Trello for managing workflow.

### General Notes on Rails
* Overview guide for a basic app: https://guides.rubyonrails.org/
* In-depth book for building a more complex app: https://www.railstutorial.org/book/

* Rails uses the MVC patter.

* The Controller part is referred to as the 'ActiveController'
* The Model part is referred to at the 'ActiveRecord'
* The View is referred to as the 'ActionView'
* ```config``` configures the routes to send you to the correct controller.

* in erb files use ```<%= some_ruby_code %>``` if we are outputting something or ```<% some_ruby_code %>``` if no output is being rendered. Use ```<%# some_ruby_comment %>``` for commenting.

* In terms of having a class in Rails, when you set up the model, the class's attributes are determined by the rows that are in that class's databases. 

* To set the routes you need to generate a controller for that model, e.g. ```rails generate controller Posts```. This will create a controller class for this model that inherits from the ApplicationController. In this new class you need to define the CRUD routes, e.g:
```
def show
end

def new
end

def create
end

def edit 
end

def destroy
end
```
The ```new``` method will be called when you hit the submit button on the new posts form and rails takes you to the path ```app/views/articles/new.html.erb```.

* Example of how to create a one to many relationship (comments on a blog post):
https://guides.rubyonrails.org/getting_started.html#adding-a-second-model

* When you create a form you use a form builder with the ```form_for``` method followed by the model the form is for, e.g. ```@post```. To see where the form goes to you can inspect the submit button on the html use the command ```rails routes``` .

* Rails has ```has_many``` and ```belongs_to``` methods for setting up databases to have many-to-one or many-to-many relationsips. 

* To set up a model with a relationship (like a post being related to a user), when you generate the model you use the `reference` keyword, e.g:
```
$ rails generate model Micropost content:text user:references
```
- the above automatically gets the user_id from the users table of the database, so each post has a foreign key being the user_id of the user that made the post. 

* For example, with apps like Twitter or Facebook, the posts model would say it belongs_to the User class:
```
class Micropost < ApplicationRecord
   belongs_to :user
end
```

* The ```resources``` method makes the resource (or object) CRUD.

### Careers workshop
* Process about persuading an employer to give you an interview more important than your CV.
- LinkedIn, twitter, events, etc. Find a company you want to work for...
- Still have to have a CV though...
* If there's a company you really want to work for then let careers team know.

### Week 8 Retro
* Do a process workshop, record it and send to coach.
* Can set 'pessimistic' 'moderate' and 'optimistic' time estimations. 
* Group work:
- Designated leader each day
- Feedback sessions? (if all happy for this)

### Initial Feedback from the Process Review (with Robert)
* A few syntax issues
* I coded before testing towards the end with the edgecases, although I noticed that I was doing it and went back to testing. 

* RED-GREEN-REFACTORING - my red-green was good. Refactor was not so good. I should refactor more as I go along. I should look for repetitions (anything that's going over and over again). The basics programming principals will always help: i.e. variables, loops, if statements, methods.

* Lots of ifs might be better than ifs and elsifs. What you need to ask yourself is - do I want all the below ifs to be ignored if this if is true (if so, just use if statements) - or, do all the statements need to be checked (if so, then you need elsifs).

* Naming conventions - "hash", "string", for example NOT GOOD. Can rename them during the REFACTOR stage. During the GREEN stage you can make as many coding sins as you want (naming conventions, loads of if statements), but you should correct these during the REFACTOR process. Keep running the tests when you are refactoring to make sure it is staying green - do it in small increments.

* Dealing with edgecases at the end was good practice. 

### Thursday Cohort Retrospective
* Migrations files are like git commits. Allow you to rollback to a certain point. 
* path_urls are helpful because these are variables that you can change. For example, you could change ```post_path_url``` to go to a different route and this will change everywhere this variable is called. 
* Framework are used in the real world and it is helpful to get used to this. Useful to get used to reading framework documentation. 
* Good to get used to not starting a project from scratch - will rarely do this in the real world. 
* In rails you should test controllers. 
* If you only feature test then you will not know where the fail is, as the database, model, controller, views are all being checked. 
* Features tests are to test the user stories, unit tests are testing that your code is solid and well-written.
* Should test-drive when you are implementing features, e.g:
   - write the feature test first
   - will fail because button does not exist, for example. 
   - then build the html so there is a button, and progress from there...

### Rock Your Tech CV Workshop
* Github CV first thing employer looks at (Makers hiring partners, anyway)
* Talk about yourself and past experience
* Github CV a bit like a covering letter and CV in one
* What you have done before Makers also important
* Also have a separate one page CV

* PROFILE SECTION
- About one paragraph
- You are a software developer now, not a trainee. Make that clear. 
- What you love about coding
- Focus on love of programming, not why you left previous job.
- Put link to blog

* PROJECT LIST
- of 3-5 projects. 
- make sure the READMEs are good

* Don't need to describe or sell Makers

* Only clean-ups READMEs of your main repositories (i.e. the 3-5 featured ones), not all your old ones

* SKILLS
- Previous skills that is relevant to tech

* EDUCATION
- Just mention degree, don't go back to A-levels. 

* HOBBIES
- mention music

* Infer your skills through example, i.e. not something like 'I have strong leadership skills' but 'When I was at school I led...'

* Despite the above guidelines, don't be afraid to break the rules. 

* Maybe build your own website as a project after Makers. 

* JOBS APPLICATIONS GENERALLY
- If you are missing a bit of experience then apply but get in touch with someone who works in that team.

* In general use some images and creativity



### Week 10
* This will be about getting job-ready.
* Clean up git hub. Look at good example, lose the bad examples. Improve on the good ones. 
* This weekend do more instagram and improve online presence - get on stackoverflow. 
