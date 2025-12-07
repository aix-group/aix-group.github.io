---
title: "LLMs for Counterfactuals (EMNLP'24)"
last_modified_at: 2024-11-10T16:20:02-05:00
classes: wide
categories:
  - publication
tags:
  - nlp
---

_"What minimal changes to this text would cause the text classifier to change its prediction?"_

Counterfactual texts, i.e. minimal changes to inputs that alter a model's predictions, are an important technique in Explainable AI (XAI) for understanding model behaviour. 

![image-center](/assets/images/posts/Nguyen2024_emnlp_teaser.png){: .align-center style="width: 50%"}


Bach and Paul evaluated the ability of open-source and closed-source LLMs (GPT-4, GPT-3.5, LLAMA-2, Mistral) to generate counterfactual texts in a variety of tasks (sentiment analysis, natural language inference, and hate speech detection).

Results in a nutshell:
- LLMs excel at generating fluent counterfactuals, but often make excessive changes.
- Generating counterfactuals for sentiment analysis is easier than for natural language inference and hate speech detection, where label reversal is less reliable.
- Human-generated counterfactuals outperform LLM-generated counterfactuals for data augmentation.
- Using LLMs to automatically assess the quality of generated counterfactuals is prone to bias: GPT-4 in particular tends to favour its own results.


![image-center](/assets/images/posts/Nguyen2024_emnlp_poster-in-action.jpg){: .align-center style="width: 50%"}

<br/>
**Links**

<i class="fa fa-book-reader" style="font-size:12px;color: #7a46eb;"></i>  {% reference Nguyen2024_emnlp_llms-for-generating-counterfactuals  %}
[PDF](https://aclanthology.org/2024.findings-emnlp.870.pdf) 

<i class="fa-brands fa-github" style="font-size:12px;color: #7a46eb;"></i>  [Source Code](https://github.com/aix-group/llms-for-cfs/)


