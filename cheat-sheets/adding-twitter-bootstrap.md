## Adding Twitter Bootstrap to a Rails App

### 1 - install it
Follow the instructions [here](https://github.com/twbs/bootstrap-sass#a-ruby-on-rails).
This should include:

* Adding the gem to your Gemfile
* Renaming your `application.css` file to `application.css.scss`
* Copying the `@import` lines into your `application.css.scss`
* Copying the specified line into `application.js`

### 2 - load it into your server

Stop your server, run `bundle` and restart your server.

### 3 - copy the html in

* Go to http://getbootstrap.com/getting-started/
* Go to the Jumbotron starter template, view the source and copy the html

In `app/views/layouts/application.html.erb`

* Paste the html into your `app/views/layouts/application.html.erb`
* Add back the `<%= stylesheet_link_tag 'application' %>` to the head of the html doc
* Add back the `<%= yield %>` line somewhere in the body
