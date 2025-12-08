---
layout: splash
title: "xAI Lab, University of Marburg"
permalink: /
author_profile: false

header:
  overlay_color: "#1b102b"
  overlay_filter: "0.75"
  # If you add a background image, uncomment and point this to it:
  # overlay_image: /assets/images/hero-bg.jpg
  actions:
    - label: "Research"
      url: /research/
    - label: "Team"
      url: /team/
    - label: "Publications"
      url: /publications/
    - label: "News"
      url: /blog/

intro: |
  We develop explainable, trustworthy, and user-centric AI –
  combining methods from machine learning, natural language processing,
  and human-centered evaluation.

feature_row:
  - image_path: /assets/images/research/explainable-ai.svg
    alt: "Explainable AI"
    title: "Explainable AI"
    excerpt: "Understanding models, generating explanations, and evaluating interpretability."
    url: "/research/#explainable-ai"

  - image_path: /assets/images/research/language-llms.svg
    alt: "Language & LLMs"
    title: "Language & LLMs"
    excerpt: "Capabilities, limitations, trustworthiness, and evaluation of language models."
    url: "/research/#language-and-llms"

  - image_path: /assets/images/research/applied-ml.svg
    alt: "Applied Machine Learning"
    title: "Applied Machine Learning"
    excerpt: "ML for sensitive, safety-critical, and real-world domains."
    url: "/research/#applied-machine-learning"
---

{% include feature_row %}

<h2 class="home-section-heading">Recent News</h2>

<div class="archive">
  {% assign recent_posts = site.posts | slice: 0, 3 %}
  {% for post in recent_posts %}
    <article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
      <h3 class="archive__item-title" itemprop="headline">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>

      {% if post.date %}
        <p class="page__meta">
          <time datetime="{{ post.date | date_to_xmlschema }}">
            {{ post.date | date: "%B %-d, %Y" }}
          </time>
        </p>
      {% endif %}

      {% if post.excerpt %}
        <p class="archive__item-excerpt" itemprop="description">
          {{ post.excerpt | strip_html | truncate: 180 }}
        </p>
      {% endif %}
    </article>
  {% endfor %}
</div>

<p class="home-more-link">
  <a href="/blog/">More news →</a>
</p>
