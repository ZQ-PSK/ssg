---
title: "Deploying the site"
weight: 10
description: ""
---
# Site deployment

## Building the site

1. In the file explorer, open the root folder of your repository.
2. If the `docs` folder exists, delete it.  
IMPORTANT: This does **not** apply to the `content/docs/` folder.
3. Right-click 
1. Enter `hugo`  
**Result:** The static site is built in the `docs` directory.
1. Commit the changes in the `docs` directory.
2. Perform one of the following actions:
   - If you are working on the "master" branch, push to "origin/master".
   - If you are working on another branch, merge the changes into "origin/master".

# Publishing the site
1. Log in to GitHub.
2. Open the homepage of the repository.
3. Select the **Settings** tab.
4. In the menu on the left, ensure that you are in the **Options** page (open by default).
4. Scroll down to the **GitHub Pages** section.
5. In the **Source** drop-down list, select the **master branch /docs folder** option.
**Result:** Publishing the site from the `docs` folder on the "master" branch begins. Depending on the size of the site, this may take some time.  
By default, the URL of the page is `https://{GitHub user name}.github.io{repository name}`