---
title: "PIP-Net - Interpretable Computer Vision (CVPR'23)"
last_modified_at: 2023-06-19T16:20:02-05:00
categories:
  - blog
tags:
  - publication
  - cv
  - XAI
---

Interpretable methods using prototypical patches help AI explain its reasoning to humans. 

<!--more-->

However, current prototype-based methods may not align with human visual perception, causing non-intuitive interpretations.

PIP-Net learns prototypical parts in a self-supervised fashion, better correlating with human vision. PIP-Net's sparse scoring sheet shows evidence for a class based on prototypical parts in an image. It can abstain from decisions for unfamiliar data. No part annotations needed, just image-level labels.

PIP-Net achieves global interpretability, showcasing the entire reasoning process through learned prototypes. Local explanations identify relevant prototypes in an image. Our prototypes correlate with ground-truth object parts. With interpretable prototypes, PIP-Net empowers users to understand decisions intuitively and meaningfully.

**Paper**
<ul class="key_pubs single_pub">
<li> {% reference Nauta2023_cvpr_pipnet %}</li>
</ul>

<iframe width="320" height="180"
        src="https://www.youtube.com/embed/GfQQFQ62SLU"
        frameborder="0"
        allow="autoplay; encrypted-media"
        allowfullscreen></iframe>




