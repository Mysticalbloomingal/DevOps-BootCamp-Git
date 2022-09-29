# **Git & Github from Beginners Level**
## **Introduction**
#### It will help you with using Git & GitHub for your personal projects and contributing to Open Source, with no prerequisites, in an easy to understand language.It starts from the very basics of Git & GitHub, covering all the essential commands, including concepts such as branching, pull requests, forking, etc. We also cover other concepts such as squashing, resolving merge conflicts, keeping your code in sync, and more.

---

## **Downloading Git**

#### This is the site in order to [download Git](https://git-scm.com/downloads)

## **Checking the git Version**

```
git -v
```

## **Seeking help**

```
git --help
```

##  **Initializing a Git Repository**
#### Create an empty Git repository or reinitialize an existing one 

```
git init
```
## **Making the first Change**
#### Changes made in the project and are not currently saved or simply say Show the working tree status 

```
git status
```

## **Staging the first change**
#### History is not been saved in the project or are not tracked, here "." represents everything in the current directory or in simple words Add file contents to the index. 

```
git add .
```
#### **Check again whether the untracked files are tracked now or not**
```
git status
```
#### **This shows how we get the output**
```
PS C:\Users\Admin\Workspace\Git_Github> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   ansible.yml
        new file:   hosts
        new file:   readme.md

```
#### **Commiting the First change**
```
git commit -m "Making the first change"
```
#### **Check again if there are any files modified or untracked**
```
git status
```

#### **Removing changes from stage or simply say Restore working tree files**
```
git restore --staged <filename>
            OR
git restore --staged <filename or . for current dir>
```
#### **Check if the files are now back to original state of modifying**
```
git status
```
#### **Viewing the overall history of your project or Show commit logs**
```
git log
```
```
PS C:\Users\Admin\Workspace\Git_Github> git log
commit 44579da8310053c66d2d05d49721773f1bea7d92 (HEAD -> master)
Author: Bhakti Vora <bhakti20150@gmail.com>
Date:   Thu Sep 29 13:35:20 2022 +0530

    Commiting the first change
```

#### **Removing a commit from the history of a project**
```
PS C:\Users\Admin\Workspace\Git_Github> git log
commit 44579da8310053c66d2d05d49721773f1bea7d92 (HEAD -> master)
Author: Bhakti Vora <bhakti20150@gmail.com>
Date:   Thu Sep 29 13:35:20 2022 +0530

    Commiting the first change
```

```
git reset 44579da8310053c66d2d05d49721773f1bea7d92
```
#### here "44579da8310053c66d2d05d49721773f1bea7d92" represents the commit ID after hitting the command it will go to the previous commit change and erase all the before commits. 

#### **Recheck by hitting the log command**
```
git log
```
#### **Recheck by hitting the status command**
```
git status
```
```
PS C:\Users\Admin\Workspace\Git_Github> git status 
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   readme.md

no changes added to commit (use "git add" and/or "git commit -a")
```

#### Here the files are back to the previous changes done earlier. 

## **Stashing Changes**
#### Whenever you work on something you want to save your changes without making any commit without making any history in a project and whenever i need that project or work i can get it back on my workspace. 

```
git stash

PS C:\Users\Admin\Workspace\Git_Github> git stash
Saved working directory and index state WIP on master: 400294f Just a sample file created
PS C:\Users\Admin\Workspace\Git_Github> git status
On branch master
nothing to commit, working tree clean
```





