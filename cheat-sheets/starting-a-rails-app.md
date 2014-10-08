# Starting your Rails app

Follow these steps to decrease the chance of errors while learning Rails.

NOTE: Replace "my-app" with the name of your application.

## Create the app

1. Create the app with `rails new my-app`
1. Change your directory to the newly-created app with `cd my-app`
1. Open the app in your editor with `atom .`

## Start the server

1. `rails server` (or `rails s` for short)

## Get the homepage setup

1. Add your root route
1. Add your controller
1. Add the view folder, and the `.html.erb` view

## Adding Twitter Bootstrap

Follow the instructions [here](https://github.com/twbs/bootstrap-sass#a-ruby-on-rails).
This should include:

* Adding the gem to your Gemfile
* Renaming your `application.css` file to `application.css.scss`

Stop your server, run `bundle` and restart your server.

* Go to http://getbootstrap.com/getting-started/
* Go to the Jumbotron starter template, view the source and copy the html

In `app/views/layouts/application.html.erb`

* Paste the html into your `app/views/layouts/application.html.erb`
* Add back the `<%= stylesheet_link_tag 'application' %>`
* Add back the `<%= yield %>` line
