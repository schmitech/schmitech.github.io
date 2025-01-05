---
layout: page
title: Use Cases
permalink: /use-cases/
hide_title: true
---

{% include logo.html %}

Explore our catalog of Proofs of Concept and Prototypes to see our solutions in action. 

See something that sparks your interest? [Let's talk!](/contact){: .cta-button}. We're eager to share the details and explore how we can tailor these solutions to your unique needs.

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