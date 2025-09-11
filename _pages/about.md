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
/* Make sidebar fixed under the site header so it doesn't leave a gap above,
   and keep content aligned to the top alongside it. Adjust --header-top
   if your header height is different. */
:root {
  --sidebar-width: 280px;
  --sidebar-left: 20px;
  --header-top: 64px; /* change this to match your header height */
}

.sidebar {
  position: fixed;
  top: var(--header-top);
  left: var(--sidebar-left);
  width: var(--sidebar-width);
  z-index: 1000;
  display: block !important;
  box-sizing: border-box;
}

/* Ensure avatar or other pinned elements don't overflow */
.sidebar img,
.sidebar .avatar {
  max-width: 100%;
  height: auto;
  display: block;
}

/* Push the page content to the right and to the same top line */
.page__content {
  margin-left: calc(var(--sidebar-width) + var(--sidebar-left) + 12px);
  margin-top: calc(var(--header-top) - 8px); /* small nudge if needed */
  box-sizing: border-box;
}

/* Portfolio grid */
.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
}

/* Small screens: make sidebar flow back into document */
@media (max-width: 768px) {
  .sidebar {
    position: relative;
    top: auto;
    left: auto;
    width: 100%;
    display: block !important;
  }
  .page__content {
    margin-left: 0;
    margin-top: 0;
  }
}
</style>