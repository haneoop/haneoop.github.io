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
/* ensure sidebar is visible and content is pushed right so they don't overlap */
.sidebar {
  display: block !important;
  position: relative;
  width: 280px;
  flex: 0 0 280px;
  margin-right: 2em;
}

/* push the page content to make room for the sidebar */
.page__content {
  margin-left: 320px; /* sidebar width + spacing */
}

/* keep your portfolio grid rules */
.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
}
.portfolio-card { /* ...existing rules... */ }
.portfolio-link { /* ...existing rules... */ }
/* other rules kept as before... */

/* mobile: stack and hide sidebar */
@media (max-width: 768px) {
  .page__content {
    margin-left: 0;
  }
  .sidebar {
    display: none !important;
  }
}
</style>