---
layout: archive
title: Publications
permalink: /publications/
---

<style>
  :root {
    --accent: #ffd447;
    --muted: #b9c0c4;
    --link: var(--link-color, #00adb5);
  }

  .simple-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .simple-item {
    display: flex;
    gap: 0.6rem;
    padding: 0.25rem 0;
    font-size: 0.95rem;
  }

  .simple-date {
    min-width: 3.5rem;
    font-variant-numeric: tabular-nums;
    font-size: 0.82rem;
    color: var(--muted);
    flex-shrink: 0;
    margin-top: 0.1rem;
  }

  .simple-main {
    flex: 1;
  }

  .item-title a {
    color: var(--link);
    text-decoration: none;
  }

  .item-title a:hover {
    text-decoration: underline;
  }

  .item-meta {
    font-size: 0.86rem;
    color: var(--muted);
  }

  .item-meta em {
    font-style: italic;
  }
</style>

<ul class="simple-list">
  {% assign pubs = site.publications | sort: 'date' | reverse %}
  {% for pub in pubs %}
    <li class="simple-item">
      <span class="simple-date">
        {{ pub.date | date: "%Y" }}
      </span>
      <div class="simple-main">
        <div class="item-title">
          <a href="{{ pub.url | relative_url }}">{{ pub.title }}</a>
        </div>

        {% if pub.authors %}
          <div class="item-meta">{{ pub.authors }}</div>
        {% endif %}

        {% if pub.venue %}
          <div class="item-meta"><em>{{ pub.venue }}</em></div>
        {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
