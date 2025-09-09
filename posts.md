---
layout: page
title: Posts
permalink: /posts/
---

# All Posts

Here are all my articles organized by topic:

<div class="posts">
  {% for post in site.posts %}
    <article class="post-item">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
      {% if post.excerpt %}
        <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      {% endif %}
    </article>
  {% endfor %}
</div>
