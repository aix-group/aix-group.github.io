---
title: "Tracing and Reversing Edits in LLMs (ICLR'26)"
last_modified_at: 2026-04-20T16:20:02-05:00
classes: wide
categories:
  - publication
tags:
  - nlp
  - xai
---


Knowledge editing is used to update large language models when facts change. Instead of retraining an entire model, editing methods can directly modify the model’s parameters so that it responds with new information.

_But what happens when such edits are unwanted, hidden, or malicious?_

In this paper, we study how knowledge edits can be detected and undone. We introduce two tasks: *tracing edits*, where the goal is to recover which fact was inserted into a model from its edited weights, and *reversing edits*, where the goal is to restore the model’s original behavior.

Our results show that edits leave recognizable traces in model weights. By analyzing low-rank approximations of the parameter update, we can often identify the edited object and reverse the change while preserving much of the model’s original performance. This provides a step toward safer and more accountable use of knowledge editing in LLMs.

![image-center](/assets/images/posts/Youssef2026_iclr_tracing-and-reversing-edits-overview.png){: .align-center style="width: 90%"}

<i class="fa fa-link" style="color: #7a46eb;"></i> [Paper and video](https://iclr.cc/virtual/2026/poster/10011004)



### References
<span class="cite-hidden">{% cite Youssef2026_iclr_tracing-and-reversing-edits %}</span>



{% bibliography --cited --group_by none --template bib %}

<i class="fa fa-user-group" style="color: #7a46eb;"></i>
Work in collaboration with Cass Zhixue Zhao, University of Sheffield, U.K.  