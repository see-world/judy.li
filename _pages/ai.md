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


**Series topics include:**

- Why Information Governance Matters More Than Ever in the Age of AI
- Why Knowledge Management Is Becoming the New Infrastructure for AI
- From Documents to Intelligence: Rethinking Knowledge in the AI Era
- Why Most Enterprise Knowledge Bases Fail
- Why Large Language Models Lack Context
- Why Organizations Need Knowledge Workflows, Not Just Chatbots
- AI Will Not Replace Documentation Teams, but It Will Transform Them
- MCP: Connecting AI to Enterprise Knowledge
- Can AI Agents Become Digital Colleagues?
- From Search to Discovery: Building the Next Generation of Knowledge Systems

[Read the series]({{ "/ai/from-documents-to-intelligence/" | relative_url }}){: .btn .btn--primary}

---

## Articles

{% assign governance_posts = site.governance | sort: "title" %}

{% for post in governance_posts %}

### <a href="{{ post.url | relative_url }}">{{ post.title }}</a>

{{ post.excerpt }}

---

{% endfor %}
