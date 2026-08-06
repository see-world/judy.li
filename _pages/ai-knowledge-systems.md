---
title: "AI & Knowledge Systems"
permalink: /ai-knowledge-systems/
layout: single
author_profile: true
---


Artificial intelligence is transforming the way organizations create, manage, discover, and apply knowledge.

This section explores the intersection of AI, knowledge management, information governance, and technical communication. Topics include AI agents, knowledge systems, intelligent information retrieval, documentation automation, Model Context Protocol (MCP), enterprise search, and the future of knowledge work.

The focus is not only on AI technologies, but also on the information architectures, governance practices, and organizational capabilities required to make AI truly effective.

AI can only be as powerful as the knowledge it consumes.

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
