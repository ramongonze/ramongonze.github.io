---
layout: archive
title: Projects
permalink: /projects/
---

<style>
  .project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
  }

  .project-card {
    background-color: #2a2a2a; /* lighter than site background for contrast */
    border-radius: 12px;
    padding: 1.2rem 1.5rem;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .project-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 6px 14px rgba(0, 0, 0, 0.4);
  }

  .project-card h3 {
    margin-top: 0;
    margin-bottom: 0.4rem;
  }

  .project-card h3 a {
    color: var(--link-color, #00adb5);
    text-decoration: none;
  }

  .project-card h3 a:hover {
    text-decoration: underline;
  }

  .project-date {
    font-size: 0.85rem;
    color: #bbbbbb;
    margin-bottom: 0.6rem;
    display: block;
  }

  .project-description {
    font-size: 0.95rem;
    color: #e0e0e0;
  }
</style>

<div class="project-grid">
  {% assign projects = site.projects | sort: 'date' | reverse %}
  {% for project in projects %}
    <div class="project-card">
      <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
      <span class="project-date">Updated on {{ project.date | date: "%b %Y" }}</span>
      {% if project.description %}
        <p class="project-description">{{ project.description }}</p>
      {% endif %}
    </div>
  {% endfor %}
</div>
