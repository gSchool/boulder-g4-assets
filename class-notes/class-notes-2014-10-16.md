## Class Notes, October 16th, 2014

(will be live-updated)

### Git

Create a branch:

```
git checkout -b my-new-branch-name
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

### Interpreting Wireframes

* Avoid comic fonts
* Avoid adding your own borders / background colors (we removed black from the wires)

### Rails CRUD

Finish https://students.gschool.it/cohorts/3/exercises/139

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
