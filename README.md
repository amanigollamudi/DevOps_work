# DevOps_work
DevOps assignments,and related documentation


# git config --global user.name “amanigollamudi”
# git config --global user.email “amanigollamudi@gmail.com”
# git config --list
# git init - it initializes empty git repository in local
Initialized empty Git repository in your local .git/ which is going to keep tracking all your changes

C:/Users/User/Documents/git_practice_latest/.git/
#git status
which is keep tracking all your changes
# touch file.html  file.php  file.txt
# git status
we have 3 untracked files, Which is under working copy not added to staging yet. 
to add these changes to staging area and to git keep tracking the changes
# git add file.html  - > Which can only move one file from working copy to the staging
# git add . - > all the files which are in working copy will moved to staging
# git commit -m " Initial commit" - Now the changes which are in staging commited to local repository
-m -> message that refers to changes you made in that commit"
-> To check history of commits
# git log
if you want to shot this output
# git log --oneline
-> To see the details in commit what was happened
# git show < commit id first 5 to 6 characters>
----
**Git Restore :-**

# git restore < file_name>  - undo the changes in working directory
git restore is a command to discard latest changes in working directory, This will only discard changes for git tracked files. if the file is untracked file it cannnot do anything for that file
 
-> After moves the changes to the staging you want to get the file to the working directory
# git restore --staged file_name
working   --   staging   ---  local  --- repository
file.html  --   git add .  --  git commit  -- git push 
undo the changes in working directory - # git restore file_name
revert the changes from staging to working - # git restore  --staged file_name
 

- > To check the differences between the commits
# git diff <commit id1> <commit id2>

**Git Reset:**

When you want to revert the changes from local repository to staging or local repository to working directory use commands
local repo to staging   - > # git reset --soft HEAD~1
local repo to working directory  -> # git reset --mixed HEAD~1
when you want to completely remove the changes -> # git reset --hard HEAD~1
Note: If you are not specified whether it is soft/mixed/hard by default it will take mixed means it will move the changes from local repo to working directory
# git reset HEAD~2 / # git reset --mixed HEAD~1
Note: - Maximum we can move the HEAD count till 4 - 5 commits
What is HEAD?
HEAD is a movable object in git which always pointing to latest commit


**Git Push:-**

To publish the changes to the remote repository use the command
$ git remote add origin (repository link) https://github.com/amanigollamudi/DevOps_work.git

