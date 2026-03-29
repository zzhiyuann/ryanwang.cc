---
layout: page
title: Blog
permalink: /blog/
description: Writing on AI agent infrastructure, MCP-native systems, and production AI workflows.
---

{% if site.posts.size > 0 %}
<ul class="posts">
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
    {% if post.description %}<p class="posts-teaser-text">{{ post.description }}</p>{% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
<div class="empty-state">
  <p>Posts are in progress. Planned topics include:</p>
  <ul>
    <li>Death & Resurrection: How I Made AI Agents Remember</li>
    <li>6 AI Agents, One Engineer: Running a Company with AgentOS</li>
    <li>What Production Agent Infrastructure Needs Beyond Better Models</li>
  </ul>
</div>
{% endif %}
