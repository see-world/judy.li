---
layout: splash
title: "Judy Li"
permalink: /
---

# Judy Li

## Knowledge Governance • Documentation Leadership • AI Transformation

Building the bridge between documentation, governance, knowledge systems, and AI-powered information experiences.

---

## Core Focus Areas

### Knowledge Governance

Ownership, quality, lifecycle, and accountability.

### Knowledge Systems

Transforming content into organizational intelligence.

### Documentation Leadership

Building documentation capabilities that scale.

### AI & Intelligent Content

Exploring MCP, AI Agents, RAG, and future knowledge ecosystems.

---

> AI is not primarily a model problem.
>
> AI is a knowledge problem.

---

## Latest Articles

{% for post in site.posts limit:5 %}
### {{ post.url | relative_url }}

{{ post.excerpt }}

{% endfor %}
