---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% for post in site.publications reversed %}
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
{% endfor %}
