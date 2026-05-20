---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% for category in site.data.publications_categories %}
  <h2>{{ category.title }}</h2>
  <ul>
  {% for post in site.publications %}
    {% if post.category == category.key %}
      <li>
        {% if post.url %}
          <a href="{{ post.url }}">{{ post.title }}</a>
        {% else %}
          {{ post.title }}
        {% endif %}
        {% if post.date %}
          ({{ post.date | date: "%Y" }})
        {% endif %}
        {% if post.venue %}
          <i>{{ post.venue }}</i>
        {% endif %}
        {% if post.paperurl %}
          <a href="{{ post.paperurl }}">[Link]</a>
        {% endif %}
      </li>
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}
