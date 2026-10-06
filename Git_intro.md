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
    - Go to setting in GitHub and go to developer ten generate a general tocken

-  and enter that tocen as password

# Note :-- 
- If i want to push again then it will ask for the id password

# hack - One methos is to add the tocken to th url :

-- git remote set-url origin https://<tocken>@github.com/radheshayamkumar/git-for-devops.


# Second Method for Git push
 cd .ssh
 ssh-keygen
 - copy the id255.pub
 -GITHUB --> account -setting
        -go to SSH and GPG
        - click on new-ssh-key
        -paste the public key
--> Go back to SSH
--> we have 3 option to clone the repo
    :- https,ssh and github cli
-> go to ssh and copy the git@github link


-> In your ubuntu -> go to your respective folder
# change the remote origin
    -git remote set url origin <paste the ssh url>
# git remote -v
# git status 
`add some changes`
# git add .
# git commit
# git push origin master

SO Now no need to enter again and again is&pass

# git pull
- `git pull origin main`
    -(if you have change in the github (remote) then to reflect that changes in your local)

## BRANCHING STRATEGIES

-`Master/main branch`
    -It is protected, used for production
- `dev/develop branch`
    - Used by developers to develop new features , after development of features it will go for testing branch.
- `Staging/QA branch`
    - Another branch to test that features after testing it will be merged to `master/main

- `Feature/ticketID branch`
    - Feature branch comes from dev branch and if 50 people working on 50 features, there will be 50 `features` branches.
- If feature works merge to `dev` then `stagging/qa` then finally `Master`.

 # Note :
  Suppose bug arrives in production -> A new branch will created `hotFix`, developer will fix then it merges to `master` and `stagging` and sttaging will go to `dev`.

# Branching
`git checkout -b dev`
`git checkout -b stagging`

-- create features.md in `dev`
# merge branch
`git checkout stagging`
`git status`
`ls` 
`git merge dev` -- To merge dev with stagging

- `git log --oneline`

# Master Branch merging
-- Always do with gitHub
-- you can create a pul req and can review it with multiple peoples.
-- But in git review process is not possible

`git push origin stagging`

- Go to GitHub
- Click on compare and pull
- Go to GitHub repo settings -> collaborations -> add people -> add as a collaborator

# doc :
https://nvie.com/posts/a-successful-git-branching-model/

# pull req
-- suppose you have added a feature in dev
-- `git add .`
-- `git commit -m "msg"`
-- `git push origin dev`

--Now you want this feature in `stagging` branch

=> In gitHub repo Click on `create pull request`
=> put the branches for compare
=> GO to new tab and search for `codeRabbit`
=> Go to `Get started` -> Sign-up through github
=> You can see all the repos of your github after sign in
=> Go to your repo -> review (chill,Assertive)
=> ignore title keyword - if written draft then it will not review

# Branch protection rule

-> Settings -> Branches ->Branch protection rule