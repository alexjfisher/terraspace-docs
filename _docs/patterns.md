---
title: Terraspace Patterns
---

We'll cover some Terraspace and infrastructure-as-code patterns.

{% assign docs = site.docs | where: "categories","patterns" %}
{% for doc in docs -%}
* [{{ doc.nav_text }}]({{ doc.url }})
{% endfor %}
