---
title: "AI"
permalink: /ai/
layout: single
author_profile: true
---


Artificial intelligence is transforming the way organizations create, manage, discover, and apply knowledge.

This section explores the intersection of AI, knowledge management, information governance, and technical communication. Topics include AI agents, knowledge systems, intelligent information retrieval, documentation automation, Model Context Protocol (MCP), enterprise search, and the future of knowledge work.

The focus is not only on AI technologies, but also on the information architectures, governance practices, and organizational capabilities required to make AI truly effective.

AI can only be as powerful as the knowledge it consumes.

---

## Featured Series

### [From Documents to Intelligence]({{ "/ai/from-documents-to-intelligence/" | relative_url }})

Exploring how AI, knowledge systems, and information governance are transforming the way organizations create, manage, discover, and apply knowledge.

From engineering information governance and knowledge management to AI agents, MCP, and intelligent workflows, this series examines what it takes to build scalable knowledge systems for the AI era.



[Read the series]({{ "/ai/from-documents-to-intelligence/" | relative_url }}){: .btn .btn--primary}

---

## Articles

{% assign governance_posts = site.governance | sort: "title" %}

{% for post in governance_posts %}

### <a href="{{ post.url | relative_url }}">{{ post.title }}</a>

{{ post.excerpt }}

---

{% endfor %}
