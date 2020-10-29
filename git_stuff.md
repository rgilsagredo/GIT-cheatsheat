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


undoing stuff:
you commited too early, want to either add files and/or change the message. you do an amend
To just chaneg the message, do "git commit --amend -m "nuevo mensaje""
si quieres añadir cosas que se te han pasado, le das a add y "git commit --amned" (with new massage optional)

para quitar cosas del stage (antes de hacer commit) haces un "git reset HEAD file2beunstaged", también "git restore --staged <file>..." to unstage
para deshacer cambios que no quieres, anets de stagear, hace un "git git checkout -- fine_name o git restore file_name

branching
this is used to develop something in paraller nd then put it back to the main branch of development
to create a branch, "git branch <name>". to go to that branch, git checkout <name>. To create a remote branch that tracks the one you created, do a
"git push -u origin <name>"



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
git commit --amend -m "some msg" --> para no añadir un commit estúpido más porque lo has hecho mal
git restore --stages file --> para destagear un archivo
git restore file_name --> para deshacer cambios en un fichero que no quieres (ojo que se pierden)
"git branch <name>" --> creates a brch
git checkout <name> --> changes to the branch <name>
git log --oneline --decorate --graph --all --> shows hist with nice graph of the branching
git checkout -b <name> --> creates new branch and switches to it
git branch -d/-D <name> --> deteles/force deletes a local branch
git push -u origin <name> --> pushes local branch to remote, and tracks it
git push origin --delete <name> --> delertes remote branch
