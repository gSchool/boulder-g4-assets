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
- 


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

### Controller / View Communication
