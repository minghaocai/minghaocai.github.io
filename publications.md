---
layout: default
title: Publications
permalink: /publications/
---

<h1>Publications</h1>
<p class="lead-small">Full list. My name is highlighted. <a href="{{ site.scholar }}">Google Scholar</a></p>

{% assign grouped = site.data.publications | group_by: "year" | sort: "name" | reverse %}
{% for year_group in grouped %}
  <h2 class="year">{{ year_group.name }}</h2>
  {% for pub in year_group.items %}
    {% include pub.html %}
  {% endfor %}
{% endfor %}

<h1>Talks &amp; Presentations</h1>
<ul class="talks">
  {% for t in site.data.talks %}
    <li>
      <span class="muted">{{ t.type }}.</span>
      {{ t.title }}{% if t.venue %}, {{ t.venue }}{% endif %}{% if t.extra %}, {{ t.extra }}{% endif %}
    </li>
  {% endfor %}
</ul>
