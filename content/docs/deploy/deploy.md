---
title: "Deploying the site"
weight: 10
description: ""
---
# Site deployment

## Building the site

To publish your content, you must first build a static site from the source files.

1. If any changes you want to publish are in a working branch, merge that branch into the master branch.
2. In the file explorer, open the project folder.
3. Right-click in the file explorer (not on any file or folder) and select **Open in Terminal**.
4. Check out the master branch by entering `git checkout master`.
5. If the `docs` folder exists, delete it by using the file explorer.  
IMPORTANT: This does **not** apply to the `content/docs/` folder.
1. In the Terminal, enter `hugo`  
**Result:** The static site is built in the `docs` directory.
1. Commit and push the changes to the origin/master branch.
1. Perform one of the following actions:
   - If this is the first time you are deploying the site, proceed to [publishing the site](#publishing-the-site).
   - If the site was published before, no further actions are required.  
   **Tip:** The site may take some time to update. To ensure that you are always browsing the latest version instead of a cached one, use the incognito/private browsing mode of your browser.

## Publishing the site

You only need to perform this procedure the first time you are deploying the site or after un-publishing.

1. Log in to GitHub.
2. Open the homepage of the repository.
3. Select the **Settings** tab.
4. In the menu on the left, ensure that you are in the **Options** page (open by default).
4. Scroll down to the **GitHub Pages** section.
5. In the **Source** drop-down list, select the **master branch /docs folder** option.  
**Result:** Publishing the site from the `docs` folder on the "master" branch begins. Depending on the size of the site, this may take some time.  
By default, the URL of the page is `https://{GitHub user name}.github.io{repository name}`  