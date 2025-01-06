---
layout: tags
title: "Tags"
permalink: /tags/
---


<h1>Tags</h1>

<ul>
  {% for tag in site.tags %}
    <li>
      <a href="{{ site.baseurl }}/tags/{{ tag[0] | slugify }}/">{{ tag[0] }}</a> ({{ tag[1].size }})
    </li>
  {% endfor %}
</ul>
