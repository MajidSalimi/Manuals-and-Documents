# Git Commands
### Initial configuration

    git config --global user.name "username"
    git config --global user.email "mail"
    git config --global colur.ui true
    git config --global core.editor
    
### Getting & Creating Projects

Initialize a local Git repository:

    git init	
    
Create a local copy of a remote repository:

    git clone ssh://git@github.com/[username]/[repository-name].git	
    
### Basic Snapshotting

Check status:

    git status	

Add a file to the staging area:

    git add [file-name.txt]	

Add all new and changed files to the staging area:

    git add -A	

Commit changes:
  
    git commit -m "[commit message]"	
    
Remove a file (or folder):

    git rm -r [file-name.txt]	
    
###Branching & Merging

List branches (the asterisk denotes the current branch):

    git branch	

List all branches (local and remote):

    git branch -a	
    
Create a new branch:
    
    git branch [branch name]	
    
Delete a branch: 

    git branch -d [branch name]	
    
Delete a remote branch:

    git push origin --delete [branchName]	

Create a new branch and switch to it:
  
    git checkout -b [branch name]

Clone a remote branch and switch to it:

    git checkout -b [branch name] origin/[branch name]
    
Switch to a branch:

    git checkout [branch name]	
    
Switch to the branch last checked out:

    git checkout -	

Discard changes to a file:

    git checkout -- [file-name.txt]	

Merge a branch into the active branch:

git merge [branch name]	

Merge a branch into a target branch

    git merge [source branch] [target branch]
    
###Sharing & Updating Projects

Push a branch to your remote repository:

    git push origin [branch name]	
    
Push changes to remote repository (and remember the branch):

    git push -u origin [branch name]	
    
Push changes to remote repository (remembered branch):

    git push	
    
Delete a remote branch:

    git push origin --delete [branch name]	
    
Update local repository to the newest commit:

    git pull	
    
Pull changes from remote repository:

    git pull origin [branch name]
    
Add a remote repository:

    git remote add origin ssh://git@github.com/[username]/[repository-name].git	
    
Set a repository's origin branch to SSH:

    git remote set-url origin ssh://git@github.com/[username]/[repository-name].git	
    
### Inspection & Comparison

View changes:

    git log

View changes (detailed):

    git log --summary	View changes (detailed)
    
    
Preview changes before merging:

    git diff [source branch] [target branch}	







