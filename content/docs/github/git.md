---
title: "Git basics"
weight: 5
description: ""
---
# Git basics
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