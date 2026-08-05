---
layout: splash
title: "Judy Li"
permalink: /
author_profile: false

header:
  overlay_color: "#17324d"
  overlay_filter: 0.4
---

# Knowledge Governance for the AI Era

Building trusted knowledge foundations for AI-ready organizations.

**Documentation Leadership • Knowledge Systems • AI Transformation**

---

## About

I help organizations transform documentation, governance, and knowledge systems into scalable foundations for AI-powered experiences.

My focus areas include:

- Knowledge Governance
- Knowledge Systems
- Documentation Leadership
- AI Readiness
- Model Context Protocol (MCP)
- AI Agents and Enterprise Knowledge

---

## Core Expertise

### Knowledge Governance

Ownership, quality, lifecycle management, accountability, and trust.

### Knowledge Systems

Transforming information assets into organizational intelligence.

### Documentation Leadership

Building documentation capabilities that scale globally.

### AI & Knowledge

Exploring MCP, AI agents, RAG, and intelligent knowledge ecosystems.

---

> AI is not primarily a model problem.
>
> AI is a knowledge problem.

---

## Latest Insights

{% for post in site.posts limit: 5 %}

### {{ post.url | relative_url }}

*{{ post.date | date: "%B %d, %Y" }}*

{{ post.excerpt }}

{{ post.url | relative_url }}

---

{% endfor %}
