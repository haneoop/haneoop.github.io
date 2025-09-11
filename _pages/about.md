---
permalink: /
title: "Software Engineering Portfolio"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I'm a Software Engineering student at Singapore Institute of Technology with experience in full-stack development, machine learning, IoT systems, and mobile app development.

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

<style>
.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.portfolio-card {
  border: 1px solid #e1e1e1;
  border-radius: 8px;
  overflow: hidden;
  transition: transform 0.2s, box-shadow 0.2s;
  background: white;
}

.portfolio-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.portfolio-link {
  text-decoration: none;
  color: inherit;
  display: block;
}

.portfolio-content {
  padding: 1.5rem;
}

.portfolio-content h3 {
  margin: 0 0 1rem 0;
  color: #2c3e50;
}

.tech-stack {
  margin-bottom: 1rem;
}

.tech-tag {
  display: inline-block;
  background: #3498db;
  color: white;
  padding: 0.2rem 0.5rem;
  border-radius: 4px;
  font-size: 0.8rem;
  margin-right: 0.5rem;
  margin-bottom: 0.3rem;
}

.portfolio-content p {
  color: #666;
  line-height: 1.5;
  margin: 0;
}
</style>