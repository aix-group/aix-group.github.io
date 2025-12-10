---
title: "Annotation-Free Breast Cancer Prediction (CBM)"
last_modified_at: 2025-11-01T12:20:02-05:00
classes: wide
categories:
  - publication
tags:
  - computer vision
  - medicine
---

Most AI models for breast cancer detection assume that each mammogram image, or even each region within an image, has been manually labeled. However, in real hospitals, clinicians only provide a final, case-level diagnosis, and the number of images per exam varies.

We introduce a two-level multi-instance learning (MIL) framework that learns directly from case-level labels without requiring manual image annotation. This method can handle a variable number of images per patient and includes a breast-specific MIL pooling strategy that reflects how mammography is performed.

Our approach achieved performance comparable to models trained using detailed image labels. It also identified which breast, view, and region were most suspicious despite using only weak supervision.
These results demonstrate that **accurate and scalable breast cancer prediction** is possible using the **labels already available in routine clinical practice**.

![image-center](/assets/images/posts/Pathak2025-breast-cancer-mammography.png){: .align-center style="width: 90%"}


### Reference

<span class="cite-hidden">{% cite Pathatk2025_cbmj_breast-cancer-mammography %}</span>
{% bibliography --cited --group_by none --template bib %}

