#HSLIDE

# git Workshop

## Get Into git easily

Norbert Eder
[@norberteder](https://www.twitter.com/norberteder)

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

Show commits

```
git show
```

Show log

```
git log
```

Show diffs

```
git diff
```

#HSLIDE

## Transfer changes to server

Add changes to local repository

```
git commit -am "meaningful commit message"
```

Push changes to remote repository

```
git push
```

#HSLIDE

## Undo Things

Unmodify modified file

```
git checkout -- <filename>
```

Revert commit

```
git revert 9f38eff
```

#HSLIDE

## Working with branches

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

## Switch branches

Switch branch

```
git checkout <branch>
```

Create and/or reset branch

```
git checkout -f <branch>
```

## Merge branches

Call from target branch

```
git merge <branch>
```

#HSLIDE

## Workshop

### Local Branch