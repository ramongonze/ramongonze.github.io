---
layout: archive
title: News
permalink: /news/
---

{% assign news = site.news | sort: 'date' | reverse %}
{% for new in news %}
  <strong>[{{ new.date | date: "%d %b %Y" }}]</strong> {{ new.description }}
  <br><br>
{% endfor %}

<style>
  strong {
    color: #00adb5;
  }
</style>