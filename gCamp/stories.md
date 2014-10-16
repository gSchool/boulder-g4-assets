# Stories

- Lesson: Views / rendering (apply)
- Produce: getting started guide
- Produce: git repo with gCamp mocks / stories

- In-progress
- Lesson: View rendering (memory, info from route / games / quiz)
- Produce: Markup and instructions for students to use
- Story: User views home page / launch page w/ image
- Extra: user views fancier content + grid
- Extra: Named view and explicit render in controller

## Git

- Lesson: Git and Github (apply)
- Lesson: Git and Github (understand)
- Story: create and push gCamp repo (using git add -A)
- Extra: git add individual files / -p / -N etc...
- Extra: git book / docs
- Lesson: Terminal / bash (apply - command line the hard way)
- Lesson: Command line memory game

## Heroku

- Lesson: Heroku (understand and apply
- Lesson: Gemfile / fails_12factor
- Story: deploy gCamp (w/ Custom name)
- Extra: Git remote stuff
- Extra: custom url
- Lesson: dev workflow typography (sequence diagrams)

## Routes / link_to

- Produce: Naming cheat sheet
- Lesson: Understand routes / link_to
- Lesson: Apply Routes / link_to
- Story: User can view about page and terms - links in the footer
- Produce: html for pages (whole body)
- Extra: header image linked (link_to do)
- Extra: separate out into different controllers
- Extra: moar pages

## Layouts

- Lesson: layouts / understanding / analysis / application
- Story: convert gCamp to layouts
- Extra: set page title from view / either with instance variables and content_for
- Extra: set layout name / custom layouts per action

## Layouts

- Lesson: view rendering review
- Lesson: view rendering advanced review
- Lesson: gSchool FRESH
- Assessment (song that doesn't end?)

## Instance variables (quotes)

- Lesson: controller / view communication w/ instance variables
- Lesson: arrays / each
- Story: add dynamic quotes
- Extra: arrays of arrays, the authors are separate from the quotes
- Extra: sort, sort by author name
- Extra: limiting, random quotes
- Extra: two columns of quotes (partition)
- Extra: blockquote / footer

## Instance variables (faq)

- Lesson: ruby classes / properties
- Story: refactor quotes to classes / user can view dates and author separately on quotes
- Extra: add initializer to class

## Testing

## CRUD

- Lesson: Understand crud
- Lesson: understand intro to db models
- Story: users can crud tasks (w/ scaffold)

## Ruby

- Lesson: ruby methods
- Lesson: intro to hashes
- Story: tweak task form to look like bootstrap (needs design)
- Extra: rewrite with parens / curlies
- Extra: bootstrap all the things

## Hand-rolled CRUD

**new / create**

- Lesson: apply new / create
- Lesson: Rails models apply (rails g model)
- Lesson: form_for (remember syntax, know that it's for putting things in the server - link_to gets things)
- Story: users can create and see all users
- Extra: formtastic

**show / edit / update**

- Lesson: Apply show / edit / update
- Story: User can edit / show update users
- Lesson: partials
- Story: users can refactor to partials

**destroy**

- Apply: Destroy
- Story: users can destroy users
- Extra: link_to method :delete confirm: true

## Associations

- Lesson: Associations / belongs_to
- Lesson: Collection select
- Story: user can assign task to specific user
- Extra:

## CRUD

- Story: user can CRUD projects
- Assess:
- Extra:

## ActionMailer

- Lesson: ActionMailer SendGrid
- Story: Users are emailed when tasks are assigned to them
- Extra: Background job

## Nested resources

- Lesson: Nested routes
- Story: users see tasks scoped by project
- Story: user can view project dashboard

## OAuth

- Lesson: oauth
- Lesson: env variables
- Lesson: omniauth w/ github
- Story: users can log in / log out
- Extra: has_secure_password

## API integration

- Story: users can see github data on project page
- Extra: projects have memberships

# Other ideas

Flow:

* Tasks
* Task lists
* Users
* Login / Signup
* Projects
* Memberships and roles
* Cancellation
* Public site

Basic dashboard

* View rendering
* Maybe image_tag
* Bootstrap
* some routes

CRUD tasks

* resources in routes
* bootstrap
* params
* instance variables
* rendering
* form_for, link_to, models, controllers, views
* flash messages
* validations
* migrations
* deployment
* erb
* immediately add totals dashboard
* some testing?

Enhance tasks

* More data types
* Due dates
* ruby methods (past_due?)
* more validations
* View helpers (time_ago_in_words)

CRUD task lists

* non-trivial migrations
* associations (has_many)
* partials
* nested routes

CRUD projects

* Associations (task lists belongs_to projects)
* nested routes
* resources

Manage project members

* has_many :through
* enum / picklist
* nested routes
* select / collection select

Login / Logout

* sessions
* cookies (remember me)
* BCrypt
* before filters
* permissions
* custom validations
* helper_method / view helpers
* deep dive could be dsl in helper method

Comment on tasks

* associations
* partials
* nested routes
* text_field
* view helpers (simple_format)
* extra can be markdown / caching rendered html

User profiles

* bootstrap
* associations

Notifications

* API integration (consumer of Twilio)
* String parsing
* View helpers (linking @mentions to those users)
* Email
* env variables
* in-app notifications / update_all / concept of being "read"

CRUD documents

* carrierwave
* s3
* environment variables

Comment on documents

* polymorphism
* recursion
* partials

Task Assignment

* collection_select
* associations
* link_to

Filter tasks

* custom sql / has_many :through / enumerable methods
* scopes / custom finders / chaining

Dashboard

* AR.count
* SQL?
* Complex controller <- good controller spec?
* Lots of queries / instance variables (all their notifications / mentions)

Activity feed

* Modularity
* Service objects / observers
* Polymorphism (concept, maybe even implementation)
* Dependent :destroy

Search

* either postgres or elastic search

Signup / account creation

* Controller / model separation
* DRY in controllers (sign_in)

API serving

* headers
* JSON

Cancellation

* dependent destroy
* background jobs (probably an extra task)

Export

* CSV
* Background jobs (probably an extra task)

Admin

* Multiple roles
* Reporting / analytics
* Google charts

Marketing site

* controller inheritance
* custom css

Some report that happens nightly

* cron
* rake

Project page

* Conditionals (empty?  present?)
* Somewhat non-standard flow of forms
* Validations that post render a page from a different controller
* Random quotes (rand sample)

String parse a quick-add task

* "do some thing by 4pm tomorrow"
* "@joe must ..."
* string parsing - real code within a rails app

SendGrid email into the app

* Request specs

# Javascript

Inline task completion

* dom class changes / hide show
* respond_with / respond_to
* event listeners

Inline task deletion

* dom removal
* respond_to
* event listeners

Inline task creation

* dom addition
* callbacks
* form clearing
* show hide
* really knowing ids and classes so ids are not duplicated
* ruby api

Inline task editing

* Templating system
* dom replacement
* ruby api
* js models

Auto flash message

* like flash, but in js

Filtering

* show / hide tasks that are complete

Sorting

* jquery
* plugins
* drag / drop terminology
* fontawesome / glyphs

Auto task population (live updates)

* polling / pusher
* reactive programming

Auto-complete of @ mentions

* wysiwyg editors (contenteditable)
* maybe a plugin, maybe we write it?
