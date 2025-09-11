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

I'm a Software Engineering student at Singapore Institute of Technology with experience in full-stack development, machine learning, IoT systems, and mobile app development.

## My Projects

<div class="page__content">
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
</div>


<style>
/* Portfolio grid */
.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
}

/* Neater styling for portfolio items */
.portfolio-card {
  background: #f9f9f9;
  padding: 1rem;
  border-radius: 4px;
}

.portfolio-link {
  display: block;
  text-decoration: none;
  color: inherit;
}

.portfolio-content h3 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  font-size: 1.25rem;
  color: #333;
  font-weight: 600;
}

.tech-stack {
  margin-bottom: 1rem;
}

.tech-tag {
  display: inline-block;
  background: #e0e0e0;
  color: #555;
  padding: 0.25rem 0.5rem;
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
  border-radius: 3px;
  font-size: 0.875rem;
  font-weight: 500;
}

.portfolio-content p {
  margin: 0;
  color: #666;
  line-height: 1.5;
}
</style>