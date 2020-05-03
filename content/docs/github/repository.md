---
title: "GitHub repository"
weight: 15
description: "Create a repository to store your work"
---
# GitHub repository
After your content is uploaded to a GitHub repository, you can start versioning your source files and keeping a history of changes.

Before you continue, ensure that you [installed Git](/docs/github/git/#installing-git).

## Creating a repository
1. Log in to GitHub.
2. In the menu on the left, click **New**.
3. In the **Repository name** field, enter a meaningful name.  
NOTE: If you host a project site from this repository, the name is part of the URL.
1. **Optional:** In the **Description** field, enter a description.
2. Make the repository public or private by selecting the corresponding radio button.
3. Click **Create repository**.  
**Result** An empty repository is created.
1. Open the Terminal by pressing **`CTRL` + `ALT` + `T`**.
2. Navigate to the directory where you want to store the Git repository.
**Example:**  
```
marcin@marcin-HP:~$ cd Documents/gitRepositories

```
4. Enter `git clone git@github.com:{your GitHub username}/{your repository name}.git`
5. If prompted to add `github.com` to the list of known hosts, enter `yes`
**Result** The repository is cloned into a new directory, named after the repository. You can now commit files from this location to GitHub.

## Committing to the repository
Your repository is empty. As your first commit, you can add the `readme.md` file.

1. Open a text editor.
2. Create a Markdown file with some content.  
**Example:**
    ```
    # Marcin's repository

    This is the repository for my personal GitHub site.
    ```
5. Save the file in the repository folder as `readme.md`
1. Open the Terminal by pressing **`CTRL` + `ALT` + `T`**.
2. Navigate to the repository folder by using the `cd` command.  
**Example:** `cd Documents/repositories/myRepository`
5. To verify that you are in the correct folder and on the correct branch, enter `git status`  
**Expected output:**  
   ```
   On branch master

   No commits yet

   Untracked files:
     (use "git add <file>..." to include in what will be committed)
   	readme.md

   nothing added to commit but untracked files present (use "git add" to track)
   ```
1. Add (stage) the change in the `readme.md` file by entering `add readme.md`
2. Verify that the file is staged by entering `git status`  
**Expected output:**  
   ```
   On branch master

   No commits yet

   Changes to be committed:
     (use "git rm --cached <file>..." to unstage)
   	new file:   readme.md
   ```
3. Commit the changes by entering `git commit --message="My first commit"`  
**Result:** The changes are committed. The output provides a summary of the changes and some additional information, such as the commit's hashId.
4. Push the changes to origin by entering `git push`
5. Log in to GitHub and open your repository.
6. Verify that the `readme.md` was added to the repository.

## Moving your project folder to the repository
Your repository is ready to use. It is time to upload your project folder to GitHub and start keeping track of your work.

1. In the file explorer, open your project folder.
2. Select all the files.
3. Copy the files to clipboard.
4. Open your repository folder.
5. Paste the files from your clipboard.
6. Right-click in the folder (not on any file or folder) and select **Open in Terminal**.
7. In the terminal, enter `git status`  
**Expected output:** Depending on your previous work with the project folder, the list of files and folders may differ slightly.
   ```
   On branch master
   Your branch is up to date with 'origin/master'.

   Untracked files:
     (use "git add <file>..." to include in what will be committed)
   	config.toml
   	content/
   	resources/
   	themes/

   nothing added to commit but untracked files present (use "git add" to track)
   ```
10. Add all files by entering `git add *`
11. Commit the changes by entering `git commit --message="Uploaded the Hugo project"`
4. Push the changes to origin by entering `git push`
**Result:** your project is uploaded to GitHub. From now on, when mentioning the *project folder*, this guide refers to the folder with the repository. The previous project folder is obsoleted.

## Committing and pushing further changes
When you make more changes to files, you should commit them in order to build a change history.

1. Open the Terminal by pressing **`CTRL` + `ALT` + `T`**.
2. Navigate to the repository folder by using the `cd` command.  
**Example:** `cd Documents/repositories/myRepository`
3. Check for new, modified, or removed files by entering `git status`.
4. If the output says that your local branch is a number of commits behind origin, enter `git pull`
5. Stage all added files by entering `git add *`
6. Stage all file modifications and deletions by entering `git add -u`
7.  Commit the changes by entering `git commit --message="{meaningful message}"`
8.  Push the changes to origin by entering `git push`

**Tip:** To simplify your work with Git, install a Git plugin for your text editor or a standalone application such as SourceTree.