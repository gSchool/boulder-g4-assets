## Class Notes, October 15th, 2014

(will be live-updated)

## Object-Oriented Programming

### Models

Structured representations of data
Models properties / attributes

MVC: Model, View, Controller

### UML Data Diagrams

4 concepts:

- Entity (aka model / object) - draw a box
- Object name in the top - nouns
- Attributes (fixed pieces of data) in the middle
- Methods (calculations) at the bottom
- Relationships drawn between

Attributes are stored in memory / Methods are calculated by the CPU

- "You're playing God" - Evan
- When modeling, you are "defining the cookie cutters" - Evan
- "We're looking at the _potential_ for things" - Turek
- "One size fits all" - Mello
- "One size fits all in that world" - Andy  (this is called a "Domain")
- "Like building legos - data model diagrams are the instruction book" - Turek

#### Drawing

- Draw a tall-ish rectangle in the middle
- Add the title with a line beneath
- Draw a line near the bottom for methods

- Draw other rectangles round the edges
- Draw lines with either crow's feet or "1 - infinity-sign"

Exercise:

* Person object
    * dob attribute
    * age, employers methods
    * has many employments
    * has many addresses
* Organization object
    * name attribute
    * employees method
    * has many employments
    * has many addresses
* Address object
    * city, state and zip attributes
    * geocode method
* Employment object
    * title attribute

### Analyzing Domains

- users can see the employment history for a person or organization
- users can see current employees of organizations, and current employers of people
- users should be able to record that an organization fired an employee
- users should be able to record that an organization laid off an employee
- users should be able to record that a person quit their job with an organization


### Ruby Classes

- Typically go in app/models
- Names are singular, start with a capital letter
- File names are lowercase, underscore names of the class

```ruby

# app/models/person.rb

# define a new Class
# like the outer rectangle w/ name
class Person

  # define some attributes
  # these are in the middle in UML
  attr_accessor :first_name, :last_name

  # define a method
  # this is at the bottom in UML
  def full_name
    "#{first_name} #{last_name}"
  end

end

```

Use `rails c` (or `rails console`) to play around.

```ruby

    my_peep = Person.new
    my_peep.first_name = "Jeff"
    my_peep.last_name = "Dean"
    my_peep.full_name  # <= "Jeff Dean"

```

### Controller / View Communication

```ruby

# in some controller, like app/controllers/pages_controller.rb

class PagesController < ApplicationController

  def index
    @jeff = Person.new
    @jeff.first_name = "Jeff"
    @jeff.last_name = "Dean"

    @peter = Person.new
    @peter.first_name = "Peter"
    @peter.last_name = "Klowes"
  end

end
```

```
# in the corresponding view, like app/views/pages/index.html.erb

<p>Hi <%= @jeff.full_name %>!</p>

<p>Hi <%= @peter.full_name %>!</p>
```

View the naming guide: https://github.com/gSchool/boulder-g4-assets/blob/master/cheat-sheets/rails-naming-guide.pdf


## Putting it all together

* Look at the wireframes
* Draw a simple UML diagram of what the class would look like
* Add the class to `app/models`
* Creates instances of those classes in the controller with `@variable_name` (the `@` symbol)
* Use those instances in the view

## Story Links

Refactor quotes:

1. Import stories: https://github.com/gSchool/boulder-g4-assets/blob/master/gCamp/0040-quotes/readme.md
2. Make the changes, commit, push to github, push to heroku and finish the stories in tracker

Add FAQ page:

1. FAQ wireframes and stories: https://github.com/gSchool/boulder-g4-assets/blob/master/gCamp/0050-faqs/readme.md


Here are all the whiteboard pictures from this morning: https://drive.google.com/drive/#folders/0B143NzKqlpeTMU12VHM5emdKTWc/0B143NzKqlpeTbG9RQ1IwTXlaUzQ
