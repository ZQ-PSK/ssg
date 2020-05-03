---
title: "Reviewing the output"
weight:
description: ""
---
# Reviewing the output

Before publishing your site to GitHub Pages, you should review the output locally. GitHub Pages do not provide an on-line staging environment and the static site pushed to "origin/master" is published immediately.

## Hosting the preview

1. Open the Terminal by pressing **`CTRL` + `ALT` + `T`**.
2. Navigate to the root folder of your repository.
3. Enter `hugo server`.  
**Result**: The site is hosted locally on your system. By default, the site is available at [http://localhost:1313/](http://localhost:1313/). 
If another site is running locally under port 1313, Hugo automatically selects a different port. You can find the current address in the output of the `hugo server` command:
   ```
   Web Server is available at http://localhost:45353/ (bind address 127.0.0.1)
   ```
   If you already completed [configuration for GitHub pages](/docs/deploy/prep), the localhost URL includes your repository name, for example `http://localhost:1313/ssg/`.

## Review considerations

Markdown requires precise application of spaces and line breaks.  
When reviewing content, pay special attention to:
- code block formatting.
- list numbering issues.
- line breaks.
- line spacing (may be broken due to redundant line breaks)
- non-working links

The live preview served at `localhost` helps you to make corrections faster, but is not perfect.  
If you make a change that should fix a problem and the output is still wrong, try restarting the preview.