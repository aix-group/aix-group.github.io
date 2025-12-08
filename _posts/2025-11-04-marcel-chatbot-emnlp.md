---
title: "Student Chatbot Marcel (EMNLP'25)"
last_modified_at: 2025-12-04T8:20:02-05:00
classes: wide
categories:
  - publication
tags:
  - nlp
  - education
---

At this year’s EMNLP in Suzhou, China, Jan Trienes presented *Marcel*—a RAG-based conversational agent built to handle enrollment questions at Marburg University {% cite Trienes2025_emnlp_marcel-chatbot %}. The project grew out of a simple observation: as our M.Sc. Data Science program expanded, so did the repetitive workload for staff answering student inquiries about deadlines, prerequisites, and language requirements. So, we set up a [project]({% post_url 2024-04-01-marflex-marcel-project %}).

### How Marcel Works
- **Precision answers**: Pulls up-to-date information from university resources (websites, exam regulations) using retrieval-augmented generation.
- **Designed for real-world use**: A **Vue.js frontend** and **FastAPI backend** make it adaptable, while an admin dashboard lets non-technical staff adjust FAQ retrieval.
- **Privacy-first**: Runs on-premise in containers, with no external dependencies.

Marcel is already in use, but we’re always open to suggestions—or collaborations with other institutions facing similar challenges.

{%- include video id="uLCB2R6szz4" provider="youtube" -%}

### Reference
{% bibliography --cited --group_by none --template bib %}






