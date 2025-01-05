---
layout: page
title: Use Cases
permalink: /use-cases/
hide_title: true
---

{% include logo.html %}

Explore our portfolio of Proofs of Concept and Prototypes to see our innovative solutions in action. If any example resonates with you, let us know—we’d be delighted to discuss the details and tailor it to your unique needs.

<div class="post-list">
  {% for post in site.use-cases %}
    <article class="post-preview">
      <h2>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <div class="post-meta">
        {{ post.date | date: "%B %-d, %Y" }}
      </div>
      <div class="post-excerpt">
        {{ post.excerpt }}
      </div>
      <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
    </article>
  {% endfor %}
</div>