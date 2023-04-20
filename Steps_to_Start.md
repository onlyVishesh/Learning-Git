# **Steps to step procedure**

(Refer README.md for mode detail)

## Setup git

    Step 1 - Make Github account
    Step 2 - Create a repo
    Step 3 - Install git (For windows download git bash)
    STEP 4 - git --version (to check if git is install successfully)

rest of the work is done on terminal

## Configure git

    Step 1 - git config --global user.email "youGithub@example.com"
    step 2 - git config --global user.name "Your github Name"

## Work on repo already exist

> ### Commands to clone and work on repo and then commit it in local repo

    Step 1 - git clone <repo url>
    Step 2 - open repo using any code editor and make changes
    Step 3 - git status
    Step 4 - git add . or git add <file name>
    Step 5 - git commit -m "Message" -m "Description"
    Step 6 - git status
    Step 7 - git log
    Step 8 - git push

you can also use git clear if the terminal is filled with code

> ### Commands to upload work on github

1st we have to prove git that we are the owner of the repo

    Step 1 - generate ssh key by ssh-keygen -t rsa -b 4096 -C "Githubemail@example.com" command
    Step 2 - give a file name to save key
    Step 3 - Enter passphrase or enter to leave it blank
    Step 4 - use ls | grep <key file name> to ge list of key
    Step 5 - use .pub key to upload to github never share key without .pub as it is a prove to show that we are the owner of the repo
    Step 6 - open .pub file using - cat <key fle name>
    Step 7 - go to github - under setting click on SSH and GPG keys option

2nd now we can push it to our repo

    Step 1 - git push origin main

## Work on repo you made locally

    Step 1 - open the dir using cd command
    Step 2 - make it a git repo using git init command
    Step 3 - ls -a to see .git file
    Step 3 - now use same commands used in topic "Work on repo already exist" till 1st

we cant use git push origin master command to push our code as there is no origin repo present

## create a empty repo in github
   
    Step 1 - git remote add origin <repo url>
    step 2 - git push origin master

## Work on someones repo

    Step 1 - fork the repo in our repo

> ### To merge

    Step 1 - pull request

## Branching

we can do all the above steps in new branch and then we merge it to main branch.

> ### To check present working branch

    git branch

> ### To create new branch

    git checkout -b <new branch name> ()

> ### To change branch

    git checkout <branch name/path>

> ### To check difference between 2 branches

    git diff <new branch name>

> ### To merge 2 branches by creating a pull request

> > ##### Add all changes to <new branch> and commit it

    git push origin <new branch name>

> > ##### Pull updated main branch

    git pull origin main

> ##### Delete <new branch> after merging

    git branch -d <new branch name>

## Undo

> ### To unstage a added file or all added file

    git reset or git reset <file name>

> ### Undo a last n commit

    git reset HEAD~n

> > ##### To undo last 1 commit

    git reset HEAd~1

> > ##### To undo a specific commit
> >
copy hashes of that specific commit with git log command and then reset

    git log
    git reset <hashes value>

> > #### To undo till a specific commit

    git reset --hard <Hashed value>
