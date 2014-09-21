---
layout: post
title: "Build Warning: Layout 'nil' requested in ..."
date: 2014-09-21 16:22:07 -0400
comments: true
categories: [blogging,octopress]
keywords: blogging,octopress,layout,nil
description: "Build Warning: Layout 'nil' requested in ..."
---

I have just finished updating my blog to the latest version of Octopress and Octoflat theme. More updates to the site should be forthcoming soon. The only minor warning I received is when running 'rake generate':

```
Build Warning: Layout 'nil' requested in blog/categories/open-source/atom.xml does not exist.
```

This can occur a number of times based on the amount of posts in the blog. After a quick lookup it can also occur in Jekyll as well. Turns out the fix was as simple as changing 'layout: nil' to 'layout: null', which is the correct way to specify a non-existent layout. I had to modify the following files to get all of the warnings to resolve:

```
source/_includes/custom/category_feed.xml
source/atom.xml
source/robots.txt
```

All looks good after this, and happy to be continuing on with Octopress.
