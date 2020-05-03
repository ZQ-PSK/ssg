---
title: "Troubleshooting GitHub Pages"
weight: 25
description: ""
---
# Troubleshooting GitHub Pages

This is a list of issues which I encountered when deploying this site to GitHub pages.  
The solutions may not be the most effective or the only possible ones.  


## Problem: styling is not applied to the site
**Solution:**  
Verify that your config file includes these lines:  
```
canonifyURLs = true
baseURL = "https://{your GitHub username}.github.io/{your repository name}/"
```

## Problem: relative links to articles do not work
**Solution:**  
Verify that your config file includes these lines:  
```
canonifyURLs = true
baseURL = "https://{your GitHub username}.github.io/{your repository name}/"
```

## Problem: images are not displayed
**Solution:** 
1. Verify that your config file includes these lines:  
   ```
   canonifyURLs = true
   baseURL = "https://{your GitHub username}.github.io/{your repository name}/"
   ```
1. Store the images in a designated folder inside the `content` folder where your store your sources.
2. Use absolute linking to images.  
**Example:** `![A fragment of a table of contents](/images/weightexample.png)  `