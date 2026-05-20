---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<!-- 加上了 ol 标签，并加上样式让它按倒序或正常序号排列，且有好看的缩进 -->
<ol style="margin-left: 20px; line-height: 1.8;">
{% for post in site.publications reversed %}
  <li style="margin-bottom: 12px;">
    {% if post.url %}
      <a href="{{ post.url }}?v={{ 'now' | date: '%s' }}">{{ post.title }}</a>
    {% else %}
      <strong>{{ post.title }}</strong>
    {% endif %}

    {% if post.date %}
      ({{ post.date | date: "%Y" }})
    {% endif %}

    {% if post.venue %}
      -- <i>{{ post.venue }}</i>
    {% endif %}

    {% if post.paperurl %}
      <a href="{{ post.paperurl }}" target="_blank" style="margin-left: 8px;">[PDF]</a>
    {% endif %}
  </li>
{% endfor %}
</ol>
