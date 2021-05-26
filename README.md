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

## github wikis
Useful for additional documentation or information about the project
