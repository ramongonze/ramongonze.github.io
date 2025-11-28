---
layout: archive
title: News
permalink: /news/
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
    min-width: 6.2rem;
    font-variant-numeric: tabular-nums;
    font-size: 0.82rem;
    color: var(--muted);
    flex-shrink: 0;
    margin-top: 0.1rem;
  }

  .simple-main {
    flex: 1;
  }

  .simple-main a {
    color: var(--link);
    text-decoration: none;
  }

  .simple-main a:hover {
    text-decoration: underline;
  }
</style>

<ul class="simple-list">
  {% assign news = site.news | sort: 'date' | reverse %}
  {% for item in news %}
    <li class="simple-item">
      <span class="simple-date">
        {{ item.date | date: "%d %b %Y" }}
      </span>
      <div class="simple-main">
        {{ item.description }}
      </div>
    </li>
  {% endfor %}
</ul>
