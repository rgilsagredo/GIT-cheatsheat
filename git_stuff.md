Starting with GIT:

you an either create a local repo and worj there, or clone a repo that is on some server like github

Create something local:
go to the folder, and type "git init". That creates a local repo. But you'll like to have also a remote repo to save and share your local work, so go to github (or similar)
and create a repo (an empty one, i created "https://github.com/rgilsagredo/GIT-cheatsheat.git") and then sync them with 
"git remote add origin https://github.com/rgilsagredo/GIT-cheatsheat.git"
After this, you set the local to treack the remote with git push -u origin master


Cloning from existin repo:
use "git clone url" to copy it to your local machine


Managing files



useful commands
git init --> create a local repo
git clone "url" clones an existing repo
git remote add origin "url" adds a remote to current repo
git "command_name" -h quick help for a command
git push -u origin master --> pushes the branch to track remote branch "master"
git branch -M "name" renames current branch to "name"
git branch -vv shows a lot of info, very useful