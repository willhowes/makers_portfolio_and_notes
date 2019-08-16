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

## Own Goals for the Week

1. Have a my process reviewed

2. Get an understanding of rails

3. Have a look at Big O Notation. 

## Takeaways & Notes

### Week kick off
* What doesn high-quality processes mean:
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
* More details book building a more complex app: https://www.railstutorial.org/book/
* It uses the MVC patter.

* The Controller part is referred to as the 'ActiveController'
* The Model part is referred to at the 'ActiveRecord'
* The View is referred to as the 'ActionView'
* ```config``` configures the routes to send you to the correct controller.

* in erb files use ```<%= some_ruby_code %>``` if we are outputting something or ```<% some_ruby_code %>``` if no output is being rendered. Use ```<%# some_ruby_comment %>``` for commenting.

* In terms of having a class in Rails, when you set up the model, the class's attributes are determined by the rows that are in that class's databases. For example, if you have set up a ```User``` model 

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
The ```new``` method will be called when you hit the submit button on the new posts form and rails take you to the path ```app/views/articles/new.html.erb```.

* Example of how to create a one to many relationship (comments on a blog post):
https://guides.rubyonrails.org/getting_started.html#adding-a-second-model

* When you create a form you use a form builder with the ```form_for``` method followed by the model the form is for, e.g. ```@post```. To see where the form goes to you can inspect the submit button on the html use the command ```rails routes``` . If the form 

* Rails has ```has_many``` and ```belongs_to``` methods for setting up databases to have many-to-one or many-to-many relationsips. 

* To set up a model with a relationship (like a post being related to a user), when you generate the model you use the `reference` keyword, e.g:
```
$ rails generate model Micropost content:text user:references
```
- the above automatically gets the user_id from the users table of the database, so each post has a foreign key bring the user_id of the user that made the post. 

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
* Can set 'pessimistic' 'moderate' and 'optimistic' time estimations. 
* Do a process workshop, record it and send to coach.
* Group work:
- Designated leader each day
- Feedback sessions? (if all happy for this)
