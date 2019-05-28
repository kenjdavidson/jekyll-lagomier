# Lagom

> #### *Lagom* is a Swedish word with no direct English equivalent, meaning "just the right amount"

Lagom, a [Jekyll][j] blog theme with just the right amount of style. 

Extracted lovingly from [http://mdswanson.com][mds] for your enjoyment!



* Responsive, based on [Skeleton][skeleton]
* [Font Awesome][font-awesome] for icons
* Open Sans from [Google web fonts][gfonts]
* Built-in Atom feed

[![Live Demo](https://img.shields.io/badge/view-live--demo-blue.svg?style=flat-square)](http://lagom.mdswanson.com/)

## Action Shots
![](http://i.imgur.com/Pmzk4j1.png)
![](http://i.imgur.com/CT2Xvug.png)
![](http://i.imgur.com/XisjqW1.jpg)

## Installation

### Forking
- [Fork this repository][fork]
- Clone it: `git clone https://github.com/YOUR-USER/lagom`
- Install the [GitHub Pages gem][pages] (includes Jekyll): `bundle install`
- Run the jekyll server: `jekyll serve`

You should have a server up and running locally at <http://localhost:4000>.

### Remote-theme
If you're not interested in making any changes to the theme directly, you can update the `_config.yml` file
in your repository to replace `theme: ...` with `remote-theme: swanson/lagom`.  You can then override
any specific files to provide your own implementation.

### Combination
You can also complete the installation using a combination of the two - Fork repo to your own account and use
the `remote-theme: youraccount/lagom` to configure.

## Customization

Next you'll want to change a few things. Most of them can be changed directly in
[theme.yml][config]. That's where you can add your social links, change the accent
color, stuff like that.

There's a few other places that you'll want to change, too:

### Custom Domain
[CNAME][cname]: If you're using this on GitHub Pages with a custom domain name, 
you'll want to change this to be the domain you're going to use. All that should 
be in here is a domain name on the first line and nothing else (like: `example.com`).

### Fav Icon
[favicon.png][favicon]: This is the icon in your browser's address bar. You should 
change it to whatever you'd like.

### Site logo
The site logo is has a number of different configuration options, in the following priority:
- Adding the `theme.logo` configuration item to the `_data/theme.yml` file.
- Adding a `gravatar` link/id to the `_data/theme.yml` file.
- Adding the file [logo.png][logo] to you repository.

Site logo can be customized by overriding the `assets/css/all.css` and providing custom styles for
`img[#avatar] { }`

### Site description
The site description can be updated using the `theme.description` or the `site.description`
from the from `_data/theme.yml` or `_config.yml` files (respectively).  Originally the description required
updates/overrides to the `_includes/sidebar.html` file.

## Deployment

You should deploy with [GitHub Pages][pages] - it's just easier.

All you should have to do is rename your repository on GitHub to be
`username.github.io`. Since everything is on the `gh-pages` branch, you
should be able to see your new site at <http://username.github.io>.

## Licensing

[MIT](https://github.com/swanson/lagom/blob/master/LICENSE) with no
added caveats, so feel free to use this on your site without linking back to
me or using a disclaimer or anything silly like that.

## Contact
I'd love to hear from you at [@_swanson][twitter]. Feel free to open issues if you
run into trouble or have suggestions. Pull Requests always welcome.

[j]: http://jekyllrb.com/
[mds]: http://mdswanson.com
[skeleton]: http://www.getskeleton.com/
[font-awesome]: http://fortawesome.github.io/Font-Awesome/
[gfonts]: http://www.google.com/fonts/specimen/Open+Sans
[fork]: https://github.com/swanson/lagom/fork
[config]: https://github.com/swanson/lagom/blob/master/_data/theme.yml
[cname]: https://github.com/swanson/lagom/blob/master/CNAME
[favicon]: https://github.com/swanson/lagom/blob/master/favicon.png
[logo]: https://github.com/swanson/lagom/blob/master/logo.png
[pages]: http://pages.github.com
[twitter]: https://twitter.com/_swanson
[pages]: https://github.com/github/pages-gem
