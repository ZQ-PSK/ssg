---
title: "Hugo"
weight: 1
---
# Hugo Static Site Generator

## Installing Hugo on Ubuntu
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

## Initializing a site

1. Open the Terminal by pressing **`CTRL` + `SHIFT` + `T`**.
2. Navigate to the parent directory of your repository.  
**Example**
```
marcin@marcin-HP:~$ cd Documents/gitRepositories

```
3. Verify that the repository catalog exists.  
**Example**
```
marcin@marcin-HP:~/Documents/gitRepositories$ ls
myRepository

```
1. Enter `hugo new site {repository dir}`  
**Example**: `hugo new site myRepository`
**Result**: An empty site is created.
5. To serve the site on your machine, perform the following steps:
   1. Enter `cd {repository dir}`
   2. Enter `hugo server`
   **Result**: By default, the site is available at [http://localhost:1313/](http://localhost:1313/).  Initially, the site has no content and you can only see a blank page.
   If another site is running locally under port 1313, Hugo automatically selects a different port. You can find the current address in the output of the `hugo server` command:  
```
...
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:45353/ (bind address 127.0.0.1)
Press Ctrl+C to stop
...
```
    3. Return to the Terminal window and stop the site by pressing **`CTRL` + `C`**.

## Adding a theme
To give your website a layout, you must add a theme. The procedure explains how to download a theme and make it a part of your repository, so you can make modifications without affecting the original theme.

1. Go to the [Hugo themes site](https://themes.gohugo.io/).
2. Browse the list of themes.  
This page uses the [book theme](https://themes.gohugo.io/hugo-book/).
3. Go the GitHub page of the theme's repository.
4. Click **Clone or download**.
5. Click **Download ZIP**.
6. Save the file to your local drive.
7. Extract the files.
8. In your repository, in the `themes/` folder, create a folder named after the theme.
9. Copy the extracted files into the theme folder.
10. In the root folder of the repository, open the `config.toml` file.
11. In the configuration file, add the following line:  
```
theme = "{theme name}
```
**Example:**
```
baseURL = "http://example.org/"
languageCode = "en-us"
title = "My New Hugo Site"
theme = "book"
```
12. Verify that the theme was added successfully:
    1. Open the Terminal by pressing **`CTRL` + `SHIFT` + `T`**.
    2. Navigate to your repository.  
    **Example:** `cd Documents/myRepository`
    3. Enter `hugo server`.  
    **Result**: Your page is available [locally](http://localhost:1313/) as an empty site with no content. Some elements of the theme should be visible.

## Adding content