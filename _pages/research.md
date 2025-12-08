---
layout: single
title: "Research"
permalink: /research/
classes:
  - wide
  - page--research
feature_row_custom:
  - icon: "fas fa-brain"
    title: "Explainable AI"
    excerpt: "Understanding models, generating explanations, and evaluating interpretability."
    url: "#explainable-ai"
  - icon: "fas fa-comments"
    title: "Language & LLMs"
    excerpt: "Capabilities, limitations, trustworthiness, and evaluation of language models."
    url: "#language-and-llms"
  - icon: "fas fa-cogs"
    title: "Applied Machine Learning"
    excerpt: "ML for sensitive, safety-critical, and real-world domains."
    url: "#applied-machine-learning"
---

Our lab develops **explainable, trustworthy, and user-centric AI systems** by integrating *machine learning*, *natural language processing*, and *human-centered evaluation*. We tackle real-world challenges where AI decisions impact people—whether in healthcare, administrative processes, or human-AI collaboration.

{% include feature_row_custom.html features=page.feature_row_custom %}

## Explainable AI {#explainable-ai}

> “Why does the model think this patient has stage 3 cancer?”
> “Why was my credit application rejected, and what can I do about it?”

When AI models support critical decisions, **transparency** and **accountability** become essential. Our work in **eXplainable AI (XAI)** develops:
- Intrinsically interpretable models
- Conversational XAI systems
- Rigorous evaluation standards for explanations
- Methods to understand AI-user interactions

**Key Publications**
{% reference Nauta2023_cvpr_pipnet %}
{% reference Papenmeier2022_tochi_trust-accuracy-explanations %}
{% reference Nauta2023_csur_evaluating-xai-survey %}
{% reference Nguyen2023_wcxai_xagent %}
{% reference Papenmeier2022a_chi_perceived-accuracy %}
{% reference Le2023_ijcai_benchmarking-xai %}


## Language & LLMs {#language-and-llms}

Language is messy, individualized, and context-dependent. Our research explores:
- **Capabilities and limitations** of large language models (LLMs)
- **Domain-specific NLP tasks**: text simplification, de-identification, and structuring of medical reports
- **Trustworthy evaluation** of language generation

If you want to know what mammoths have to do with natural language generation, check out this [ICLR Blog post](https://iclr-blog-track.github.io/2022/03/25/PPLM/).

**Key Publications**
{% reference Youssef2023_emnlp_survey-probing %}
{% reference Pathak2019_tcbb_post-structuring-radiology-reports %}
{% reference Trienes2023_inlg_guidance-radiology-report-summarization %}
{% reference Zerhoudi2022_cikm_simiir20framework %}


## Applied Machine Learning {#applied-machine-learning}

> *“Theory and practice sometimes clash. And when that happens, theory loses. Every single time.”*
> — Linus Torvalds

Applying ML in real-world settings requires addressing:
- **Data quality** and annotation challenges
- **Legal and ethical compliance** (e.g., [privacy-preserving compute infrastructures](https://ieeexplore.ieee.org/document/9750320))
- **Multi-modal data** (text, structured data, 2D/3D imagery, sensor data)

The medical domain serves as an example where robustness and reliability are paramount.

**Key Publications**
{% reference Pathak2021_aim_automatic-sleep-scoring %}
{% reference Nauta2019_mdpi-make_causal-discovery-tcdf %}
{% reference Vries2021_osteoporosis_risk-assessment-for-future-fractures %}
{% reference Paalvast2022_aim_radiology-report-generation %}
