---
layout: default
title: Sid Jayanna
---
[Sid](/about) is passionate about technology, software development, product development, social entrepreneurship, startups and good design. He loves to use technology to help improve communities. [Read more](/about)
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
