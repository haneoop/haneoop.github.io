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

/* Portfolio card styling for a neat card appearance */
.portfolio-card {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: box-shadow 0.3s ease, transform 0.3s ease;
}

.portfolio-card:hover {
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
  transform: translateY(-2px);
}

.portfolio-link {
  display: block;
  text-decoration: none;
  color: inherit;
}

.portfolio-content {
  padding: 1.5rem;
}

.portfolio-content h3 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  font-size: 1.25rem;
  color: #333;
}

.tech-stack {
  margin-bottom: 1rem;
}

.tech-tag {
  display: inline-block;
  background: #f0f0f0;
  color: #666;
  padding: 0.25rem 0.5rem;
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
  border-radius: 4px;
  font-size: 0.875rem;
}

.portfolio-content p {
  margin: 0;
  color: #666;
  line-height: 1.5;
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