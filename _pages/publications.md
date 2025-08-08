---
layout: archive
title: Publications
permalink: /publications/
---

<style>
  :root{
    --accent:#ffd447;
    --link:var(--link-color,#00adb5);
    --card:#2a2a2a;
    --muted:#b9c0c4;
    --divider:rgba(255,255,255,0.08);
  }

  .pub-list{ display:grid; gap:.8rem; margin-top:1rem; }

  .pub-card{
    background:var(--card);
    border-radius:12px;
    padding:1rem 1.2rem;
    box-shadow:0 4px 12px rgba(0,0,0,.18);
    transition:transform .15s ease, box-shadow .15s ease;
  }
  .pub-card:hover{ transform:translateY(-2px); box-shadow:0 8px 18px rgba(0,0,0,.25); }

  .pub-head{
    display:flex; align-items:baseline; gap:.6rem;
    margin:0 0 .35rem 0;
  }

  .year-badge{
    display:inline-block; font-weight:700; font-size:.85rem;
    padding:.15rem .45rem; border-radius:999px;
    background:rgba(255,212,71,.14); color:var(--accent);
    flex:0 0 auto;
  }

  .pub-title{ font-weight:600; line-height:1.35; }
  .pub-title a{ color:var(--link); text-decoration:none; }
  .pub-title a:hover{ text-decoration:underline; }

  .pub-meta{ font-size:.92rem; color:var(--muted); margin-top:.1rem; }
  .pub-venue{ font-size:.95rem; }

  /* optional divider between year groups */
  .year-divider{
    margin:1.5rem 0 .25rem; padding-top:.75rem;
    border-top:1px solid var(--divider); font-weight:700;
  }
</style>

{% comment %}
If you’d rather show just the latest N, add:  limit:5  to the loop.
{% endcomment %}

{% assign pubs = site.publications | sort: 'date' | reverse %}

<div class="pub-list">
  {% assign current_year = "" %}
  {% for pub in pubs %}
    {% assign y = pub.date | date: "%Y" %}
    {% if y != current_year %}
      {% unless forloop.first %}
        <!-- space between year groups -->
      {% endunless %}
      <div class="year-divider">{{ y }}</div>
      {% assign current_year = y %}
    {% endif %}

    <article class="pub-card">
      <div class="pub-head">
        <div class="pub-title">
          <a href="{{ pub.url | relative_url }}">{{ pub.title }}</a>
        </div>
      </div>

      {% if pub.authors %}
        <div class="pub-meta">{{ pub.authors }}</div>
      {% endif %}

      {% if pub.venue %}
        <div class="pub-venue"><em>{{ pub.venue }}</em></div>
      {% endif %}
    </article>
  {% endfor %}
</div>
