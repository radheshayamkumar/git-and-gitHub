###Git

GIT -Global Information Tracker

-Version control system

-Also Called as SCM (Source Code Management)

--Download the Git Bash
(https://github.com/git-for-windows/git/releases/download/v2.56.0.windows.1/Git-2.56.0-64-bit.exe)
- Git Bash is a tool that provides a simulation of Linux

--Every Folder should have its own git
--So always create a folder for your project, Context :- If you installed git in your C Drive git will track your system.. 


## File System Limitations :
- Can't Restore files.
- Can't control Versions.
- Can't understand who edied the file and time of editing.

## Git version control system :
-can restore
-can manage version 
-can understand the author and time of editing.

--  touch nibba.txt nibbi.txt
## Git init 
- initialize the git
## ls -a
- you can see the .git folder
- version control system is in .git folder
## git status (untracked..)
- It tells about untracked files.
- Both nibba.txt and nibbi.txt are untracked.
## git add .  (staged)
- git add nibbi.txt (now this file is tracked : staged)
- still another file nibba.txt is untracked.
Note : Untracked :red , Tracked : Green

- git add nibba.txt
- Now both files are staged

## git rm <file_name> (To untracked the file)
- git rm nibba.txt (This file will now Unstaged)

To staged again : git add nibba.txt  

# git commit -m <"messgae">  (Tracked)
- git commit -m "nibba nibbi added.

## If i remove the file from file system
- rm nibba.txt (Deleted from file system)

# git status 
- you can still see here that file as :
deleted : nibba.txt

# git restore  <file_name>
- git restore nibba.txt

# Note :- Add author
- git config --global user.name "user_name"
-git config --global user.email "email@gmail.com"

# Note :
- If you change something in file
- the changed will be untracked 
- To track :
    -- git add .  (staged)
    -- git commit -m "msg" (tracked)
Note : A new version will created 

# git log 
- You can see the commit logs
 
 # Branch
 - git checkout -b dev
    -- (-b) creating a new branch
- git checkout master
    -- (switch to master branch)
-- git branch

-- git log (every branch has its seperate logs)

-- git switch dev (same as checkout)

# Head
-- Latest commit of any branch

# git log --oneline
    -- log in single line (latest commit)
    -- you can see the head

# git clone
    --To clone your repo from gitHub to local

#  git status
    -- check status of files : tracked or Untracked
 # git remote -v
    -- check the location of your code

# git push
    -- To publish the local change
    ask for username :
    password :
    