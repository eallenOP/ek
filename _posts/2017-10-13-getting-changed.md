---
layout: post
title: Getting changed
categories: tech
tags: technical jekyll web challenge
---
So, I decided to try adding a new theme to my blog.

Adding a theme to a new site is really easy. You just specify it when you first build the site. In fact, adding a new theme to an existing page isn't that hard either. It's explained in the [docs right here](https://jekyllrb.com/docs/themes/#installing-a-theme).

But if you started with no theme at all or you have already been hacking around with overrides, there are a few things to watch out for. I had to delete a whole lot of stuff to get my new theme to take, because I'd started from a no-theme tutorial. Custom css: gone. Directories for _layouts and _includes: gone. I also had to change the front matter in some pages because the layouts had different names in my new theme. So basically, it's still not that hard, but you have to be ready and willing to get that delete key going and do a bit of spring cleaning.

And then the home page broke.

The theme I had chosen to try used pagination to display posts on the home page. I spent a long time looking in the theme files for what might be causing my home page to be totally blank. In the end, I fixed it by altering (overriding) the index layout.

Then I spotted [this](https://jekyllrb.com/docs/pagination/) and had a bit of a facepalm moment. Add `pagination: [number]` to the config file and away we go. Duh.