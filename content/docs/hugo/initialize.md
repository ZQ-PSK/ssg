---
title: "Initializing a site"
weight: 10
description: "Create a 'skeleton' site as a basis for further work"
---
# Initializing a site
Before you can add styling and content to a site, you must initialize a folder structure and configuration files.

1. In the file explorer, create a folder for your project.  
**NOTE:** Whenever this page mentions *project folder*, it refers to this folder.
3. Open the Terminal by pressing **`CTRL` + `ALT` + `T`**.
4. Navigate to the project folder by using the `cd` command.  
**Example:**
   ```
   marcin@marcin-HP:~$ cd Documents/gitRepositories/myHugoSite
   ```
1. Enter `hugo new site .`  
**Result**: An empty site is created.
1. To serve the site on your machine, perform the following steps:
   1. Enter `cd {project folder}`
   2. Enter `hugo server`  
   **Result**: By default, the site is available at [http://localhost:1313/](http://localhost:1313/).  
   Initially, the site has no content and you can only see a blank page.
   If another site is running locally under port 1313, Hugo automatically selects a different port. You can find the current address in the output of the `hugo server` command:  
      ```
      ...
      Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
      Web Server is available at http://localhost:45353/ (bind address 127.0.0.1)
      Press Ctrl+C to stop
      ...
      ```
   1. Return to the Terminal window and stop the local server by pressing **`CTRL` + `C`**.