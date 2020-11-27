---
layout: post
title:  "Jekyll Minima Version"
date:   2020-11-19 00:00:00 +0000
categories: 
---

This blog was created using Jekyll with Minima theme via Ruby Gem.  While the Minima theme has been receiving continuous updates, the version in [github-pages plugins](https://github.com/github/pages-gem/blob/master/lib/github-pages/plugins.rb#L52) was still on 2.5.1, which was created back on 2019-08-16.  There is a [pull request](https://github.com/jekyll/minima/issues/411) to create a new release tag.  However, until that happens, you can use `jekyll-remote-theme` to access the latest version directly, as suggested by [ashmaroli](https://github.com/jekyll/minima/issues/411#issuecomment-730160996).

```yml
# _config.yml

# Add to plugins: list
plugins:
  - jekyll-remote-theme

# set up remote_theme
remote_theme: jekyll/minima
```