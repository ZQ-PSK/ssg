---
title: "GitHub repository"
weight:
description: ""
---
# GitHub repository
## Creating a repository
1. Log in to GitHub.
2. In the menu on the left, click **New**.
3. In the **Repository name** field, enter a meaningful name.  
NOTE: If you host a project site from this repository, the name is part of the URL.
1. **Optional**: In the **Description** field, enter a description.
2. Make the repository public or private by selecting the corresponding radio button.
3. Click **Create repository**.  
**Result** An empty repository is created.
1. Open the Terminal by pressing **`CTRL` + `SHIFT` + `T`**.
2. Navigate to the directory where you want to store the git repository.
**Example**:  
```
marcin@marcin-HP:~$ cd Documents/gitRepositories

```
4. Enter `git clone git@github.com:{your GitHub username}/{your repository name}.git`
5. If prompted to add `github.com` to the list of known hosts, enter `yes`
**Result** The repository is cloned into a new directory, named after the repository. You can now commit files from this location to GitHub.