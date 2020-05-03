---
title: "Hugo"
weight: 5
---
# Hugo Static Site Generator

## What is Hugo?

[Hugo](https://gohugo.io/) is a free and open-source static site generator.  
It allows for wide customization without any plugins and enables the use of templates to automate your work and content management.

This website is built entirely with Hugo.

## Hugo templating
Hugo templates are based on the Golang programming language and make use of programming concepts such as IF statements or loops.  
Templates can be used in *partials* and *shortcodes*. A template may be simple, such as encasing a piece of text in a `<div>` HTML tag for styling. More complex templates can be used to build tables of contents or complex relationship maps, similar in functionality to DITA reltables.  

This guide does not currently cover instructions on creating custom templates.

### Partials
Partials are templates used in page layouts. The menus on the left and right of this site are created using the built-in partials offered by the [book theme](https://themes.gohugo.io/hugo-book/).

### Shortcodes
Shortcodes are templates used to insert additional elements into the content. They are used in the content source and can be used, for example, to create colored notes or warnings without typing raw HTML into the source.
