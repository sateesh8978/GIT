# GIT
## GIT Basics

git init <directory> 
  Create empty Git repo in specified directory. Run with no arguments to initialize the current directory as a git repository.
  
git cone <repo>
  Clone repo located at <repo> onto local machine. Original repo can be located on the local filesystem or on a remote machine via HTTP or SSH.
  
git config user.name <name>
  Define author name to be used for all commits in current repo. Devs commonly use --global flag to set config options for current user.
  
git add <directory>
  Stage all changes in <directory> for the next commit. Replace <directory> with a <file> to change a specific file.
  
git commit -m "<message>"
  Commit the staged snapshot, but instead of launching a text editor, use <message> as the commit message.
  
git status
  List which files are staged, unstaged, and untracked.
  
git log
  Displays the entire commit history using the default format. For customization see additional options.
  
git diff
  Show unstaged changes between your index and working directory.


## Undoing Changes 

git revert <commit> 
  Create new commit that undoes all of the changes made in <commit>, then apply it ti the current branch.
  
git reset <file>
  Remove <file> from the staging area, but leave the working directory unchanged. This unchanges a file without overwriting any changes.
  
git clean -n 
  Shows which files would be removed from working directory. Use the -f flag in place of the -n flag to execute the clean.


## Rewriting Git history

git commit --amend
  Replace the last commit with the staged changes and last commit combined. Use with nothing staged to edit the last commit's message.

