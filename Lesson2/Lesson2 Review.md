# Lesson 2: OOP and Version Control Review

Now that you have Git downloaded and cloned the repo we created during the lesson, 
let's review the topics that we touched on during our OOP and version control lesson.

### Object Oriented Programming (OOP)
This is a **programming paradigm** centered around objects. An object has **fields** (or data) and **methods** (or code logic).

An object's fields store what we consider the object's **state**.

A method can access and modify the fields of the object. 

### Version Control
A system that keeps track of changes to files over time, for the purpose of 
accountability, auditing, access, version rollbacks and backups.

Types of version control systems (VCS):
1. Local VCS - stores only differences (patch-sets) in a local database
2. Centralised VCS - stores all files and their versions on a centralised server
3. Distributed VCS - stores all files and their version histories on a server as 
well as on clients' machines

For some handy diagrams on these three VCS, see 
[this link](http://toolsqa.com/git/local-central-and-distributed-version-control-systems/ "ToolsQA Git Tutorial Basics").


### Git
A DVCS that supports non-linear development (Git branching).

A **commit** records changes to your local repository. We need to push the local changes to the remote repository.

A "commit" (colloquially) is a two step process:

1. Staging (preparing a file for a commit)
2. The actual commit

**Staging** allows us to pick exactly which file(s) we want to commit. This is handy in cases where we are done one section 
of work and we want to record the modifications but still have unfinished changes we don't want to track yet.

We can have **tracked** and **untracked** files. Tracked files are the ones that are already in the remote repo, while untracked 
are new files we have added to our local repository that haven't been staged yet. 

### Git commands
* **Clone** a remote repository. Git will download a complete copy of the repository, including its version history.
```text
git clone <remote url>
```
If it is an HTTPS url, credentials must be provided.

* Check the **status** of the local repository. 
```commandline
git status
```

This will show:
 1. What branch you are on (after a clone, this is traditionally the master branch but more about branching later!)
     ```text
    On branch master
    ```
 2. The status of your local branch in comparison to the remote (if a remote is set)
    ```text
    Your branch is ahead of 'origin/master' by 1 commit.
    (use "git push" to publish your local commits)
    
    OR if it is up to date:

    Your branch is up to date with 'origin/master'.

    ```
 3. Which tracked files have been staged for a commit 
      ```text
    Changes to be committed:
    (use "git reset HEAD <file>..." to unstage)

        new file:   Lesson2/Lesson2 Review.md
    ```
 4. Which tracked files have been changed
      ```text
    Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   Lesson2/Lesson2 Review.md
    ```
 5. What untracked files have been added to the project
     ```text
    Untracked files:
    (use "git add <file>..." to include in what will be committed)

        Lesson2/Lesson2 HW.md
    ```
    
* Check the **difference** between the last version and your latest changes
```commandline
git diff
git diff Lesson2/Lesson2 Review.md
git diff --cached Lesson2/Lesson2 HW.md
```
The first command will show all changes to all files.

The second will show all unstaged changes to the specific file.

The third will show all staged changes to the specific file.

* **Add** a file(s) to be **staged**
```commandline
git add Lesson2/Lesson2 Review.md
```

* **Commit** a file, with a message
```commandline
git commit -m "Added the Lesson2 review file."
git commit --amend
```
Always including a descriptive commit message is good practice.
The second command allows you to amend your commit message. (N.B. This is a vim editor)

* **Push** changes 

Update the remote repo branch with your changes.
```commandline
git push
git push -u origin feature/lesson2
```
The first command will push changes to the remote branch (this is already configured when you clone a repo).

The second will set the "upstream" (i.e. the -u flag) of your local branch to point at the remote branch you want to push your commits to.