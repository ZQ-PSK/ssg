---
title: "GitHub account"
weight: 10
description: ""
---
# GitHub account

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

1. Open the Terminal by pressing **`CTRL` + `ALT` + `T`**.
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
