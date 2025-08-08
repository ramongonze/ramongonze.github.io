---
layout: archive
title: News
permalink: /news/
---

<style>
  :root {
    --accent: #ffd447;
    --link: var(--link-color, #00adb5);
    --card: #2a2a2a;
    --muted: #b9c0c4;
  }

  .news-list {
    display: grid;
    gap: .6rem;
    margin-top: .6rem;
  }

  .news-item {
    background: var(--card);
    border-radius: 12px;
    padding: .55rem .75rem;
    box-shadow: 0 4px 12px rgba(0,0,0,.18);
    display: flex;
    align-items: flex-start;
    gap: .5rem;
  }

  .news-date {
    display: inline-block;
    font-weight: 700;
    font-size: .85rem;
    padding: .15rem .45rem;
    border-radius: 999px;
    background: rgba(255,212,71,.14);
    color: var(--accent);
    margin-right: .5rem;
  }

  .news-text {
    flex: 1;
    color: var(--muted);
  }

  .news-text a {
    color: var(--link);
  }
</style>

<div class="news-list">
  {% assign news = site.news | sort: 'date' | reverse %}
  {% for item in news %}
    <div class="news-item">
      <span class="news-date">{{ item.date | date: "%d %b %Y" }}</span>
      <div class="news-text">{{ item.description }}</div>
    </div>
  {% endfor %}
</div>
