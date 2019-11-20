---
layout: default
title: Page Assets
permalink: /page-assets/
---

# Page Assets

There are a number of standard theme page assets that are provided, they can all be over writen within the `/assets` folder:

## 404

A `/404.html` page is provided - but in most cases this should be overwritten.

## Atom

An `/atom.xml` page is provided.

## Site Json

A `/site.json` file is provided, which can be used for searching/ajax related functionality.  Although the file is provided, the javascript features need to be added by the implementing project.

## Archive

An `/archive/` page is created with a list of posts grouped by year.  The archive content can be edited by overriding or modifying the following files:

{% highlight markdown %}
# theme.yml
archive:
  title: Archive
  description: |
    Please browse through my published articles - comments and corrections are always welcome.
{% endhighlight %}

while each post entry is displayed using the `_include/archive-post-item.html`.  The template has requires allows for a number of parameters:

{% highlight markdown %}
{% raw %}
{% include archive-post-item.html 
    p=post 
    date_format="%b %-d"
    categories=true|false
    tags=true|false %}
{% endraw %}
{% endhighlight %}

## Categories

A `/categories/` page is creating grouping posts by category.  Posts can appear in multiple categories if they've been assigned to both.  Categories have the same configuration of title and description:

{% highlight markdown %}
# theme.yml
categories:
  title: Categories
  description: |
    Please browse through my published articles - comments and corrections are always welcome.
{% endhighlight %}

The same `_include/archive-post-item.html` is used.
