# 2021-05-25 git

- `git init` : initialise git repo in current location
- `git status` : gives you the status
- `git add <FILE>` : adds <FILE> to the staging area
- `git commit` : commits files from staging area
- `git log` : show you commit history
	- `git log --oneline` : condensed history
- `git diff` : shows you changes since last known state
	- `git diff --staged` : shows you changes of what's in staging vs last commit
- `git checkout <commitID> <FILE>` : retrieve <commitID> version of <FILE>
- `git checkout <commitID>` : move HEAD to <commitID>, for whole repo. Useful if wanting to run code from a specific time
	- `git checkout main|master` : get back to last commit for branch name
	- `git switch` : newer version of doing checkout?


HEAD :  where we are at currently  
