---
layout: default
title: Jekyll Github Pages - Category Pages
date: 2020-04-03
categories: [site]
last_modified_at: 2020-04-03 15:00 -6
comments: true
---

# Jekyll Github Pages - Category Pages

Well, it took a while but I finally got category pages going on this site.

I am using Github Pages to host the site and the jekyll-archive plugin is not supported so I had to make the pages myself. I can come up with a tutorial if you leave a comment, below, letting me know you'd like to see one.

At this time, I will say I didn't go with a method I saw on any of the many sites I read while trying to figure this out. Since I use pages with categories (and not posts with tags), my setup is a little different.

I did have to make each category page manually (e.g. "_category/blog.md") but the code in each one is identical. The only things to configure are adding a page tag (tags: blog) and setting the permalink. Then in the page body there is code like the code that generates the list of posts on this site's homepage except it checks if page.categories contains page.tag. 
