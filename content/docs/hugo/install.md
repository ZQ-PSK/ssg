---
title: "Installing Hugo"
weight: 5
description: ""
---
# Installing Hugo on Ubuntu
Hugo offers a few installation methods. The method described in this procedure lets you control the version you are installing and installs it globally.  

1. Go to the [Hugo releases page](https://github.com/gohugoio/hugo/releases).
2. Choose a release :
   - If you are preparing to create a new site, choose the latest release.
   - If you are going to work with an existing site, on the list locate the same release that the site is deployed with.
3. In the **Assets** section of the release, locate the installation file for your operating system.
**Example**: `hugo_extended_x.y.z_Linux-64bit.tar.gz` is compatible with 64-bit Ubuntu.
NOTE: The extended version is required if you need to process SCSS or SASS files.
4. Click the file.
5. In the dialog window that opens, select the **Save file** radio button and click **OK**.
6. In the file explorer, open the directory where the file was saved.
7. Right-click the downloaded file and select **Extract here**.  
   The files are extracted to a new directory named after the `.tar.gz` file, for example `hugo_0.69.2_Linux-64bit`.
8. Right-click the directory where the files were extracted and select **Open in Terminal**.  
**Result**: A Terminal window opens, with the extracted directory set as the working directory.
1. In the Terminal window that opens, enter `sudo mv hugo /usr/local/bin`
2. Enter your password.
3. To verify that Hugo was installed globally, perform the following actions:
   1. Enter `cd ~`
   2. Enter `hugo version`
   **Result**: If Hugo was installed successfully, the output lists the version, for example:  
```
marcin@marcin-HP:~$ hugo version
Hugo Static Site Generator v0.69.2-EC9DCF30/extended linux/amd64 BuildDate: 2020-04-24T07:57:53Z
marcin@marcin-HP:~$ 
```