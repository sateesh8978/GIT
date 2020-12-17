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

git log -<limit>
Include which files were altered and the relative number of lines that were added or deleted from each of them.
git log --oneline
Display the full diff of each commit.
git log --stat
Search for commits by a particular author.
git log -p
git log --author=
”<pattern>”
Show commits that occur between <since> and <until>. Args can be a commit ID, branch name, HEAD, or any other kind of revision reference.
git log --grep=”<pattern>”
git log <since>..<until>
Only display commits that have the specified file.
git log -- <file>
--graph flag draws a text based graph of commits on left side of commit msgs. --decorate adds names of branches or tags of commits shown.
