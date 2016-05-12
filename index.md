---
layout: default
title: Sid Jayanna
---

<img src="http://www.gravatar.com/avatar/0687e6637524442617cc342a1ee4755c?s=200" alt="sid jayanna">

[Sid](/about) is passionate about technology, software development, product development, social entrepreneurship, startups and good design. [Read more...](/about)

<div class='posts'>
<hl>
  {% for post in site.posts %}

    <div class='post-listing'>
      <a class='title' href='{{ post.url }}'>{{ post.title }}</a>
      <br>
      <span class='published-on'>{{ post.date | date: "%-d %B %Y" }}</span>
      {% for category in post.categories %}
      <a href="/categories/{{ category }}/" class='category'> #{{ category }} </a>
      {% endfor %}
    </div>

  {% endfor %}
</div>
