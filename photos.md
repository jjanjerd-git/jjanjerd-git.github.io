---
layout: page
title: Photos
permalink: /photos/
---

<div class="photo-grid">
{% for photo in site.photos %}
  <a href="{{ photo.url | relative_url }}" class="photo-grid-item">
    <img src="{{ photo.image | relative_url }}" alt="{{ photo.title }}">
    <span>{{ photo.title }}</span>
  </a>
{% endfor %}
</div>

{% if site.photos.size == 0 %}
<p>No photos yet — check back soon!</p>
{% endif %}

<style>
.photo-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 16px;
  margin-top: 24px;
}
.photo-grid-item {
  display: block;
  text-decoration: none;
  color: inherit;
}
.photo-grid-item img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 6px;
}
.photo-grid-item span {
  display: block;
  margin-top: 6px;
  font-size: 0.9em;
}
</style>
