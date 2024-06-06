# GIT COMMANDS  

## Basic info setup  

to set username - `git config --global user.name "anushka murade"`  
to set email - `git config --global user.email "muradeanushka04@gmail.com"`  
to set code editor - `git config --global core.editor "code --wait"`  
to ....- `git config --global core.autocrlf "input"`  
to check the value of above things - `git config --global -e`  

## Checkpoints  

to see how many commits/checkpoints we have been created - `git log --oneline`  
to see all the info related to checkpoint for eg:author and all then use - `git log`  
to go one checkpoint back (undo) - `git reset --hard HEAD~1`  

## To push code from Local system to Repo  

Create a repo and then follow these 7 steps and commands in local folder to push it to that github repository  

1. add a readme.md file then  
2. to enable git - `git init`  
3. to add untracked files to staging area - `git add [filename]`(for adding a particular file) or `git add .` (for adding all files)  
4. to create a check point - `git commit -m "[message]"`  
5. `git branch -M main`  
6. `git remote add origin [url]`  
to verify remote origin - `git remote -v`  
to remove a remote origin - `git remote rm origin`  
7. `git push -u origin main`  
optional :  
to go back to previous checkpoint - `git reset`  

## Cloning  

to copy that repo in ur computer use - `git clone [url]`  
to create a new branch and switch simultaneously - `git switch -C [branchname]`  
add changes in new branch  
`git add.`  
`git commit -m "message"`  
`git push origin [newbranch]`  

## xyz  

to check status of files - `git status -s`  
After commiting file git status -s do not shows status  
to remove git from system of folder - `rm -rf .git`  

## Stages of files  

Untracked  
Added  
Modified  
Commited  

## Branching  

to create a new branch - `git branch [branchname]`  
to switch/go on that branch - `git switch [branchname]`  
{note - copy the code create new branch and make changes in the code of that new branch  }  
to merge the branch u are supposed to be on main branch and then run this command - `git merge [anotherbranchname]`  
{note - while merging there can be conflict  
for eg. branch1 has code with line no. 10 as `<div></div>`  
branch2 has code with line no. 10 as `<p></p>`  
so while merging they as whether u want code of branch1 or 2 or both so choose according and then again do git add. and git commit -m "msg"  }  
to delete a branch - `git branch -d [branchname]`  
to create a new branch and switch simultaneously - `git switch -C [branchname]`  

drafting - `git stash`  
{we made some changes on current branch and didn't commited and moved to another branch so the changes made in previous branch is saved or kept draft so that when u come on this branch later u will be able to see those changes that u made earlier }  
to get back those changes that u made in previous code - `git stash apply`
to delete the draft - `git stash clear`  

## Collaboration  

### Person 1  (main)

Create a repo and then follow these 7 steps and commands in local folder to push it to that github repository  

1. add a readme.md file then  
2. to enable git - `git init`  
3. to add untracked files to staging area - `git add [filename]`(for adding a particular file) or `git add .` (for adding all files)  
4. to create a check point - `git commit -m "[message]"`  
5. `git branch -M main`  
6. `git remote add origin [url]`  
to verify remote origin - `git remote -v`  
to remove a remote origin - `git remote rm origin`  
7. `git push -u origin main`  
optional :  
to go back to previous checkpoint - `git reset`  

### Person 2  (contributor)

to copy that repo in ur computer use - `git clone [url]`  
to create a new branch and switch simultaneously - `git switch -C [newbranchname]`  
add changes in new branch  
`git add.`  
`git commit -m "message"`  
`git push origin [newbranch]`  

### again Person 1  (who fetches and merges and pushes code again)  

to get that new branch created by person 2 - `git fetch`  
to switch to that branch - `git switch [newbranchname]`  
to merge to back to main branch - `git merge [newbranchname]`  
push - `git push origin main`  

### again Person 2 (who fetches final code)  

fetch-> merge  
instead do pull since (fetch+merge->pull)  

So to get final code - `git pull`  
