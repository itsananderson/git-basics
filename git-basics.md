title: Git Basics
author:
    name: Will Anderson
    twitter: itsananderson
    github: itsananderson
output: index.html
controls: true


--

# Git Basics
## A quick tour through what you need to get started

--

### Overview

* Git is a database of objects
* Each commit is a snapshot of the entire repository
* Branches diverge history of the *entire* repository

--

### Git is a database of objects

* `git clone` downloads the entire database
* Commits, branches, tags, and files are all objects
* Each object is stored with the SHA of its contents as the key
* Objects can be added and removed, but never edited

--

### Each commit is a snapshot of the entire repository

* The state of the entire tree is captured
* Unchanged files stored as a pointer to the previous version
* Changed files are stored as a new snapshot, not a diff
* Commits are immutable. You can copy a commit with modifications, but technically that's a new commit

--

### Branches diverge history of the *entire* repository

* A branch is a pointer to a commit
* When you commit, you're just moving the pointer to the new commit

