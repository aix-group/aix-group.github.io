---
title: "Unlearning spurious correlations (TMLR)"
last_modified_at: 2025-04-09T8:20:02-05:00
categories:
  - blog
tags:
  - publication
  - representation learning
  - computer vision
---

"This is a cow, because the background is a meadow."

<!--more-->

Machine learning models often rely on **spurious correlations** — features that are strongly associated with class labels but lack any causal connection. For example, a model might misclassify a seabird as a landbird simply because it is seen standing on the ground, fail to recognize a cow on a beach due to the atypical background, or erroneously detect pneumonia in an X-ray image due to the presence of hospital-specific markers. A common way to mitigate such behavior is to retrain models using specially curated datasets that explicitly include such counterexamples—e.g., images of cows on beaches, landbirds in forested settings, or X-rays without markers. However, constructing these datasets requires prior knowledge of the spurious correlations and is often impractical or infeasible.

We propose **PruSC (Pruning Spurious Correlations)** — a method that addresses spurious correlations without requiring any prior annotation or knowledge of the spurious features. Moreover, PruSC is capable of handling multiple spurious attributes simultaneously.

![image-center](/assets/images/posts/Le2025_tmlr_spurious_idea.png){: .align-center style="width: 70%"}


The key insight behind PruSC is that training neural networks via Empirical Risk Minimization (ERM) often results in representation space clusters that are shaped by spurious correlations. To mitigate this, PruSC introduces a **supervised contrastive loss** designed to break apart these spurious clusters, encouraging the network to group samples based purely on class-specific features.

Empirical results show that PruSC outperforms existing annotation-free approaches and achieves worst-group accuracy on par with methods that rely on group annotations. These findings suggest that it is possible to extract a subnetwork from a dense model that depends solely on invariant features for classification—effectively eliminating the influence of spurious correlations.


<i class="fa fa-book-reader" style="font-size:12px;color: #7a46eb;"></i> {% reference Le2025_tmlr_spurious-correlations-wo-group-annotations  %} [PDF](https://openreview.net/pdf?id=EEeVYfXor5) 

<i class="fa-brands fa-github" style="font-size:12px;color: #7a46eb;"></i>  [Source Code](https://github.com/aix-group/prusc)


