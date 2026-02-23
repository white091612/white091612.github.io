---
layout: page
title: Tags
permalink: /tags/
---

<div class="tag-cloud" style="margin-bottom: var(--spacing-xl);">
{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
  <a href="#{{ tag[0] | slugify }}" class="tag" style="margin: 4px; display: inline-block;">
    #{{ tag[0] }} ({{ tag[1].size }})
  </a>
{% endfor %}
</div>

<ul class="taxonomy-list">
{% for tag in sorted_tags %}
  <li>
    <h2 id="{{ tag[0] | slugify }}">#{{ tag[0] }}</h2>
    <ul class="taxonomy-posts">
      {% for post in tag[1] %}
        <li>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y.%m.%d" }}</time>
        </li>
      {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>

{% if site.tags.size == 0 %}
<p style="color: var(--color-text-muted);">아직 태그가 없습니다.</p>
{% endif %}
