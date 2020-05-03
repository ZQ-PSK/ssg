---
title: "Themes"
weight: 15
description: "Hugo offers a number of free ready-to-use themes"
---
# Themes
To give your website a graphical layout, you must add a theme.

You can also create your own theme from scratch. This requires knowledge of HTML, CSS, JS, and Hugo templating.

## Adding a theme
This procedure explains how to download a theme and use it without connection to the theme's original repository. This allows you to easily introduce your own modifications or update the theme at your own pace.  
**IMPORTANT:** Before making any changes to a theme, verify that the license allows it and to what extent. License information is available on the theme's homepage.

1. Go to the [Hugo themes site](https://themes.gohugo.io/).
2. From the list, select a theme.
This page uses the [book theme](https://themes.gohugo.io/hugo-book/).
1. Go the GitHub page of the theme's repository.
2. Click **Clone or download**.
3. Click **Download ZIP**.
4. Save the file to your local drive (not to your project folder).
5. Extract the files.
6. In your project folder, in the `themes` folder, create a folder named after the theme.
7. Copy the extracted files into the theme folder you created.
8. In the project folder, open the `config.toml` file.
9. In the `config.toml` file, add the following line:  
```
theme = "{theme folder name}"
```
**Example:**
```
baseURL = "http://example.org/"
languageCode = "en-us"
title = "My New Hugo Site"
theme = "book"
```
12. Verify that the theme was added successfully:
    1. Open the Terminal by pressing **`CTRL` + `ALT` + `T`**.
    2. Navigate to your repository.  
    **Example:** `cd Documents/myRepository`
    3. Enter `hugo server`.  
    **Result**: Your page is available [locally](http://localhost:1313/) as an empty site with no content. Some elements of the theme should be visible.

## Theme-specific features
Most themes provide custom shortcodes, partials, and configuration options. Information about those features is usually available on the theme's homepage or its `README.md` file.
