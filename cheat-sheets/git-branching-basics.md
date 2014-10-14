# Git Branching Basics

### Create a branch and pull changes into master

1. You should be on the master branch with some commits, working directory clean. To verify:
  * $ git status
    * will tell you what branch you are on and if you have a clean working directory
    * if you are not on your master branch
      * $ git checkout master
    * if you need to commit changes
      * $ git add -A
      * $ git commit -m "\<descriptive message>"
  * $ git log
    * will tell you if you have any commits
    * if you don't have any commits
      * Create desired initial files
      * $ git add -A
      * $ git commit -m "Initial commit"
1. Create and checkout a branch to develop a new feature
  * $ git checkout -b \<awesome branchname>
  * PROTIP : you can always run git status to find out which branch you are in
1. Make one or a few commits to the branch until you are satisfied with the feature in the branch
1. Make sure directory is clean
  * $ git status
1. Go back to the master branch
  * $ git checkout master
1. Bring the changes in your feature branch into master
  * $ git merge \<awesome branchname>
  * PROTIP : You need to STAND in the branch you want to merge changes INTO
  * Merge the changes in the named branch INTO this branch that I am standing in

### Create a branch and abandon changes (AKA Oh god this is a disaster)

1. Follow all steps but the last one listed above
1. If you want that branch to disappear forever and ever
  * $ git branch -D \<awesome branchname>
