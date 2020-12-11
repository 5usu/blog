---
layout: post
title: Using Jekyll to generate static sites and hosting them on Github Pages [Part 2]
tags: jekyll
description: This is a tutorial for using jekyll to generate static sites
---

-- [Vedant Paranjape](https://github.com/VedantParanjape)

# Advanced usage

If you go to your repository you will see a new file, named `_config.yml`, we didn't add this, then how was it added ??? Hahah, I hacked your github account, xD.

Chill, just joking, obviously I didn't. Remember earlier, when you set the theme from repository settings, because of that `_config.yml` was added to the repository.

## What is _config.yml

It is a configuration file used by jekyll to generate your webpage, it contains various settings like site source, site name, author, etc.

You can read more about it here: [https://jekyllrb.com/docs/configuration/](https://jekyllrb.com/docs/configuration/). I will only cover the basic case.

## Creating a _config.yml

* Add the following lines to the already existing `_config.yml`

```yml
title: Jekyll tutorial
url: index.md
description: This is an amazing site I created while learning jekyll.
```

* Now save the file, and check your website after some time, you'll see the website title, and description change as follows.

![](/assets/posts/using-jekyll-with-github-pages-part-2/title_description.png)

## Viewing the site locally

Make sure to install jekyll before hand, from: [https://jekyllrb.com/docs/installation/](https://jekyllrb.com/docs/installation/)

To run the site locally, we need a file called, Gemfile, create a new file called `Gemfile`, and copy the following to it.

```yml
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
```

* Run the following command to install the gems `bundle install`
* Run the following command to start the server `bundle exec jekyll serve`
* Open `127.0.0.1:4000` to view the site locally.   
* You can see, a new folder is created, `_site`, if you look into it, it has all the html files, these have been generated by jekyll and are being shown.
