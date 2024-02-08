---
title: "Paper 'Give Me the Facts!' at EMNLP'23"
last_modified_at: 2023-12-05
categories:
  - blog
tags:
  - publication
  - natural language processing
  - survey
---

How do we know what Language Models know? And what are obstacles in using them as knowledge bases? In our recent paper presented at EMNLP {% cite Youssef2023_emnlp_survey-probing %}, we survey methods and datasets for probing PLMs along a categorization scheme. 

![image-center](/assets/images/posts/Youssef2023_emnlp_probing-taxonomy.png){: .align-center style="width: 50%"}


We identify three main prevalent obstacles for using PLMs as knowledge bases:
- PLMs' sensitivity to input queries results in inconsistent fact retrieval.
- Understanding where facts are stored and how they are retrieved is necessary for trustworthy applications.
- Methods for reliably updating knowledge and/or enhancing facts with time-frames.

<div class="bib">
{% bibliography --cited  %}
</div>
