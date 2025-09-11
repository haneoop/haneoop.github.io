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
/* --- Step 1: Create a two-column layout for the main content area --- */

/* * We are targeting the theme's main content wrapper, which holds both
 * the sidebar and your page content. Applying Flexbox here is key.
 * The selector #main is a common one, but may be different in your theme.
 */
#main {
  display: flex;
  justify-content: space-between;
}

/*
 * Force the sidebar to be visible and assign it a fixed width.
 * `flex: 0 0 280px` means it won't grow or shrink and will be 280px wide.
 */
.sidebar {
  display: block !important; /* Override any 'display: none' from the theme */
  flex: 0 0 280px; /* Adjust width as needed */
  margin-right: 2em; /* Adds some space between the sidebar and the grid */
}

/*
 * This is the theme's container for your page content. We tell it to
 * take up all the remaining flexible space. Your grid will live inside this.
 */
#main .archive {
  flex-grow: 1;
}


/* --- Step 2: Your existing styles for the portfolio grid --- */
/* (No changes needed here) */

.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem; /* Reduced gap slightly for better fit */
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
  font-size: 1.2rem;
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
  font-size: 0.95rem;
}


/* --- Step 3: Ensure it looks good on mobile phones --- */
@media (max-width: 768px) {
  #main {
    display: block; /* Stack the content and sidebar on mobile */
  }
  .sidebar {
    display: none !important; /* Hide the sidebar on mobile */
  }
  .portfolio-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}
</style>