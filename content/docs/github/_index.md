---
title: "GitHub"
weight:
description: ""
---
# Introduction
Assumes the use of Ubuntu.

# GitHub

## Creating a GitHub account
A free GitHub account lets you access the basic features.

1. Go to [https://github.com/](https://github.com/).
2. Fill in the following fields:
    - **Username**
    - **Email**
    - **Password**  
3. Click **Sign up for GitHub**.
4. In the page that opens, perform the following actions:
   1. Click **Verify**.  
   A puzzle appears.
   1. Solve the puzzle according to the instructions on the screen.
   2. Click **Join a free plan**.
   **Result**: A page opens, asking for more information about your work profile.
5. **Optional**: Provide the information.
6. Click **Complete**.  
**Result:**: GitHub sends a verification email to the address you provided earlier.
1. In the email, click **Verify email address**.
**Result**: The verification page opens.
8. If prompted, log in to GitHub.  
**Result**: Your account is verified.
9. In the page that opens, ignore the tutorials by clicking **Skip this for now**.

**Result**: Your GitHub account is ready to use.

## Adding an SSH key to GitHub
An SSH key is necessary to authorize git requests sent from your local machine to GitHub.

1. Open the Terminal by pressing **`CTRL` + `SHIFT` + `T`**.
2. Check for existing keys by entering `ls -al ~/.ssh`  
3. Perform one of the following actions:
   - If the output says that the `~/.ssh` directory does not exist, proceed to the next step.
   - If the output lists any `.pub` files, but you do **not** want to use any of those keys with GitHub, proceed to the next step.
   - If the output lists any `.pub` files and you want to use one of those keys with GitHub, skip to step X.
4. Generate a new key by performing the following actions:
   1. Enter `$ ssh-keygen -t rsa -b 4096 -C "{your_email@example.com}"`  
    where `{your_email@example.com}` is the email address you used to create your GitHub account.  
   1. When prompted to enter the file in which to save the key, perform one of the following actions:
      - To accept the default location, press **`ENTER`**.
      - To change the location, enter the new location.
   2. When prompted to enter a passphrase, perform one of the following actions:
      - To use a passphrase, enter and repeat the passphrase.
      - To save the key without a passphrase, press **`ENTER`**.
      **Result**: The key is saved to a file.
5. Add your private key to the ssh-agent by performing the following actions:
   1. Enter `eval "$(ssh-agent -s)"`  
   **Result**: The ssh-agent starts running in the background.
   2. Enter `ssh-add {path to private key file}`  
   TIP: The default path is `~/.ssh/id_rsa`
   **Example**: `ssh-add ~/.ssh/id_rsa`
   3. If prompted, enter the passphrase.
6. Copy the SSH key to the clipboard by performing the following actions:
   1. Enter `gedit <path to public key file>`  
   TIP: The default path is `~/.ssh/id_rsa.pub`
   2. From the text editor window that opens, copy all the contents into the clipboard.
   3. Close the text editor.
7. Log in to GitHub.
8. Go to [the profile settings page](https://github.com/settings/profile).
9.  In the menu on the left, click **SSH and GPG keys**.
10. In the upper-right corner, click **New SSH key**.
11. In the **Title** field, enter a meaningful name for the key.  
   **Example**: `John's personal laptop`
12. In the **Key** field, paste the public SSH key.
13. Click **Add SSH key**.
14. Enter your GitHub password.
**Result**: The system is authorized to perform git operations on your GitHub account.

## Installing git

1. Open the Terminal by pressing **`CTRL` + `SHIFT` + `T`**.
1. Check if git is installed by entering `git --version`
2. Perform one of the following actions:
   - If the output displays a version number, no further actions are required.
   - If the output say the `git` command was not found, install git by performing the following actions:
     1. Enter `sudo apt install git`. 
     2. If prompted, enter the password.
     3. When asked if you want to continue, enter `y`
     **Result:** git is downloaded and installed. Required dependencies are installed automatically.
3. Set your git credentials by performing the following steps:
   1. Enter `git config --global user.email "{your email}"`
   2. Enter `git config --global user.name "{your name}`

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