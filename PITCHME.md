#HSLIDE

# git Workshop

## Get Into git easily

Norbert Eder
[@norberteder](https://www.twitter.com/norberteder)

#HSLIDE

## Glossary

Topic | Description
----- | -----------
Clone | Clone a repository into a new directory
Checkout | Switch branches or restore working tree files
Merge | Join two or more development histories together
Stash | Shelve the changes in a dirty working directory away

#HSLIDE

## Basics

Introduction into git

#VSLIDE

* Distributed version control system
* Remote and local version database
* Git only adds data (never deletes)

#VSLIDE

### Configuration

* global
* local

#VSLIDE

#### List Configuration

List global configuration

```
git config --global -l
```

List local configuration

```
git config -l
```

#VSLIDE

#### Configure Identity

Set global configuration

```
git config --global user.name "Max Mustermann"
git config --global user.email "m.mustermann@test.com"
```

Set local configuration

```
git config user.name "Max Mustermann"
git config user.email "m.mustermann@test.com"
```

Remove configuration

```
git config --unset <name>
git config --unset-all <name>
```

#HSLIDE

## Common Commands

Commands you have to know

#VSLIDE

### Repository

Initialize Repository

```
git init
```

Clone Repository

```
git clone https://github.com/norberteder/git-workshop
```

#VSLIDE

### Handling files

Add new file

```
git add file-to-add.md
```

Add all files

```
git add .
```

Remove file

```
git rm file-to-delete.md
```

#VSLIDE

### Show information

Show working tree status

```
git status
```

Show commits/diffs

```
git show
```

Show log

```
git log [<file>]
```

Show diffs

```
git diff
```

#HSLIDE

## Handling changes

Working with changes

#VSLIDE

### Transfer changes to server

Add changes to local repository

```
git commit -am "meaningful commit message"
```

Push changes to remote repository

```
git push
```

#VSLIDE

### Undo Things

Unmodify modified file

```
git checkout -- <filename>
```

Revert commit

```
git revert 9f38eff
```

#VSLIDE

## Stashing

Stash working changes

```
git stash
```

Show all stashes

```
git stash list
```

Show specific stash

```
git stash show <stash>
```

Drop stash

```
git stash drop <stash>
```

Apply stash

```
git stash pop <stash>
```

#HSLIDE

## Branches

Working with branches

#VSLIDE

### Working with branches

List branches

```
git branch
```

Create branch

```
git branch <branchname>
```

Rename branch

```
git branch -m <old-branchname> <new-branchname>
```

Delete branch

```
git branch -d <branchname>
```

#VSLIDE

### Switch branches

Switch branch

```
git checkout <branch>
```

Create and/or reset branch

```
git checkout -f <branch>
```

### Merge branches

Call from target branch

```
git merge <branch>
```

#HSLIDE

## Workshop

### Local Branch

```
(master): git checkout -b hotfix
(hotfix): git commit -am "Change .... "
(hotfix): git checkout master
(master): git merge hotfix
(master): git push
(master): git branch -d hotfix
```