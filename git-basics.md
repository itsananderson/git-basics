title: Git Basics
author:
    name: Will Anderson
    twitter: itsananderson
    github: itsananderson
output: output/index.html
controls: true


--

# Git Basics
## A quick tour through what you need to get started

--

### Overview

* Git is a database of objects
* Each commit is a snapshot of the entire repository
* Branches diverge history of the *entire* repository
* Cloning and pulling and pushing OH MY!
* Concepts to understand, coming from TFS
* GitHub Pull Request (PR) demo

--

### Git is a database of objects

* Commits files are examples of objects
* Each object is stored with the SHA of its contents as the key
* Objects can be added and removed, but never edited

--

### Each commit is a snapshot of the entire repository

* The state of the entire tree is captured
* Unchanged files stored as a pointer to the previous version
* Changed files are stored as a new snapshot, not a diff
* Commits are immutable. You can copy a commit with modifications, but technically that&#39;s a new commit

--

### Branches diverge history of the *entire* repository

* A branch is a pointer to a commit
* When you commit, you&#39;re just moving the pointer to the new commit

--

### Cloning and pulling and pushing OH MY!

* `git clone` downloads the entire history
* `git pull` fetches changes from the server, and merges them with the local history
* `git push` sends the local changes to the server
* `git fetch` downloads changes from the server, but doesn&#39;t merge them with the current branch
* `git merge` merges changes between two branches.

`git pull` is like doing `git fetch` followed by `git merge`

--

### Concepts to understand, coming from TFS

* Branches diverge the entire history, and can&#39;t be "enlisted" piecemeal
* Most actions happen without talking to the server
  * **Local** - commit, checkout, merge, log
  * **Server** - clone, push, pull
* Most branches are short-lived and feature specific. Merge with `master` and remove branch when feature is complete
* Because you download the entire history, only check in sources. No binaries

--

### GitHub Pull Request (PR) demo

http://github.com/itsananderson/github-pr-demo
