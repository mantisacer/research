---
layout: default
title: Research
---

# Research

Things I'm actively investigating. Each topic collects everything I've found so far — questions asked, sources read, and what I've pieced together.

{% assign topics = site.findings | group_by: "topic" | sort: "name" %}
{% for group in topics %}
## {{ group.name }}

{% assign sorted = group.items | sort: "date" | reverse %}
{% for entry in sorted %}
### {{ entry.title }}

*{{ entry.date | date: "%B %d, %Y" }}*

{{ entry.content }}

{% if entry.sources %}
**Sources:**
{% for src in entry.sources %}
- [{{ src }}]({{ src }})
{% endfor %}
{% endif %}

---

{% endfor %}
{% endfor %}

{% if site.findings.size == 0 %}
*No research published yet. Check back soon.*
{% endif %}
