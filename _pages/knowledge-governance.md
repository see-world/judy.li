---
title: "Knowledge Governance"
permalink: /knowledge-governance/
layout: single
author_profile: true
---

# Knowledge Governance

Knowledge Governance focuses on ownership, accountability, quality, lifecycle management, and trust in organizational knowledge.

As organizations adopt AI, governance becomes increasingly important because AI systems depend on the quality of the knowledge they consume.

## Articles

{% assign governance_posts = site.governance | sort: "title" %}

{% for post in governance_posts %}

### [{{ post.title }}]({{ post.url | relativecerpt }}

<a href="{{ post.url |_url }}

---

{% endfor %}
