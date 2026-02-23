---
layout: page
title: Categories
permalink: /categories/
---

<ul class="taxonomy-list">
{% assign sorted_cats = site.categories | sort %}
{% for category in sorted_cats %}
  <li>
    <h2 id="{{ category[0] | slugify }}">{{ category[0] }} <small>({{ category[1].size }})</small></h2>
    <ul class="taxonomy-posts">
      {% for post in category[1] %}
        <li>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y.%m.%d" }}</time>
        </li>
      {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>

{% if site.categories.size == 0 %}
<p style="color: var(--color-text-muted);">아직 카테고리가 없습니다.</p>
{% endif %}
