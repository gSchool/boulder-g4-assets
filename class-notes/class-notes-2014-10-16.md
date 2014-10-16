## Class Notes, October 16th, 2014

(will be live-updated)

### Git

Create a new git directory:

```
cd ~/workspace/
git init branching-demo
cd branching-demo
atom .
```

Add some files, commit and change

Create a branch:

```
git checkout -b my-new-branch-name
```

Make changes and commit.

See a fancy log

```
git log --oneline --all --decorate --graph
```

Switch branches:

```
git checkout my-new-branch
git checkout master
```

Merge branches:

```
git checkout master
git merge my-new-branch
```

Delete a branch that's already been merged:

```
git branch -d my-new-branch
```

View branches:

```
git branch -a
```

Great talk about git internals: https://www.youtube.com/watch?v=1ffBJ4sVUb4 (long and awesome)

### Interpreting Wireframes

* Avoid comic fonts
* Avoid adding your own borders / background colors (we removed black from the wires)

### Rails CRUD

Finish https://students.gschool.it/cohorts/3/exercises/139

- **C**reate
- **R**ead
- **U**pdate
- **D**elete

Steps are:

* run the `rails generate scaffold` command
* run migrations
* commit and push
* after you push to heroku, you need to `heroku run rake db:migrate`

**Steps to running a scaffold**

If you were generating a model for a Car with a make, model and year:

```
rails g scaffold car make:string model:string year:integer
```

Then run:

```
rake db:migrate
```

To see it in action, go to `http://localhost:3000/cars`

Then after committing and pushing to Github:

```
git push heroku master
heroku run rake db:migrate
```

### gCamp Stories

Basic CRUD

* [MVP Wires](https://github.com/gSchool/boulder-g4-assets/tree/master/gCamp/0060-task-with-scaffold)
* [MVP Stories](https://raw.githubusercontent.com/gSchool/boulder-g4-assets/master/gCamp/0060-task-with-scaffold/mvp.csv)
* [Stretch Wires](https://github.com/gSchool/boulder-g4-assets/blob/master/gCamp/0060-task-with-scaffold/stretch.md)
* [Stretch Stories](https://raw.githubusercontent.com/gSchool/boulder-g4-assets/master/gCamp/0060-task-with-scaffold/stretch.csv)

Bootstrapify the views

* [MVP Wireframes](https://github.com/gSchool/boulder-g4-assets/tree/master/gCamp/0070-twitter-bootstrap-tasks)
* [MVP Stories](https://raw.githubusercontent.com/gSchool/boulder-g4-assets/master/gCamp/0070-twitter-bootstrap-tasks/mvp.csv)
* [Stretch Wireframes](https://github.com/gSchool/boulder-g4-assets/tree/master/gCamp/0070-twitter-bootstrap-tasks/stretch.md)
* [Stretch CSV](https://raw.githubusercontent.com/gSchool/boulder-g4-assets/master/gCamp/0070-twitter-bootstrap-tasks/stretch.csv)

References for bootstrap stories:

* http://api.rubyonrails.org/classes/ActionView/Helpers/FormHelper.html#method-i-text_field
* http://getbootstrap.com/css/#tables
* http://getbootstrap.com/css/#forms
