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

List global configuration:

```
git config --global -l
```

List local configuration:

```
git config -l
```

#VSLIDE

#### Configure Identity

Set global configuration:

```
git config --global user.name "Max Mustermann"
git config --global user.email "m.mustermann@test.com"
```

Set local configuration: 

```
git config user.name "Max Mustermann"
git config user.email "m.mustermann@test.com"
```

#HSLIDE

## Common Commands

#VSLIDE

### Initialize Repository

```
git init
```

### Clone Repository

```
git clone https://github.com/norberteder/git-workshop
```

#VSLIDE

### Add new file

```
git add file-to-add.md
```

### Remove file

```
git rm file-to-delete.md
```

### Commmit changes

```
git commmit -am "Add new feature 1"
```

#HSLIDE

## Workshop

### Local Branch