# Steps to step procedure

(Refer README.md for mode detail)

## Setup git

Step 1 - Make Github account
Step 2 - Create a repo
Step 3 - Install git (For windows download git bash)
rest of the work is done on terminal

## Configure git

Step 1 - git config --global user.email "youGithub@example.com"
step 2 - git config --global user.name "Your github Name"

## Work on repo already exist

### Commands to clone and work on repo and then commit it in local repo

Step 1 - git clone <repo url>
Step 2 - open repo using any code editor and make changes
Step 3 - git status
Step 4 - git add . or git add <file name>
Step 5 - git commit -m "Message" -m "Descrption"
Step 6 - git status
Step 7 - git push

you can also use git clear if the terminal is filled with code

### Commands to upload work on github

1st we have to prove git that we are the owner of the repo

Step 1 - generate ssh key by ssh-keygen -t rsa -b 4096 -C "Githubemail@example.com" command
Step 2 - give a file name to save key
Step 3 - Enter passphrase or enter to leave it blank
Step 4 - use ls | grep <key file name> to ge list of key
Step 5 - use .pub key to upload to github never share key without .pub as it is a prove to show that we are the owner of the repo
Step 6 - open .pub file using - cat <key fle name>
Step 7 - go to github - under setting click on SSh and GPG keys option

2nd now we can push it to our repo
Step 1 - git push origin master

## Work on repo you made locally

Step 1 - open the directory using cd command
Step 2 - make it a git repo using git init command
Step 3 - now use same commands used in topic Work on repo already exist till 1st
we cant use git push origin master command to push our code as there is no origin repo present

option 1 - create a empty repo in github
Step 1 - git remote add origin <repo url>
step 2 - git push origin master
