---
layout: default
title: Publications
permalink: /publications/
---

<h1>Publications</h1>
<p class="lead-small">Full list. My name is highlighted. <a href="{{ site.scholar }}">Google Scholar</a></p>

{% assign pubs = site.data.publications | sort: "year" | reverse %}
{% assign current_year = "" %}
{% for pub in pubs %}
  {% if pub.year != current_year %}
    {% assign current_year = pub.year %}
    <h2 class="year">{{ pub.year }}</h2>
  {% endif %}
  {% include pub.html %}
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
