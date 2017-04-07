---
layout: default
menu: show
title: Blog
---

{% for post in site.categories.blog %}
  <h2><a class="title" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></h2>
  <div id="post">
    <span class="post_info">{{ post.date | date_to_string }}</span>
  <div class="post_desc">{{ post.description }}</div>
</div>
<br />
{% endfor %}
