---
layout: blog
permalink: /blog/
author_profile: true
---

<div class="category-links">
  <p><a href="#ai-ml">AI/ML</a> | <a href="#data-science">Data Science</a> | <a href="#miscellaneous">Miscellaneous</a></p>
</div>

<div id="ai-ml" class="category-section">
  {% assign ai_posts = site.posts | where: "categories", "ai" %}
  {% if ai_posts.size > 0 %}
    {% for post in ai_posts %}
      <div class="post-entry">
        <a href="{{ post.url }}" class="post-title">{{ post.title }}</a>
        <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
      </div>
    {% endfor %}
  {% else %}
    <p class="no-posts">No posts yet in this category.</p>
  {% endif %}
</div>

<div id="data-science" class="category-section">
  {% assign ds_posts = site.posts | where: "categories", "data-science" %}
  {% if ds_posts.size > 0 %}
    {% for post in ds_posts %}
      <div class="post-entry">
        <a href="{{ post.url }}" class="post-title">{{ post.title }}</a>
        <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
      </div>
    {% endfor %}
  {% else %}
    <p class="no-posts">No posts yet in this category.</p>
  {% endif %}
</div>

<div id="miscellaneous" class="category-section">
  {% assign misc_posts = site.posts | where: "categories", "misc" %}
  {% if misc_posts.size > 0 %}
    {% for post in misc_posts %}
      <div class="post-entry">
        <a href="{{ post.url }}" class="post-title">{{ post.title }}</a>
        <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
      </div>
    {% endfor %}
  {% else %}
    <p class="no-posts">No posts yet in this category.</p>
  {% endif %}
</div>

<style>
.category-links {
  margin-bottom: 2em;
  text-align: center;
}
.category-links a {
  text-decoration: none;
  color: #333333;
  margin: 0 1em;
}
.category-links a:hover {
  color: #008080;
  text-decoration: underline;
}
.category-section {
  margin-bottom: 3em;
  padding-top: 1em;
}
.post-entry {
  margin-bottom: 1em;
  text-align: left;
  padding: 0 1.5em;
  display: flex;
  align-items: baseline;
  justify-content: space-between;
}
.post-title {
  text-decoration: none;
  color: #333333;
  font-size: 1em;
  font-weight: normal;
  margin-right: 1em;
}
.post-title:hover {
  color: #008080;
  text-decoration: underline;
}
.post-date {
  color: #666666;
  font-size: 0.9em;
  font-family: "Lato", sans-serif;
  white-space: nowrap;
}
.no-posts {
  color: #666;
  font-style: italic;
  text-align: center;
}
</style> 