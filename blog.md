---
layout: page
title: Blog
permalink: /blog/
---

## Latest Insights

Explore our latest thoughts on AI, machine learning, and how businesses can leverage these technologies.

<div class="post-list">
  {% for post in site.posts %}
    <article class="post-preview">
      <h2>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <div class="post-meta">
        {{ post.date | date: "%B %-d, %Y" }}
      </div>
      {% if post.image %}
        <div class="post-image">
          <img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
        </div>
      {% endif %}
      <div class="post-excerpt">
        {{ post.excerpt }}
      </div>
      <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
    </article>
  {% endfor %}
</div>