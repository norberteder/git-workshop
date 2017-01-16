#HSLIDE

# git Workshop

## Get Into git easily

Norbert Eder
[@norberteder](https://www.twitter.com/norberteder)

#HSLIDE

## Glossary 1

Topic | Description
----- | -----------
Blame | Show annotation
Clone | Clone a repository into a new directory
Checkout | Switch branches or restore working tree files
Merge | Join two or more development histories together

#VSLIDE

## Glossary 2

Topic | Description
----- | -----------
Pull | Incorporates changes from a remote repository into the current branch
Push | Updates remote refs using local refs
Remotes | Repositories on internet or network
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

Add new file (stage)

```
git add <filename>
```

Add all files

```
git add .
```

Remove file

```
git rm <filename>
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

### List branches

List existing branches

```
git branch
```

List remote and local branches

```
git branch -a
```

List only remote branches

```
git branch -r
```

#VSLIDE

### Working with branches

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

You can switch branches while having uncommitted work.

#VSLIDE

### Merge branches

Call from target branch

```
git merge <branch>
```

#HSLIDE

## Merging

How merging works

#VSLIDE

### Types of merges

* *Fast-forward*: Current branch head is an ancestor of the named commit
* *True merge*: Branches to be merged must be tied together by a merge commit; has two parents

### Merge Commands

Abort merge

```
git merge --abort
```

#HSLIDE

## Remotes

Working with Remotes

#VSLIDE

### Basics

* Remote repositories are hosted on the internet or network
* One repository can have several remotes

#VSLIDE

### List remotes

Showing your remotes

```
git remote
```

Showing remote URLs

```
git remote -v
```

#VSLIDE

### Working with remote repositories

Add remote repository

```
git remote add [shortname] [url]
git remote add test http://mygitserver/test
```

Fetch remote repository

```
git fetch [shortname]
git fetch test
```

> fetch does not merge anything!

#VSLIDE

### Working with remote repositories 2

Pushing to remotes

```
git push [remote-name] [branch-name]
git push origin master
```

Inspecting a remote

```
git remote show [shortname]
git remote show test
```

#VSLIDE

### Working with remote repositories 3

Rename

```
git remote rename test final
```

Remove

```
git remote rm final
```

#HSLIDE

## Workshop

Hands on samples

#HSLIDE

### Local Branch

```
(master): git checkout -b hotfix
(hotfix): git commit -am "Change .... "
(hotfix): git checkout master
(master): git merge hotfix
(master): git push
(master): git branch -d hotfix
```

#HSLIDE

### Rename

* git tracks content, no files
* Automatic detection (add + delete)
* Log does not show renames (default)
* Detection works without `git mv`

#VSLIDE

#### Rename sample

```
echo "test1" > test1.txt
git commit -am "commit 1"
echo "test1+" > test1.txt
git commit -am "commit 2"
ren test1.txt test11.txt
git commit -a am "rename"  // don't forget -a
git log test11.txt
git log --follow test11.txt
```

#VSLIDE

#### Rename tipps

Show renames in log per default
```
git config --global diff.renames true
```

#HSLIDE

## Reference

See [https://git-scm.com/docs](https://git-scm.com/docs "git reference")