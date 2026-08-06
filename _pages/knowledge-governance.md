---
title: "Knowledge Governance"
permalink: /knowledge-governance/
layout: single
author_profile: true
---


Knowledge Governance focuses on ownership, accountability, quality, lifecycle management, and trust in organizational knowledge.

As organizations adopt AI, governance becomes increasingly important because AI systems depend on the quality of the knowledge they consume.

---

## Featured Series

### [Engineering Information Governance]({{ "/governance/engineering-information-governance/" | relative_url }})

A practical exploration of how Document Control evolves into Information Governance and becomes a strategic capability for engineering organizations.

**Series topics include:**

- What Does Document Control Really Manage?
- Why Engineering Projects Lose Control
- Why Is MDL the Most Important Project Document?
- Revision Chaos
- Configuration Management
- Information Governance

[Read the series]({{ "/governance/engineering-information-governance/" | relative_url }}){: .btn .btn--primary}

---

## Articles

{% assign governance_posts = site.governance | sort: "title" %}

{% for post in governance_posts %}

### <a href="{{ post.url | relative_url }}">{{ post.title }}</a>

{{ post.excerpt }}

---

{% endfor %}
