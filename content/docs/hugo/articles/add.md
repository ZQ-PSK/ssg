---
title: "Adding articles"
weight: 5
description: ""
---
# Adding articles
1. Open the `content/docs` folder.
2. Create a new Markdown file.  
The name of the file will be visible in the URL of the article.
3. Open the new file with a text editor.
4. At the beginning of the file, add the following metadata:
   - `title` (string)
   - `weight` (integer)
   - `description` (string)
   - **optional**: other metadata that your site uses

**Example**:  
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
