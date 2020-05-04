---
title: "Git basics"
weight: 5
description: "The basic concepts needed to understand Git"
---
# Git basics
## What is Git?
Git is a distributed version control system. It is free, open source, and popular with software developers worldwide.  

Git stores information about incremental changes, which means you can see and compare how a file changed over a long period of time, and control what is included in the production environment.

Git is a powerful and complex tool. This article covers only the most basic concepts needed to perform simple operations within your own repository. If you want to use Git on a regular basis or in a professional environment, you should complete a more comprehensive tutorial.

### Git glossary
Here are the explanations of the basic terms you need to know to understand Git.
#### Repository
A repository is the central element of a Git-controlled project. It stores all the data: files, branches, history, and so on.
#### Branch
By default, a repository only includes a *master* branch which stores the files released into production. When you're working on a personal project and learning to use Git, you do not need to create any other branches.  

Additional branches (in this guide, they are called working branches, but the nomenclature differs depending on the applied work methodology) may be created from the master branch (or other working branches) at any time to work on different features of a project. Development work can be in progress on many branches at the same time.

When the work is complete, the commits from the branch are merged into the master branch.

You can create local branches and never push them to origin. This can be useful for testing purposes.
#### Origin
The *origin* branches are the branches stored in the original remote repository (in the case of this site, the remote repository is stored in the GitHub cloud service).
#### Local
When you want to work on a your computer, you create a local counterpart of an origin branch. Changes made on local branches must be *pushed* to the origin counterparts of those branches. If you do not do that, the changes remain visible only on your hard drive.

It is also possible to create a local branch first and then push it to the remote repository, creating an origin branch in the process.
#### Cloning
The operation that downloads a repository from the cloud to your local drive so you can work with the files on your own computer before pushing them to origin.
#### Checkout
When you check out a branch, you set it as your current working branch. Such a branch can also be called the active branch. Commits, pushes, and other operations are performed on the active branch.

Checking out can also be used to create a new local branch.
#### Commit
A commit can be understood as saving your work to the branch you are currently working on (most of the time, it is a local branch). As the name implies, you are making a commitment, informing Git that the changes are final.  
Cancelling a commit is much more difficult than reverting the changes in a text editor.  
When committing, you can choose some of the files you modified, or add all of them to the commit.  
Commits can be made with a message. It is good practice to add meaningful, short commit messages.  
You can make a series of commits locally before pushing your work to the cloud.
#### Staged changes
Staged changes are changes that are included in the commit at the time the commit is made. You can add all changes to a commit or pick only some of them.

Changes are added on a file-by-file basis. You cannot stage only a part of the changes made to a particular file.
#### Push
Pushing means uploading the commits from your local branch to its origin counterpart.

When you push a branch that does not have an origin counterpart, you can create the counterpart in the process.
#### Pull
Pulling means downloading the changes from the origin branch to its local counterpart. This is done to keep a branch up-to-date if commits were made to the branch from another system since you cloned it to your local drive. The changes could be made by another contributor or by you, from another computer.
#### Merge
A merge transfers the commits form one branch to another. Merges are usually done into the master branch, but you can also merge working branches into one another.

Another common use is merging the master branch into the working branch in order to keep the working branch up-to-date with the latest production changes.
#### Pull request
When you want to merge the changes from a *source branch* (the working branch) into a *target* branch (usually master), you can do it by creating a *pull request*.

A pull request lets you compare the changes that will be introduced into the target branch when merging. It may be configured so that it requires a review and acceptance from someone. After a pull request is made, you can still work on the files on the source branch and make changes according to comments made in the pull request.

Repositories are often configure so that a pull request is the only way to introduce changes to the master branch.
### Git workflow example

A simple example of how Git may be used:
1. Marcin clones a repository to his local drive.
2. He creates a new branch locally or checks out an existing branch.
3. He makes changes to some files.
4. He stages the changes.
5. He commits the changes the the local branch.
6. He pushes the commits to the origin branch.
7. Using the GitHub GUI, he creates a pull request.
8. Marcin's teammates review the pull request and submit their approvals.
9. Marcin accepts the pull request and the changes are merged into the master branch.
10. The content of the master branch is published to production, making it available to the clients.
11. Marcin deletes the working branch from local and origin.
12. When he wants to introduce more changes, Marcin creates a new branch for that work.

## Git GUIs
Git can be used entirely from the Terminal, but to make your work easier, you can use GUIs such as SourceTree or text editor plugins.  
**Note:** To use the GUIs effectively, you must understand the basic concepts of Git first, even if you plan to never use Git in the Terminal.

## Installing Git
Before you can start using Git, you need to install it in your system.

1. Open the Terminal by pressing **`CTRL` + `ALT` + `T`**.
1. Check if git is installed by entering `git --version`
2. Perform one of the following actions:
   - If the output displays a version number, no further actions are required.
   - If the output say the `git` command was not found, install Git by performing the following actions:
     1. Enter `sudo apt install git`. 
     2. If prompted, enter the password.
     3. When asked if you want to continue, enter `y`
     **Result:** Git is downloaded and installed. Required dependencies are installed automatically.
3. Set your Git credentials by performing the following steps:
   1. Enter `git config --global user.email "{your email}"`
   2. Enter `git config --global user.name "{your name}"`
