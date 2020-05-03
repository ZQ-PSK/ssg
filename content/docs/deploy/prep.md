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
4. Add the following line: `relativeURLs = true`  
IMPORTANT: Other Hugo themes may require you to add the `baseURL` variable in order to publish to GitHub pages properly.  
**Example:**  
   ```
   publishDir = "docs"
   languageCode = "en-us"
   title = "Marcin Misiak - writing samples"
   theme = "hugo-book"
   relativeURLs = true
   ```

