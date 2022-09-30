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

## **How to Create a README.MD file**

```
git add README.md
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

## **Restoring a Deleted File**
#### You can restore a file which was accidently deleted with the help of restore command. 

```
PS C:\Users\Admin\Workspace\Git_Github> git status

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)        
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    names.txt
```
#### here in the above example you can see that a file is accidently deleted if you want to get it back you can use restore command. 

```
git restore <FileName>
```
#### Example
```
git restore names.txt
```

## **If you want to Remove a File**

```
git rm -rf <FileName>
```

```
PS C:\Users\Admin\Workspace\Git_Github> git rm .\names.txt
error: the following file has changes staged in the index:
    names.txt
(use --cached to keep the file, or -f to force removal)
PS C:\Users\Admin\Workspace\Git_Github> git rm -rf .\names.txt
rm 'names.txt'

PS C:\Users\Admin\Workspace\Git_Github> git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    names.txt
        modified:   readme.md
```
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

## **Popping Stash**
#### You want to get back all the previous stuff which was at backstage. 

```
git stash pop
```
#### **Other commands for Stash**

```
usage: git stash list [<options>]
   or: git stash show [<options>] [<stash>]
   or: git stash drop [-q|--quiet] [<stash>]
   or: git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
   or: git stash branch <branchname> [<stash>]
   or: git stash clear
   or: git stash [push [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [-m|--message <message>]        
                 [--pathspec-from-file=<file> [--pathspec-file-nul]]
                 [--] [<pathspec>...]]
   or: git stash save [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet] 
                 [-u|--include-untracked] [-a|--all] [<message>]
```

## **Clearing the Stash** 

```
git stash clear
```

## **Starting GitHub**
#### Hosting our project on Github, and share it with other people through out the world. 
#### Steps in order to create a new project and host it on Git

1. **Creating a new repo on Git**
2. **Connecting Remote Repo to Local Repo or or push an existing repository from the command line**

```
git remote add origin <url>

Example:
git remote add origin https://github.com/Mysticalbloomingal/DevOps-BootCamp-Git.git

git: its a basic commands
remote: working with url's 
add: adding a new URL
origin: Name of the url your going to add
```

```
git remote -v

PS C:\Users\Admin\Workspace\Git_Github> git remote -v
origin  https://github.com/Mysticalbloomingal/DevOps-BootCamp-Git.git (fetch)
origin  https://github.com/Mysticalbloomingal/DevOps-BootCamp-Git.git (push)

which means it will display all the url which are attached to the project. 
```
3. **Pushing local changes to remote repository.**
#### push the commits in the local branch named master to the remote named origin
```
git push origin <branch>

Example:

PS C:\Users\Admin\Workspace\Git_Github> git push origin master 
Counting objects: 100% (14/14), done.
Delta compression using up to 8 threads
Compressing objects: 100% (12/12), done.
Total 14 (delta 5), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (5/5), done.
To https://github.com/Mysticalbloomingal/DevOps-BootCamp-Git.git
 * [new branch]      master -> master
```
## **What are branches**
#### A branch in Git is simply a lightweight movable pointer to one of these commits. The default branch name in Git is master . As you start making commits, you're given a master branch that points to the last commit you made. Every time you commit, the master branch pointer moves forward automatically.

## **Use of Branches**
#### When your working on a new feature or resolving a bug always create a seperate branch. 
#### **Note: You should never commit on a main branch**

## **Making a new Branch and Swicthing to it (Learn Branching)**

```
git branch <branch-name>

Example:
PS C:\Users\Admin\Workspace\Git_Github> git branch feature 

Here your already switched to branch name as "Feature"
```
## **Switch to Different Branch**
#### If you want to toggle between the branches, you need to first save your workspace and then toggle or switch between the branches [ **Please commit your changes or stash them before you switch branches** ]


#### **Example 1**
``` 
git checkout <branch-name>

Example:

PS C:\Users\Admin\Workspace\Git_Github> git checkout feature
Switched to branch 'feature'
```
#### **Example 2**

```
git checkout <branch-name>

Example:

PS C:\Users\Admin\Workspace\Git_Github> git checkout master
Switched to branch 'master'
```

## **merging branch to main**

#### Once your code and workstuff is finalized you can merge your code with other users so that everybody can access it

```
git merge <branch-name>

Example:

PS C:\Users\Admin\Workspace\Git_Github> git merge feature
Already up to date.
```
## **Pushing new changes to master branch**
```
git push origin <branch-name>

Example: 
PS C:\Users\Admin\Workspace\Git_Github> git push origin master  
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 347 bytes | 347.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0        
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Mysticalbloomingal/DevOps-BootCamp-Git.git
   78a992c..f694224  master -> master
```

## **Why Fork, and How to Fork?**
#### Forking is a git clone operation executed on a server copy of a projects repo. A Forking Workflow is often used in conjunction with a Git hosting service like Bitbucket.

## **Cloning the Forked project to local**
```
git clone <url>

Example:

PS C:\Users\Admin\Workspace\Git_Github> git clone https://github.com/Mysticalbloomingal/DevOps-Tools-Practics.git
Cloning into 'DevOps-Tools-Practics'...
remote: Enumerating objects: 23, done.
remote: Counting objects: 100% (23/23), done.
remote: Compressing objects: 100% (17/17), done.
remote: Total 23 (delta 1), reused 21 (delta 1), pack-reused 0
Receiving objects: 100% (23/23), 5.62 KiB | 261.00 KiB/s, done.
Resolving deltas: 100% (1/1), done.

Here you can see that after running the command you will get a copy of your project from github to your local system
```

## **What is Upstream and adding it to local**

#### In the git world, upstream refers to the original repo or a branch. For example, when you clone from Github, the remote Github repo is upstream for the cloned local copy.

```
git remote add upstream <url>

Example:
PS C:\Users\Admin\Workspace\Git_Github> git remote add upstream https://github.com/Mysticalbloomingal/sample.git

PS C:\Users\Admin\Workspace\Git_Github> git remote -v
origin  https://github.com/Mysticalbloomingal/DevOps-BootCamp-Git.git (fetch)
origin  https://github.com/Mysticalbloomingal/DevOps-BootCamp-Git.git (push) 
upstream        https://github.com/Mysticalbloomingal/sample.git (fetch)     
upstream        https://github.com/Mysticalbloomingal/sample.git (push)   
```


## **What is a Pull Request?**
#### Pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.

#### Or simply you can say that Pull requests are proposed changes to a repository submitted by a user and accepted or rejected by a repository's collaborators. Like issues, pull requests each have their own discussion forum.

## **Never Commit on Main branch & Creating our first pull request**










