# My GIT Cheatsheet


## Starting a project
You can either start a project locally on your computer *or* you can clone a repo from a server (GitHub or similar).

### Local
To create a local project, go to the folder with the console and type **git init**. And that's it. But you'll like to have something remote to save your local changes.
So create an empty repo in GitHub or similar and do a **git remote add origin _url_to_the_repo_**. After this, you want to "sync" them, use 
**git push -u origin master** so master branch in your local computer tracks master branch in remote repo. The points of this are several, 
but basically makes your life easier.

### Clone from remote
Just type **git clone _url_to_repo_** and that's it. I believe it automatically tracks branches.

## Managing files
To manage files, the basic command is **git status** Gives a nice overview of how things are. If you add a new file, a call to **git status** will mark it as
**untracked**, and you have to **git add _filename_** to start tracking it. Once you are done with the changes in that file, you **git commit _filename_ -m _"message"_**
so git takes a snapshot of your progress. The message is something short that summaries what you've done. What is committed is the status of the file when it was added.
So if you add a file, then modify it, and ask git for status, it will appear as prepared to be committed and changed. The new changes after you add the file 
must have to be added again in order to save them in a snapshot.

### Ignoring files
sometimes there are some files you don't want git to track. To do so, you can create a **.gitignore** file and either manually add there what files you wnat to ignore,
or you could use some rules (look for them online) to ignore certain type of files (like all .pyc files etc.)

### Undoing stuff
If you committed too early, or want to change something, or the commit message, you do a **git commit --amend**. The message is optional (I think), so if you
just wanna add things you forgot to commit, this is the way.

If you wanna _unstage_ staged files, run **git restore --staged _filename_**

If you wanna *undo* changes to files that are NOT staged (you will lose these changes, will get back to the commit version of the file), do a **git restore _filename_**

## Branching
This is done to work in parallel and then merge your changes back to the main line of code (ie, master branch). To create a branch, you can either
**git branch _branchname_** and then **git checkout _branchname_** to change to that branch, or you can directly do a 
**git checkout -b _branchname_**. To create a remote branch that tracks the one you created, do a
**git push -u origin _branchname_**. To merge a branch into *current* branch, do a **git merge _branchname_**, and solve all the conflicts that will appear.
To delete a branch, you do a **git branch -d _branchname_**

## Rebasing
This is very similar to merging, but different. The main point is to clean up messy things. And you should only do it locally, NEVER 
rebase something you pushed somewhere.
Ok, the idea is the following: at some point you have a feat. branch and that branch diverges from master. Now you're ready to merge
feat into master. Well, wha you could do is rebasing instead. That puts the work of the feat branch onto the wotk of the master branch
(you can find merging conflicts) but once you do that, everything is back on  master branch, and a fast forward merge can be easily done.
In commands, you are in the branch feat, that you wanna merge into master, then **git rebase master** to rebase it. Solve potential conflicts
then checkout to master and **git merge feat**

# Table of useful commands
| Command | Functionality |
|--|--:|
|adfaf|afasf|
|asas|afafafafafaf|
|||