---
permalink: /
title: "Software Engineering Portfolio"
excerpt: "Software Engineering student with experience in full-stack development, machine learning, IoT systems, and mobile app development."
author_profile: true
layout: single
redirect_from: 
  - /about/
  - /about.html
---

## My Projects

<div class="portfolio-grid">
{% for post in site.portfolio %}
  <div class="portfolio-card">
    <a href="{{ post.url | relative_url }}" class="portfolio-link">
      <div class="portfolio-content">
        <h3>{{ post.title }}</h3>
        <div class="tech-stack">
          {% if post.tech_stack %}
            {% for tech in post.tech_stack %}
              <span class="tech-tag">{{ tech }}</span>
            {% endfor %}
          {% endif %}
        </div>
        <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
      </div>
    </a>
  </div>
{% endfor %}
</div>