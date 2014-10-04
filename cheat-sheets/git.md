# Git Cheat Sheet

### How to Initialize a local directory as a git repository

1. Create the project folder and initial files.

1. Make sure you are in the topmost directory in your project directory in terminal.

1. Initialize the folder as a git repository.

    $ git init

1. Stage initial content files.

    $ git add -A

1. Commit staged files.

    $ git commit -m "Descriptive Commit Message"

1. Go to GitHub and create a new repository.

    https://github.com

1. Copy the SSH clone URL.

1. Return to your project directory and add the SSH clone URL as a remote.

    $ git remote add origin (SSH clone URL)

1. Push your commits to GitHub.

    $ git push origin master

### How to add new changes to an existing git repository

1. Make any desired changes in your git initialized project directory (see above).

1. Stage any changed files.

    $ git add -A

1. Commit staged files.

    $ git commit -m "Descriptive Commit Message"

1. Push your commits to GitHub.

    $ git push origin master
