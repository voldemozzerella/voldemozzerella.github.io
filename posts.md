---
layout: default
title: "posts"
---

{% if site.show_excerpts %}
  {% include home.html %}
{% else %}
  {% include archive.html title="Posts" %}
{% for post in site.posts %}
    <article>
      <header>
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      </header>
      <p>{{ post.excerpt | strip_html | truncate: 150 }}...</p>
      <a href="{{ post.url }}">Read More</a>
    </article>
{% endfor %}
{% endif %}
