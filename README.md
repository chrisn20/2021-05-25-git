# 2021-05-25 git

- `git init` : initialise git repo in current location
- `git status` : gives you the status
- `git add <FILE>` : adds <FILE> to the staging area
- `git commit` : commits files from staging area
- `git log` : show you commit history
	- `git log --oneline` : condensed history
- `git diff` : shows you changes since last known state
	- `git diff --staged` : shows you changes of what's in staging vs last commit
	- `git diff HEAD~2` : diff 2 commits ago
	- `git diff <SHA> <FILE>` : diff a file against a specific commit
- `git checkout <SHA> <FILE>` : retrieve <SHA> version of <FILE>
- `git checkout <SHA>` : move HEAD to <SHA>, for whole repo. Useful if wanting to run code from a specific time
	- `git checkout main|master` : get back to last commit for branch name
	- `git switch` : newer version of doing checkout?


- HEAD :  where we are at currently  
- .gitkeep : convention to create this as a file in an empty directory that should be tracked/kept in the repo
- .gitignore : for files that shouldn't be committed - e.g. data files, temporary/auxilliary files/compiled binaries/etc


## remotes
- `git remote add <NAME> <URL>`: <NAME=origin> point to the remote
- `git push <WHERE> <WHAT>` : local -> remote
- `git pull <WHERE> <WHAT>` : remote -> local

## fix branches
1. git checkout -b main
2. git push origin main
3. fix branch names on github

## github project management
- `issues` can be used to track tasks and things that need doing
- `labels` can be applied to issues to give more context about the issue - i.e. the issue may be a bug to fix, enhancements/new features to add, or other
- issues can be grouped into `milestones` of similar issues or to sign-point when particular issues may be addressed
- when writing commits, `fixes #<issue>` in the commit message will automatically close the issue once the commit is merged into master and pushed to github

## github wikis
Useful for additional documentation or information about the project

## branches
Branches are useful for prototyping new code whilst preserving known last good versions of code in the main branch. Changes in the branch will only be visible in the branch until merged/pulled back into the main branch.
- `git branch <BRANCH>` : create new branch called <BRANCH>
- `git branch -a` : list all branches
- `git branch -d <BRANCH>` : delete  <BRANCH>. Add -r flag for remote branches
- `git checkout <BRANCH>` : switch to <BRANCH>
- `git checkout -b <BRANCH>` : create new <BRANCH> and switch to it 

To merge branches, switch to the branch to merge changes into and run `git merge <BRANCH>` where <BRANCH> is the branch to merge from.

### Pull Requests
- Pull requests are a way to merge branches on GitHub. 

### Cleanup branches
- `git fetch --prune` : updates the information from github, and deletes local branches that no longer exist on remote


## working with VSCODE and git
- VSCODE has a GUI to interface with git, which can help manage staging, commits, pushes/pulls, and merges
- However, if a command line experience is preferred, it is also possible to use the git commands in the integrated terminal
- The GUI will reflect commands ran in the terminal, so everything lines up very nicely! Good job, Microsoft!

## Workflows
- Could have main branch, then development branch, then feature branch.
- Development branch used to track development. Individual features are created as branches from development and merged back in.
- Once development branch is stable and ready for a release, these can be merge back into the main branch.