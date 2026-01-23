---
title: "Content Selection in Text Summarization and Simplification"
last_modified_at: 2026-01-05T8:20:02-05:00
classes: wide
categories:
  - phd-thesis
tags:
  - nlp
  - xai
---

On December 17th, Jan Trienes successfully defended his PhD thesis. Over the past years, he investigated content selection in large language models (LLMs). While NLP tasks such as automatic text summarization and simplification can now be solved very effectively, the black-box nature of LLMs makes it difficult to understand and control how they select content.

Key questions addressed in the thesis include:
- what information LLMs choose to keep or omit, 
- how their strategies differ from those of human experts, and 
- how content selection can be adapted to specialized domains such as clinical text.
Since summarization and simplification inevitably involve information loss, an additional challenge lies in enabling readers to recover omitted information when needed.

Jan's thesis addresses these challenges by studying content selection behavior in LLMs and developing methods to make it more transparent, interpretable, and controllable. It introduces an interpretable representation of content grounded in **Questions Under Discussion (QUDs)**, methods for analyzing content salience in summarization models, and presents guidance signals to steer content selection. It also investigates information loss in text simplification and introduces an interactive system that allows users to recover missing information. Finally, it contributes a new dataset for clinical text simplification, supporting non-expert readers and advancing research in domain-specific text simplification.

And since the defense was shortly before Christmas, the occasion was marked with a special gift.

![image-center](/assets/images/posts/Trienes2025-phd-defense.jpeg){: .align-center style="width: 50%"}



<i class="fa fa-user-group" style="color: #7a46eb;"></i>
Thanks to [Jessy Li](https://jessyli.com) (University of Texas, Austin) for serving as an examiner for this thesis.



### Key Publications

<span class="cite-hidden">{% cite Trienes2025_acl_information-salience %}</span>
<span class="cite-hidden">{% cite Trienes2024_acl_infolossqa%}</span>
<span class="cite-hidden">{% cite Trienes2023_inlg_guidance-radiology-report-summarization %}</span>
{% bibliography --cited --group_by none --template bib %}