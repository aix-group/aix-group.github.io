---
title: "PIP-Net - Interpretable Computer Vision (CVPR'23)"
last_modified_at: 2023-06-19T16:20:02-05:00
classes: wide
categories:
  - publication
tags:
  - computer vision
  - xai
---

Interpretable methods using prototypical patches help AI explain its reasoning to humans. 

However, current prototype-based methods may not align with human visual perception, resulting in non-intuitive interpretations.

PIP-Net learns prototypical parts in a self-supervised manner that better correlates with human vision. PIP-Net's sparse scoring sheet provides evidence for a class based on prototypical parts within an image. It can abstain from making decisions about unfamiliar data. No part annotations are needed, only image-level labels.

PIP-Net achieves global interpretability by showcasing the entire reasoning process through learned prototypes. Local explanations identify relevant prototypes in an image. Our prototypes correlate with ground-truth object parts. With these interpretable prototypes, PIP-Net enables users to intuitively and meaningfully understand decisions.

{%- include video id="GfQQFQ62SLU" provider="youtube" -%}


### Reference

<span class="cite-hidden">{% cite Nauta2023_cvpr_pipnet %}</span>
{% bibliography --cited --group_by none --template bib %}




