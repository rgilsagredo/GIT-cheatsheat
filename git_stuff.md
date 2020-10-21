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
one you have your git repo, yu can start managing the files that are in it.  the basic command is "git status". Whenever you create a new file on the repo and check
the status it will be tagged wth "untracked", meaning isnew for git. you hac¡ve to "git add file" so git can start making snapshots of it, otherwise
it will be forever untracked. one you add it, it will be tagged as new file. then you can commit (take a snapshot of it"
what is saved in a commit is the status of the file when "added", if you modify afterwards and commit, you wont get the changes unless you re-add the file.
when you modify a tracked file git tells you that it has been modified.
and yeah, commit is basically take a snapshot of what i just added
you can unadd a file with git reset
ignoring files: 
first you should create a ".gitignore" file, in windows, just create a txt file called gitignore.txt, and rename it to ".gitignore."
in that file, add the file you want git to ignore, or he patters for multiple files/folders. Seek for the patterns online



useful commands
git init --> create a local repo
git clone "url" clones an existing repo
git remote add origin "url" adds a remote to current repo
git "command_name" -h quick help for a command
git push -u origin master --> pushes the branch to track remote branch "master"
git branch -M "name" renames current branch to "name"
git branch -vv shows a lot of info, very useful
git status to see how your work is doing
git reset file unadds a file