# GIT
## GIT Basics


Create empty Git repo in specified directory. Run with no arguments to initialize the current directory as a git repository.
```python
git init <directory>
```
  
Clone repo located at <repo> onto local machine. Original repo can be located on the local filesystem or on a remote machine via HTTP or SSH.
```python
git cone <repo>
```

Define author name to be used for all commits in current repo. Devs commonly use --global flag to set config options for current user.
```python
git config user.name <name>
```
  

Stage all changes in <directory> for the next commit. Replace <directory> with a <file> to change a specific file.
```python
git add <directory>
```

Commit the staged snapshot, but instead of launching a text editor, use <message> as the commit message.
```python
git commit -m "<message>"
```  

List which files are staged, unstaged, and untracked.
```python
git status
```
  
Displays the entire commit history using the default format. For customization see additional options.
```python
git log
```  

Show unstaged changes between your index and working directory.
```python
git diff
```

## Undoing Changes 


Create new commit that undoes all of the changes made in <commit>, then apply it ti the current branch.
```python
git revert <commit>
```  

Remove <file> from the staging area, but leave the working directory unchanged. This unchanges a file without overwriting any changes.
```python
git reset <file>
```
  
Shows which files would be removed from working directory. Use the -f flag in place of the -n flag to execute the clean.
```python
git clean -n
```

## Rewriting Git history

Replace the last commit with the staged changes and last commit combined. Use with nothing staged to edit the last commit's message.
```python
git commit --amend
```

Rebase the current branch onto <base>. <base> can be a commit ID, a branch name, a tag, or a relative reference to HEAD.
```python
git rebase <base>
```

Show a log of changes to the local repository's HEAD. Add --relative-date flag to show date onfo or --all to show all refs.
```python
git reflog
```

## Git Branches 

List all of the branches in your repo. Add a <branch> argument to create a new branch with the name <branch>.
```python
git branch
```
Create and check out a new branch named <branch>. Drop the -b flag to checkout an existing branch.
```python
git checkout -b <branch>
```
  
Merge <branch> into the current branch.
```python
git merge <branch>
```
## Remote Repositories

Create a new connection to a remote repo. After adding a remote, you can use <name> as a shortcut for <url> in other commands.
```python
git remote add <name> <url>
```

Fetches a specific <branch>, from the repo. Leave off <branch> to fetch all remote refs.
```python
  git fetch <remote> <branch>
```

Fetch the specified remote’s copy of current branch and immediately merge it into the local copy.
```python
git pull <remote>
```

Push the branch to <remote>, along with necessary commits and objects. Creates named branch in the remote repo if it doesn’t exist.
```python
  git push <remote> <branch>
```
  


  




