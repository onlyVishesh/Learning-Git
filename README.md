# Basic commands to start working on git

## Commands and their working
| SNo.| commands | Description |
| :- | - | - |
| 1 | git config | A convenient way to set configuration options for your Git installation. You’ll typically only need to use this immediately after installing Git on a new development machine. |
| 2 | git init (git init [repository name]) | A convenient way to set configuration options for your Git installation. You’ll typically only need to use this immediately after installing Git on a new development machine. |
| 3 | git add (git add [file(s) name] or git add . or git add *) | Moves changes from the working directory to the staging area. |
| 4 | git clone (git clone [repo URL]) | Creates a copy of an existing Git repository. Cloning is the most common way for developers to obtain a working copy of a central repository. |
| 5 | git status (git status)| Displays the state of the working directory and the staged snapshot. You’ll want to run this in conjunction with git add and git commit to see exactly what’s being included in the next snapshot. |
| 6 | git commit (git commit -m “message”) | Takes the staged snapshot and commits it to the project history. Combined with git add, this defines the basic workflow for all Git users. |
| 7 | git commit --amend | Passing the --amend flag to git commit lets you amend the most recent commit.  This is very useful when you forget to stage a file or omit important information from the commit message. |
| 8 | git log (git log) | Lets you explore the previous revisions of a project. It provides several formatting options for displaying committed snapshots. |
| 9 | git branch (git branch [name-of-the-branch]) | It lets you create isolated development environments within a single repository. |
| 10 | git pull (git pull origin master) | Pulling is the automated version of git fetch. It downloads a branch from a remote repository, then immediately merges it into the current branch. This is the Git equivalent of svn update. |
| 11 | git push (git push origin [branch name]) | Pushing is the opposite of fetching (with a few caveats). It lets you move a local branch to another repository, which serves as a convenient way to publish contributions. This is like svn commit, but it sends a series of commits instead of a single changeset. |
| 12 | git clean | Removes untracked files from the working directory. This is the logical counterpart to git reset, which (typically) only operates on tracked files. |
| 13 | git merge (git merge [another-file-name]) | A powerful way to integrate changes from divergent branches. After forking the project history with git branch, git merge lets you put it back together again. |
| 14 | git checkout | In addition to checking out old commits and old file revisions, git checkout is also the means to navigate existing branches. Combined with the basic Git commands, it’s a way to work on a particular line of development. |
| 15 | git fetch | Fetching downloads a branch from another repository, along with all of its associated commits and files. But, it doesn't try to integrate anything into your local repository. This gives you a chance to inspect changes before merging them with your project.
| 16 | git rebase | Rebasing lets you move branches around, which helps you avoid unnecessary merge commits. The resulting linear history is often much easier to understand and explore.
| 17 | git rebase -i | The -i flag is used to begin an interactive rebasing session. This provides all the benefits of a normal rebase, but gives you the opportunity to add, edit, or delete commits along the way.
| 18 | git reflog | Git keeps track of updates to the tip of branches using a mechanism called reflog. This allows you to go back to changesets even though they are not referenced by any branch or tag.
| 19 | git remote | A convenient tool for administering remote connections. Instead of passing the full URL to the fetch, pull, and push commands, it lets you use a more meaningful shortcut. |
| 20 | git reset | Undoes changes to files in the working directory. Resetting lets you clean up or completely remove changes that have not been pushed to a public repository. |
| 21 | git revert | Undoes a committed snapshot. When you discover a faulty commit, reverting is a safe and easy way to completely remove it from the code base. |

## Setup commands
1. open termenal and write these commands

        git config --global user.name "Your Github name"
        git config --global user.email "Your Github email id"

## Starting a Project with Git 
1. Create a local repo (omit <directory> to initialise the current directory as a git repo) 

        git init <directory>

2. Download a remote repo

        git clone <repo url>


##  Make a change
1. Add a file to staging 

        git add <file>

2. Stage all files 

        git add .

3. Commit all staged files to git 

        git commit -m "commit message"

4. Add all changes made to tracked files & commit

        git commit -am "commit message"

## Branches

List all local branches. Add -r flag to show all remote branches. -a flag for all branches.

1. To git present working branch

        git branch

2. Create a new branch 

        git branch <new-branch>

3. Switch to a branch & update the working directory

        git checkout <branch>

4. Create a new branch and switch to it 

        git checkout -b <newbranch>

5. Delete a merged branch 

        git branch -d <branch>

6. Delete a branch, whether merged or not 

        git branch -D <branch>

7. Add a tag to current commit (often used for new version releases) 

        git tag <tag-name>

## Merging
Merge branch a into branch b. Add --no-ff option for no-fast-forward merge

    git checkout b
    git merge a

Merge & squash all commits into one new commit - git merge --squash a

to be continued ..

  
  
  
Reference - https://dev.to/doabledanny/git-cheat-sheet-50-commands-free-pdf-and-poster-4gcn

testing git status
