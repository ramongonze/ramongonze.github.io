---
layout: archive
title: Publications
permalink: /publications/
---

{% assign pubs = site.publications | sort: 'date' | reverse %}
{% for pub in pubs limit:5 %}
({{ pub.date | date: "%Y" }}) <a href="{{ pub.url | relative_url }}"><strong>{{ pub.title }}</strong></a><br>
{{ pub.authors }}<br>
<em>{{ pub.venue }}</em>
<br>
{% endfor %}