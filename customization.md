---
layout: page
title: Customizing Lagmier
permalink: /customization/
read_time: 5 min read
---

The next thing to do is start customizing and adding content to your site.  The following options are available when doing so:

## Theme.yml

The `_data/theme.yml` file was refactored to only contain textual and graphical configuration for the theme.  Removing or clearing any of the items below will remove them from the output:

{% highlight markdown %}
name: Lagomier User   
email: test@example.com
tagline: "Weak opinions, strongly held"
bio: |
  A brief bio or comment can be updated within theme.yml - 
  removing it completely is also possible.    
logo: # displayed in header
favicon: # displayed in browser tab
follow_me: "Follow me:"    
{% endhighlight %}

## Social.yml

The social section is created by providing any number of social media objects to the `_data/social.yml` configuration file:

{% highlight markdown %}
# Social objects require an object to be created
- name: Github 
  display: Github User
  id: github_user
  url: https://github.com/github_user
  icon: fab fa-github
- name: Instagram
  display: Instagram User 
  id: instagram_user
  url: https://www.instagram.com/instagram_user
  icon: fab fa-instagram
{% endhighlight %}

## Logo and Fav Icon

The site logo defaults to the file `/assets/img/logo.png`.  There are a number of ways to override this in your own site:
- Replace `/assets/img/logo.png` in your own repository.
- Adding a replacement image and setting the `logo` entry in `theme.yml`

The fav icon can be updated in much the same ways:
- Replace `/assets/img/favicon.png` in your own repository.
- Adding a replacement image and setting the `favicon` entry in `theme.yml`

## Floating Action Button (Mobile Menu)

When on a smaller device (mobile or tablet) the menu will be accessible through the floating action button.  The button can be customized by `/_includes/fab.html` file.  To just change the image displayed, set the `site.data.theme.fab` setting in `/data/theme.yml`.

The image will default to the `/assets/img/logo.png` if not provided.

## Custom Domain

If you're using this on GitHub Pages with a [custom domain name][cname], you'll want to change this to be the domain you're going to use. All that should be in here is a domain name on the first line and nothing else(like: `example.com`).

## Rouge Highlight

Just as with the original [Lagom][lagom] the Rouge highlight is using the Solarized theme.  This can be overwritten by providing a new `_sass/syntax.scss` or manually applying styles to the `.highlight` selector.

{% highlight java linenos %}
package com.example;

import com.example.UserMapper;

public class UserServiceImpl {

    @Inject
    private UserMapper userMapper;

    @CacheGet
    public User getUserByEmail(String email) {
        return userMapper.getByEmail(email);
    }
}
{% endhighlight %}

[lagom]: https://github.com/swanson/lagom
[cname]: https://help.github.com/en/github/working-with-github-pages/configuring-a-custom-domain-for-your-github-pages-site