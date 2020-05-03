---
title: "Preparing for GitHub Pages deployment"
weight: 5
description: "GitHub Pages requires some initial configuration from the static site generator"
---
# Configuring Hugo for GitHub Pages deployment

GitHub Pages requires some initial configuration from the static site generator.

1. In the project folder, open the `config.toml` file.
2. In the configuration file, search for the `publishDir` setting.
3. Perform one of the following actions:
   - If the setting exists, change its value to `"docs"`
   - If the setting does not exist, create it by adding the following line to the file: `publishDir = "docs"`
4. If the `relativeURLs` key exists and is set to `true`, set it to `false`.
5. Add the following key-value pair: `canonifyURLs = true`
6. Add the following key-value pair: `baseURL = "https://{your GitHub username}.github.io/{repository name}/`  
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
**IMPORTANT:** The configuration file affects the local URL when using the `hugo server` command. The localhost URL is shown in the output of the command:
```
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ssg/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```