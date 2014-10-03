# Starting your Rails app

Follow these steps to decrease the chance of errors while learning Rails.

NOTE: Replace "my-app" with the name of your application.

1. Create the app with `rails new my-app --skip-spring --database postgresql`
1. Change your directory to the newly-created app with `cd my-app`
1. Open the app in your editor with `atom .`
1. Remove `gem "turbolinks"` from your Gemfile
1. Remove `//= require turbolinks` from application.js
1. Search for "data-turbolinks-track" attributes in your layouts and remove them
1. Run `bundle`

## Adding Twitter Bootstrap

Follow the instructions here: https://github.com/twbs/bootstrap-sass#a-ruby-on-rails

## Preparing to deploy to Heroku

Follow the instructions here: https://github.com/heroku/rails_12factor#install
