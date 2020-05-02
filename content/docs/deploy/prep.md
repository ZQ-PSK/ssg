---
title: "Preparing for GitHub Pages deployment"
weight: 5
description: ""
---
# Configuring Hugo for GitHub Pages deployment

1. In the root folder of your repository, open the `config.toml` file.
2. In the configuration file, search for the `publishDir` setting.
3. Perform one of the following actions:
   - If the setting exists, change its value to `"docs"`
   - If the setting does not exist, create it by adding the following line to the file: `publishDir = "docs"`
4. Change the value of `baseURL` to the URL of your page.  
By default, the URL is `{your username}.github.io/{repository name}`.
IMPORTANT: This setting also affects the URL of the local page published by the `hugo server` command. 
**Example:**  
   ```
   baseURL = "zq-psk.github.io/ssg/"
   publishDir = "docs"
   languageCode = "en-us"
   title = "Marcin Misiak - writing samples"
   theme = "book"
   ```

