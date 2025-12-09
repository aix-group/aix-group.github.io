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
    excerpt: "Intrinsically interpretable models, explanation evaluation, user centric-aspects."
    url: "#explainable-ai"

  - icon: "fas fa-comments"
    title: "Language & LLMs"
    excerpt: "Capabilities, limitations, and behavior of Large Language Models."
    url: "#language-and-llms"

  - icon: "fas fa-cogs"
    title: "Applied ML"
    excerpt: "Machine learning in sensitive, safety-critical, and real-world domains."
    url: "#applied-machine-learning"
---


Our lab develops **explainable, trustworthy, and user-centric AI systems**. We combine machine learning, natural language processing, and human-centered evaluation to design models that people can actually understand and rely on.

We focus on real-world settings where AI decisions have meaningful impact — from healthcare and public administration to everyday human–AI collaboration.

{% include feature_row_custom.html features=page.feature_row_custom %}

## Explainable AI {#explainable-ai}

> “Why does the model think this patient has stage 3 cancer?”
> “Why was my credit application rejected, and what can I do about it?”


Machine learning systems are deployed in settings where people must understand, trust, and sometimes contest automated decisions. In our Explainable AI (XAI) work, we design methods that make model reasoning transparent and evaluate how explanations affect real users.

Our Explainable AI research develops **interpretable models**, {% cite Nauta2021_cvpr_prototree %}; {%cite Nauta2023_cvpr_pipnet %},
creates **conversational agents for explanations**, {% cite Nguyen2023_wcxai_xagent %},
examines **evaluation of explanation quality**, {% cite Nauta2023_csur_evaluating-xai-survey %}; {% cite Le2023_ijcai_benchmarking-xai %},
and studies **how people perceive errors and uncertainty**, {% cite Papenmeier2022a_chi_perceived-accuracy%}; {%cite Papenmeier2022_tochi_trust-accuracy-explanations %}.



## Language & LLMs {#language-and-llms}

Language is messy, individualized, and deeply context-dependent. Our work investigates how large language models (LLMs) represent information, how they can be adapted or constrained, and how we can evaluate their outputs in reliable, human-centered ways.

Our research in this area examines **LLM representations and probing**, 
{% cite Youssef2023_emnlp_survey-probing %} {%cite Youssef2025_icml_position-llm-editing-safetey-risk %}, develops **methods for text generation and summarization**, 
{% cite Trienes2023_inlg_guidance-radiology-report-summarization %}, {% cite Koras2024_ecir_bass-replication %}, {% cite Nguyen2024_emnlp_llms-for-generating-counterfactuals %}
advances **techniques for understanding LLM behavior** {%cite Trienes2025_acl_information-salience%} {%cite Trienes2024_acl_infolossqa %} 
and builds **domain-specific NLP tools for healthcare**, 
{% cite Trienes2022_tsar_patient-friendly-clinical-notes %}, {% cite Pathak2019_tcbb_post-structuring-radiology-reports %}, {% cite Libbi2021_futint_synthetic-data-deidentification %}.

If you want to know what mammoths have to do with natural language generation, check out this  
[ICLR Blog post](https://iclr-blog-track.github.io/2022/03/25/PPLM/) on Plug-and-Play Language Models.




## Applied Machine Learning {#applied-machine-learning}

> *“Theory and practice sometimes clash. And when that happens, theory loses. Every single time.”*
> — Linus Torvalds

We collaborate with partners in medicine, public administration, and industry to build machine learning systems that operate reliably under real-world constraints. Beyond accuracy, our models must be interpretable, fair, robust, and aligned with domain needs.

Our applied work includes developing **decision-support models**, {% cite Pathatk2025_cbmj_breast-cancer-mammography %}, {% cite Vries2021_osteoporosis_risk-assessment-for-future-fractures %}, creating **AI systems that support users in practice**, such as **student-facing chatbots**, {% cite Trienes2025_emnlp_marcel-chatbot %}, and tools that **assist clinical workflows**, {% cite Trienes2023_inlg_guidance-radiology-report-summarization %},  
as well as methods enabling **legally compliant data sharing**, {% cite Libbi2021_futint_synthetic-data-deidentification %}.
We also investigate **pressing challenges in applied ML**, including **shortcut learning and spurious correlations**, {% cite Le2025_tmlr_spurious-correlations-wo-group-annotations %}, {% cite Nauta2022_diagnostics_short-cut-learning-skin-cancer %}.

## References

{% bibliography --cited --group_by none --template bib %}

