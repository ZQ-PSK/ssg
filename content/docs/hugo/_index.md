---
title: "Hugo"
weight: 5
---
# Hugo Static Site Generator

## Adding a theme
To give your website a layout, you must add a theme. The procedure explains how to download a theme and make it a part of your repository, so you can make modifications without affecting the original theme.

1. Go to the [Hugo themes site](https://themes.gohugo.io/).
2. Browse the list of themes.  
This page uses the [book theme](https://themes.gohugo.io/hugo-book/).
3. Go the GitHub page of the theme's repository.
4. Click **Clone or download**.
5. Click **Download ZIP**.
6. Save the file to your local drive.
7. Extract the files.
8. In your repository, in the `themes/` folder, create a folder named after the theme.
9. Copy the extracted files into the theme folder.
10. In the root folder of the repository, open the `config.toml` file.
11. In the configuration file, add the following line:  
```
theme = "{theme name}
```
**Example:**
```
baseURL = "http://example.org/"
languageCode = "en-us"
title = "My New Hugo Site"
theme = "book"
```
12. Verify that the theme was added successfully:
    1. Open the Terminal by pressing **`CTRL` + `SHIFT` + `T`**.
    2. Navigate to your repository.  
    **Example:** `cd Documents/myRepository`
    3. Enter `hugo server`.  
    **Result**: Your page is available [locally](http://localhost:1313/) as an empty site with no content. Some elements of the theme should be visible.

## Adding content