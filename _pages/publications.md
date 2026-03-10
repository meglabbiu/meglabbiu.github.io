---
layout: single
title: "Publications"
permalink: /publications/
---

{% assign pubs_by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}

{% for year_group in pubs_by_year %}
## {{ year_group.name }}

{% for pub in year_group.items %}
{{ pub.authors }} **{{ pub.title }}** *{{ pub.journal }}.*{% if pub.link %} [Link]({{ pub.link }}){% endif %}
{: .notice}
{% endfor %}

{% endfor %}
