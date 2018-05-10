---
layout: page
menu: show
title: Archives
permalink: /archives.html
---

<div class="archives">
<ul>
{% for post in site.posts  %}
{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}

{% if forloop.first %}
<div id='hr_dotted'></div>
<center><p><h1>{{this_year}}</h1></p></center>
<div id='hr_dotted'></div>
{% endif %}
<li><span class='left_0'>{{ post.date | date:"%Y-%m-%d" }} <span class='postName'>&raquo; <a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></span></span></li>
{% if forloop.last %}
{% else %}
{% if this_year != next_year %}
<div id='hr_dotted'></div>
<center><p><h1>{{next_year}}</h1></p></center>
<div id='hr_dotted'></div>
{% endif %}
{% endif %}
{% endfor %}
</ul>
</div>
