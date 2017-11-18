---
layout: page
title: "Jekyll"
date:  2016-05-19 13:00:06
---
[Jekyll](https://jekyllrb.com/) is the framework which I use to power my personal [website](http://sjayanna.github.io). It is minimal design and has a very low footprint and hosted right on Github which makes it easy to maintain. You can view the code [here](https://github.com/sjayanna/sjayanna.github.io). You can read more Information about hosting site on Github pages via Jekyll [here](https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/)

Below is my workflow creating new posts.

To create a new post -

{% highlight bash %}
☆|ruby-2.3.1@homepage| GFC-13-mbp in ~/Dropbox/src/homepage/sjayanna.github.io
± |master ✓| → rake post
Title: Deploying site on Github pages using Jekyll
Slug: deploy-iste-to-github-pages
Categories: jekyll
{% endhighlight %}

To create a new page -

{% highlight bash %}
☆|ruby-2.3.1@homepage| GFC-13-mbp in ~/Dropbox/src/homepage/sjayanna.github.io
± |master ✓| → rake page
Title: Jekyll
Slug: notes/jekyll
{% endhighlight %}

To serve the files locally and you should be able to view them at localhost:4000

{% highlight bash %}
☆|ruby-2.3.1@homepage| GFC-13-mbp in ~/Dropbox/src/homepage/sjayanna.github.io
± |master ✓| → jekyll s
{% endhighlight %}

Add the files and commit and push to github to publish the posts.

{% highlight bash %}
☆|ruby-2.3.1@homepage| GFC-13-mbp in ~/Dropbox/src/homepage/sjayanna.github.io
± |master ✓| → git add . && git commit -m "message" && git push origin master
{% endhighlight %}


### References
* [How to create Jekyll Drafts](http://www.fizerkhan.com/blog/posts/Working-with-upcoming-posts-in-Jekyll.html)
* [Using Jekyll with Github pages](https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/)
* [Jekyll Drafts](http://jekyllrb.com/docs/drafts/)
* [Drafts](http://hamishwillee.github.io/2014/06/11/public-drafts-in-jekyll/)
* [Another link for drafts](http://tqclarkson.com/2012/08/22/jekyll-drafts/)
* [Changes in new Github-pages](https://github.com/blog/2100-github-pages-jekyll-3)
