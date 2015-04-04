[Week 1 Home](../)

# U1.W1: Tracking Changes

## Learning Competencies

- Define "commit"
- Demonstrate best practices for commit messages
- Describe the three states of a file in git (working, staged, commit)
- Outline the process from creating a change to a commit

## Summary

Git works by following all of the changes in the files inside a git tracked folder. The save point in git is called a commit. Think of a commit like a checkpoint in a video game. It is a point where you can go back to and look at the state of the files at that commit. Just like in a video game if you die at a boss or make the wrong decision, you can go back to the checkpoint. This saves the pain of starting over from the beginning. A commit is your safety net if you accidentally introduce bugs in your code. You can revert to a working state while you debug your code. It is a great idea to commit often to create more frequent save points to fall back on.

## Releases

## Release 0: Watch: What is a change?
[![Tracking Changes](http://img.youtube.com/vi/cBTs3WWMXUs/0.jpg)](http://www.youtube.com/watch?v=cBTs3WWMXUs)

Note: Emmanuel made a new branch here called `git-playground`. You don't have to do that. You can do everything on the `master` branch for this challenge. The `master` branch is the one you are on automatically. You can check which branch you are on by typing `git status`.

## Release 1: Good Commit Messages

Because commits are 'save points', it is important to start getting in the habit of writing good commit messages so you know what each commit includes. Here is [Tim Pope's style guide](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) for commits.There's a bunch of advanced git talk here, so just focus on the first part of the post. See [this article](http://365git.tumblr.com/post/3308646748/writing-git-commit-messages) for a better explanation of why to use the imperative form of verbs.

You can type your commit messages in your terminal with `git commit -m "message goes here between the quotes"`.

You can check the commit history of a repository in the command line by typing `git log` and scroll using the up and down arrows. Exit using `q`. How would you score our git commit messages? Would you know where to look in each message to find what files were changed?

## Release 2: Tracking Changes

Whenever you change the state of a file, it is tracked. You can check the status of all the files in the local repo by typing `git status` . If you have modified any files you will see some categories: Changes not staged for commit:, Changes to be committed:, and if you have created a new file, Untracked files:. No changes would return the message:

`On branch master
nothing to commit, working directory clean`

You can only push changes that have been committed.

Git also gives you handy instructions below these categories. In untracked files it tells you how to add the files (use "git add <file>..." to include in what will be committed) from untracked to staged(changes to be committed), and how to remove a file from the added section to bring it back to untracked (use "git reset HEAD <file>..." to unstage).

If you commit some files and decide that you actually want to change the files, use the command:

`git reset --soft HEAD^`

HEAD is the commit you are currently on, HEAD^ is the last commit, HEAD~3, HEAD~4, HEAD~5, are the 3rd 4th and 5th commit from HEAD respectively.

## Release 3: Make Changes

Now you know about how git tracks changes, so it's time to make some changes! Make sure you are on the `master` branch for this.

Type `git checkout -b making-changes` to create a new branch called `making-changes`.

- Using Sublime, open the [my_reflection.md](my_reflection.md) file associated with this challenge
- Answer the first question in the reflection file - make sure to save your file
- Check your git status
- Write something in this README.md
- Check your git status (notice a pattern?)
- Add the changes you made in the my_reflection.md and README.md to the stage
- Discard the change made to the README.md
- Add and commit the changes for my_reflection.md
- Check the git log to see your commits

Make sure all of your changes are committed before moving on.

## Release 4: Pushing Changes

Now it's time to make your changes live on GitHub. There are two ways to do this, but we aren't going to cover the easiest one because it's bad practice and we've had feedback from students that it should not be included in the curriculum.

The best practice way is by [making pull requests](making-pull-requests.md), which is highly favored when working with teams. We recommend using it, because you will not be happy with yourself if you push to master at Dev Bootcamp. If any of these steps are confusing look at the link above and hopefully that will help.

Before you can push your changes up, you'll want to make sure you don't have different versions of your repository locally and remotely. Checkout your master branch by typing:

`git co master` (if you have the co shortcut working, otherwise write out "checkout")

Pull changes from the remote to your local copy by typing:

`git pull`  git pull fetches changes and merges them. You can also fetch and merge separately if you prefer.

Since you've been working on the making-changes branch you'll want to push that branch up to GitHub. Simply type:

`git push origin making-changes`

`origin` refers to the remote location (in this case your repository on Github), and `making-changes` is the branch you want to push to.

Go to your fork on GitHub. If you click on "Branches" you should see a `making-changes` branch. Click on that.

Right below the branch name you should see a grey bar. On the right of that bar should be a "pull request" button. Click on that. From here, you should see the base pointing to your Fork's master branch. (base:master). Below that you should see a box to type what you changed and a list of the files that have been changed. Fill in the box with important information - like what you did. Then click "Create Pull Request."

Once created, GitHub will tell you whether your changes can be automatically merged. If they can, you should merge them and delete the branch. If they can't, then you have changes somewhere that are causing conflicts. If this is the case, ask for help on the community.

## Release 5: Reflect
Now that you have pushed your changes once, go through it again to add your reflection. You'll want to start off every challenge by creating a new branch. 

Go ahead and answer each of the questions in the my_reflection.md file (using Sublime). Add your changes and commit them. Make sure you make a great commit message when done with this challenge. Don't forget to push your changes, make a pull request, and merge it!

## Release 6: Practice
Remember the reflections you did for the first three challenges? Find your answers and go through the workflow to edit the reflection files for each challenge to add your answers.