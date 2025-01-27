---
layout: tags
title: "Tags"
permalink: /tags/
---

<style>
  .tags-list {
    column-count: 2;
    column-gap: 2rem;
    padding-left: 0;
    list-style: none;
  }
  .tags-list li {
    break-inside: avoid-column;
    margin-bottom: 0.8rem;
    font-family: 'Helvetica Neue', Arial, sans-serif;
    font-size: 1.1rem;
  }
  @media (max-width: 768px) {
    .tags-list {
      column-count: 1;
    }
  }
</style>

<h1>Tags</h1>

<!-- Debug section remains -->
<p>Debug: {{ site.tags | inspect }}</p>

<!-- Sorted tags in 2 columns -->
<ul class="tags-list">
  {% assign sorted_tags = site.tags | sort %}
  {% for tag in sorted_tags %}
    <li>
      <a href="{{ site.baseurl }}/tags/{{ tag[0] | slugify }}/" 
         style="text-decoration: none; color: #2d3e50;">
        {{ tag[0] | capitalize }}
      </a> 
      <small>({{ tag[1].size }})</small>
    </li>
  {% endfor %}
</ul>

<!-- Add image section here if needed -->
<!-- <img src="/assets/images/your-image.jpg" alt="Tags Illustration"> -->