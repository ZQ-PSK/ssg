---
title: "Initializing a site"
weight: 10
description: ""
---
# Initializing a site

1. Open the Terminal by pressing **`CTRL` + `ALT` + `T`**.
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