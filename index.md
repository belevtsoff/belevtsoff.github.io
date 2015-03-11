---
layout: page
title: Welcome, comrade!
---
{% include JB/setup %}

Let me introduce you to a **bunch of stuff** (how awesome is that?) that I
think might be of any use to other strangers, seeking for answers. 

## Posts

Here's what I've got so far:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
