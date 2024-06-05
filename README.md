# GIT COMMANDS  

## Basic info setup  

to set username - `git config --global user.name "anushka murade"`  
to set email - `git config --global user.email "muradeanushka04@gmail.com"`  
to set code editor - `git config --global core.editor "code --wait"`  
to ....- `git config --global core.autocrlf "input"`  
to check the value of above things - `git config --global -e`  

## Checkpoints  

to see how many commits/checkpoints we have been created - `git log --oneline` / `git log --oneline --graph`  
to see all the info related to checkpoint for eg:author and all then use - `git log`  
to go one checkpoint back (undo) - `git reser --hard HEAD~1`  

## To push code from Local system to Repo  (will edit this later)

to enable git - `git init`  
to add untracked files to staging area - `git add [filename]`(for adding a particular file) or `git add .` (for adding all files)  
to create a check point - `git commit -m [message]`  
to go back to previous checkpoint - `git reset`  

## xyz  

to check status of files - `git status -s`  
After commiting file git status -s do not shows status  
to remove git from system of folder - `rm -rf .git`  

## Stages of files  

Untracked
Added
Modified

## branching  

