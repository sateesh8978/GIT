# GIT

## Git config

Define the author name to be used for all commits by the current user.
```python
git config --global user.name <name>
```

Define the author email to be used for all commits by the current user.
```python
git config --global user.email <email.
```

Create shortcut for a Git command. E.g. alias.glog log --graph --oneline will set git glog equivalent to git log --graph --oneline.
```python
git config --global alias. <alias-name> <git-command>
```

Set text editor used by commands for all users on the machine. <editor> arg should be the command that launches the desired editor (e.g., vi).
```python
git config --system core.editor <editor>
```

Open the global configuration file in a text editor for manual editing.
```
git config --global --edit
```

## git log

Limit number of commits by <limit>. E.g. git log -5 will limit to 5 commits.
```python
  git log -<limit>
```

Condense each commit to a single line.
```python
git log --online
```

Display the full diff of each commit.
```python
git log -p
```

Include which files were altered and the relative number of lines that were added or deleted from each of them.
```python
git log --stat
```

Search for commits by a particular author.
```python
git log --author=”<pattern>”
```

Search for commits with a commit message that matches <pattern>.
```python
git log --grep="<pattern>'
```

Show commits that occur between <since> and <until>. Args can be a commit ID, branch name, HEAD, or any other kind of revision reference.
```python
git log <since>..<until>
```
  
Only display commits that have the specified file.
```python
git log -- <file>
```

--graph flag draws a text based graph of commits on left side of commit msgs. --decorate adds names of branches or tags of commits shown.
```python
git log --graph --decorate
```

## Git diff

Show difference between working directory and last commit.
```python
git diff HEAD
```

Show difference between staged changes and last commit
```python
git diff --cached
```


## Git reset

Reset staging area to match most recent commit, but leave the working directory unchanged.
```python
git reset
```

Reset staging area and working directory to match most recent commit and overwrites all changes in the working directory.
```python
git reset --hard
```

Move the current branch tip backward to <commit>, reset the staging area to match, but leave the working directory alone.
```python
git reset <commit>
```


Same as previous, but resets both the staging area & working directory to match. Deletes uncommitted changes, and all commits after <commit>.
```python
git reset --hard <commit>
```

## git rebase

Interactively rebase current branch onto <base>. Launches editor to enter commands for how each commit will be transferred to the new base.
```python 
git rebase -i <base>
```

## git pull

Fetch the remote’s copy of current branch and rebases it into the local copy. Uses git rebase instead of merge to integrate the branches.
```python
git pull --rebase <remote>
```

## git push

Forces the git push even if it results in a non-fast-forward merge. Do not use the --force flag unless you’re absolutely sure you know what you’re doing.
```python
git push <remote> --force
```

Push all of your local branches to the specified remote.
```python
git push <remote> --all
```

Tags aren’t automatically pushed when you push a branch or use the --all flag. The --tags flag sends all of your local tags to the remote repo.
```python
git push <remote> --tags
```



