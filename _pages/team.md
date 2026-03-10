---
layout: single
title: "Team"
permalink: /team/
---

## Principal Investigator

{% for person in site.data.team.pi %}
<div style="display: flex; gap: 24px; align-items: flex-start; margin-bottom: 32px;">
  <img src="{{ person.image }}" alt="{{ person.name }}" style="width: 150px; height: 150px; border-radius: 50%; object-fit: cover; flex-shrink: 0;">
  <div>
    <h3 style="margin-top: 0;">{{ person.name }}</h3>
    <p>{{ person.role }}<br>{{ person.bio }}</p>
    {% if person.scholar %}<a href="{{ person.scholar }}">Google Scholar</a>{% endif %}
    {% if person.email %} · <a href="mailto:{{ person.email }}">{{ person.email }}</a>{% endif %}
  </div>
</div>
{% endfor %}

---

## Current Members

<div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); gap: 24px; margin-top: 16px;">
{% for person in site.data.team.current %}
<div style="text-align: center;">
  <img src="{{ person.image }}" alt="{{ person.name }}" style="width: 130px; height: 130px; border-radius: 50%; object-fit: cover; margin-bottom: 8px;">
  <div style="font-weight: 600; font-size: 15px;">{{ person.name }}</div>
  <div style="font-size: 13px; color: #6c757d;">{{ person.role }}</div>
</div>
{% endfor %}
</div>

---

## Alumni

{% for person in site.data.team.alumni %}
{{ person.name }}{% unless forloop.last %} · {% endunless %}
{% endfor %}
