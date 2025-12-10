---
layout: splash
title: "xAI Lab, University of Marburg"
permalink: /
author_profile: false
classes:
  - page-home
  - page--research

header:
  overlay_color: "#1b102b"
  overlay_filter: "0.7"
  overlay_image: /assets/images/hero-bg.png  
  actions:
    - label: "Research"
      url: /research/
    - label: "Team"
      url: /team/
    - label: "Publications"
      url: /publications/
    - label: "News"
      url: /posts/

home_feature_row:
  - icon: "fas fa-brain"
    title: "Explainable AI"
    excerpt: "Understanding models, generating explanations, and evaluating interpretability."

  - icon: "fas fa-comments"
    title: "Language & LLMs"
    excerpt: "Capabilities, limitations, and behavior of large language models."

  - icon: "fas fa-cogs"
    title: "Applied Machine Learning"
    excerpt: "ML for high-stakes, safety-critical, and real-world domains."
---

<div class="home-intro">
  <p class="page__lead">
    We study how to make AI systems <strong>transparent, robust, and aligned with people</strong> —
    from interpretable models and trustworthy language technology to applied machine learning in
    sensitive domains.
  </p>
</div>

<h2 class="home-section-heading site-heading accent-color-primary">Our research areas</h2>

{% include feature_row_custom.html features=page.home_feature_row %}

  <p class="home-news-more">
    <a href="/posts/">Read more →</a>
  </p>

<h2 class="home-section-heading site-heading accent-color-secondary">Recent news</h2>

<div class="home-news">
  <div class="home-news-list">
    {% assign recent_posts = site.posts
          | where_exp: "post", "post.draft != true"
          | sort: "date"
          | reverse %}
    {% for post in recent_posts limit:3 %}
      <article class="home-news-item" itemscope itemtype="http://schema.org/CreativeWork">
        <h3 class="home-news-title" itemprop="headline">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h3>

        {% if post.date %}
          <p class="home-news-meta">
            <time datetime="{{ post.date | date_to_xmlschema }}">
              {{ post.date | date: "%B %-d, %Y" }}
            </time>
          </p>
        {% endif %}

        {% if post.excerpt %}
          <p class="home-news-excerpt" itemprop="description">
            {{ post.excerpt | strip_html | truncate: 220 }}
          </p>
        {% endif %}
      </article>
    {% endfor %}
  </div>

  <p class="home-news-more">
    <a href="/posts/">More news →</a>
  </p>
</div>




<h2 class="home-section-heading site-heading accent-color-tertiary">Selected publications</h2>

<span class="cite-hidden">{% cite Le2025_tmlr_spurious-correlations-wo-group-annotations Youssef2025_naacl_detecting-knowledge-edits Trienes2025_acl_information-salience Nauta2023_cvpr_pipnet  Papenmeier2022a_chi_perceived-accuracy%}</span>
{% bibliography --cited --group_by none --template bib %}

  <p class="home-news-more">
    <a href="/posts/">All publications →</a>
  </p>

<!-- <h2 class="home-section-heading site-heading accent-color-quartiary">People & projects</h2>

<p>
  Our work is highly collaborative and interdisciplinary, spanning computer science, medicine,
  public administration, and the social sciences.
</p>

<p>
  <a class="btn" href="/team/">Meet the team →</a>
  <a class="btn btn--inverse" href="/research/">Explore our projects →</a>
</p> -->
