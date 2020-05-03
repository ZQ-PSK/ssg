---
title: "Content enrichment"
weight: 10
description: ""
---
# Content enrichment
You can enrich your content by using shortcodes or inserting HTML into the Markdown file.

## Shortcodes
Hugo offers a number of built-in shortcodes. Themes usually add additional shortcodes you can use. You can also create your own.

Shortcodes are processed when the Markdown sources are parsed into HTML.  

A full list of the built-in shortcodes is available in the [Hugo documentation](https://gohugo.io/content-management/shortcodes/#use-hugos-built-in-shortcodes).

The shortcodes added by a theme are usually described in the theme's `README.md` file.

### Using shortcodes

1. Open a Markdown file.
2. Insert a shortcode.  
**NOTE:** The example is provided as a screenshot, because a shortcode cannot be included as a code snippet without creating another shortcode to make this possible.  
**Example:** the `youtube` shortcode, with the video ID as a parameter.  
![Screenshot of a Markdown source file with a shortcode](/images/shortcode.png) 
**Result:** the video player is embedded in the site:
{{< youtube dQw4w9WgXcQ >}}

### Creating shortcodes
You can create your own shortcodes. This procedure presents an example of creating a simple shortcode that changes the color of a fragment of text {{< color >}}red and makes it bold{{< /color >}}.

1. In the file explorer, navigate to `{project folder}/themes/{theme name}/layouts/shortcodes`
2. In the `shortcodes` folder, create a new file named `color.html`
The name should be meaningful. It is used to call the shortcode in the Markdown files. It cannot contain any spaces.
5. Open the file.
6. In the file, add the following code:  
   ```
   <span style="color:red"><strong>{{ .Inner }}</strong></span>
   ```  
   **Explanation:** The shortcode takes a fragment of plain text included in the code that called it and encases it with HTML markup.
7. Save the file.
8. Try using the shortcode in practice.  
**Example:** {{< color >}}The shortcode is used to color the text you are reading now.{{< /color >}}  
![Screenshot showing a fragment of text colored with the color shortcode](/images/shortcodeexample.png)

For more information on creating shortcodes and the available functions and variables, refer to the [Hugo documentation](https://gohugo.io/templates/shortcode-templates/).

## Raw HTML
<span style="color:red"><strong>You can include raw HTML markup in the Markdown files.</strong></span>

To achieve the same result as in the [shortcode created earlier](#creating-shortcodes), you can do this:
```
<span style="color:red"><strong>You can include raw HTML markup in the Markdown files.</strong></span>
```
**NOTE:** If the code does not work, you need to [enable raw HTML in Hugo configuration](#enabling-raw-html).

### Enabling raw HTML
1. In the file explorer, open the project folder.
2. Open the `config.toml` file.
3. Add the following lines:  
```
[markup]
    [markup.goldmark]
        [markup.goldmark.renderer]
            unsafe = true
```