# Class Notes, October 17th, 2014

## Personal Projects

Personal project

**Create a Pivotal Tracker project**

* Name it whatever you like.
* Make sure it's in the gCamp account
* Do NOT make it public
* Invite the following members as owners:
    * jeff@galvanize.it
    * emily@galvanize.it
    * aaron@galvanize.it
    * luke@galvanize.it

Add some tracker stories.  Here are some you can start with:

```
Current State,Estimate,Type,Title
unstarted,1,chore,invite instructors as project members
unstarted,1,chore,create rails app locally
unstarted,1,chore,install twitter bootstrap
unstarted,1,feature,users should be able to see a simple homepage with my personal info
unstarted,1,feature,users who visit your github repo should see a nice looking readme with a heroku url
```

**Create a rails app locally**


NOTE: replace `my-app` with the name of your app

```
cd ~/workspace
rails new my-app --database postgresql
cd my-app
```

Here's [the Rails guide](http://guides.rubyonrails.org/getting_started.html) with more info about getting started.

**Add twitter bootstrap**

From within your new rails app directory, rename `app/assets/stylesheets/application.css` to `app/assets/stylesheets/application.css.scss`

From the command line, this line should work:

```
mv app/assets/stylesheets/application.css app/assets/stylesheets/application.css.scss
```

https://github.com/twbs/bootstrap-sass#a-ruby-on-rails

Instead of copying the entire bootstrap template, try just adding one component
at a time.

**Add a readme**

Rails generated a README.rdoc file for you.

* `mv README.rdoc README.md`
* Delete everything in it
* Add useful content

Markdown syntax: http://daringfireball.net/projects/markdown/syntax

**Add a simple homepage**

* Add a route like `root "pages#index"`
* Add a controller
* Add a view

**Configure your application layout**

* Add a footer that has "created by <your name>", a link to your linkedin profile and / or other personal website

If you want standard twitter bootstrap goodness, I suggest:

```
<div class="navbar">
  <div class="container">
    <!-- navbar here -->
  </div>
</div>
<div class="container">
  <%= yield %>
</div>
<footer>
  <div class="container">
    <!-- footer stuff here -->
  </div>
</footer>
```

**Get it in git**

On Github.com

* Create project (make it public)

Locally, from your rails directory

```
git init
git remote add origin <your github ssh url>
```

Whenever you are ready, commit and push.

**Deploy it to heroku**

Add the following to your `Gemfile`:

```ruby
gem 'rails_12factor', group: :production
```

Then run:

```
bundle
git add -A
git commit -m "added rails_12factor gem for Heroku"
heroku apps:create
git push heroku master
heroku open
```

To add a name, see https://devcenter.heroku.com/articles/creating-apps#creating-a-named-app - like `heroku apps:create my-special-name`

NOTE: you should _not_ have an sqlite gem anywhere in your app

**Tell us about your project!**

* Go to https://students.gschool.it/cohorts/3/personal_project
* Paste in your full tracker URL (starting with `http`)
* Paste in your full github URL (starting with `http`)
* Paste in your full Heroku URL (starting with `http`)

**Run at the same time as gCamp**

`rails s -p 3001`
