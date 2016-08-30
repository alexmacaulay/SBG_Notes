#22nd August - Git

## Git Revision

* git reset --soft HEAD^
  * this goes back to one before HEAD and keeps changes in staging
  * like an undo on the commit
* git commit --amend -m "Added new files 1 and 2"
  * adds these changes to last commit as well
  * useful for if missed commit message or a rubbish one
  * useful if forgot to commit something that should have been all in one

**_Look up git stash_**

## Git Branching

* **git branch new-branch** - creates a new branch
* **git checkout new-branch** - changes to new branch

## Git Merging

* Fast-forward merge
* Recursive merge

## Git Rebase

* git checkout new-branch
* git rebase master
* git checkout master
* git merge master
* git branch -d new-branch
* **What does rebase -i do?**

## Git Homework

* Watch https://www.youtube.com/user/GitHubGuides/videos
* Read https://git-scm.com/documentation
* Practice branching, merging and rebasing
* Set up some bash or git aliases to streamline your workflow
* Research the feature branch workflow: https://youtu.be/EwW~byjDs9c
