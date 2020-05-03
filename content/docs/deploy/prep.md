---
title: "Preparing for GitHub Pages deployment"
weight: 5
description: ""
---
# Configuring Hugo for GitHub Pages deployment

1. In the root folder of your repository, open the production configuration file.
2. In the configuration file, search for the `publishDir` setting.
3. Perform one of the following actions:
   - If the setting exists, change its value to `"docs"`
   - If the setting does not exist, create it by adding the following line to the file: `publishDir = "docs"`
4. If the `relativeURLs` value exists and is set to `true`, set it to `false`.
5. Add the following line: `canonifyURLs = true`
6. Add the following line: `baseURL = "https://{your GitHub username}.github.io/{repository name}/`  
**Example:**  
   ```
   publishDir = "docs"
   languageCode = "en-us"
   title = "Hugo on GitHub Pages"
   theme = "hugo-book"
   canonifyURLs = true
   baseURL = "https://zq-psk.github.io/ssg/"
   ```
**Result:** The page is configured for GitHub pages deployment.  
**IMPORTANT:** The configuration file affects the local URL when using the `hugo server` command.