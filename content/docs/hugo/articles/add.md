---
title: "Adding articles"
weight: 5
description: "Add new content to your page"
---
# Adding articles
1. In the project folder, open the content folder.  
By default, the folder is `content`. The "book" theme uses the `content/docs` folder.
2. Create a new Markdown file in the location where you want to add an article.  
For more information on content organization, read [this article](/docs/hugo/articles/#content-organization).
1. Open the new file with a text editor.
2. At the beginning of the file, add the following metadata:
   - `title` (string)
   - `weight` (integer)
   - `description` (string)
   - **optional:** other metadata that your site uses

**Example:**  
```
---
title: "Content"
weight: 20
description: "Short description"
customParam: "string"
customArrayParam:
    - "string"
    - "string"
---
```
5. After the metadata block, add the Markdown content.
6. Save the file.
7. Verify that the output is correct.  
See [Reviewing the output](/docs/hugo/articles/review).