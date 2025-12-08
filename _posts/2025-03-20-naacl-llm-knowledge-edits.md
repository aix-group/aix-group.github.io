---
title: "Knowledge Editing in Large Language Models (ICML, NAACL'25)"
last_modified_at: 2025-03-20T16:20:02-05:00
classes: wide
categories:
  - publication
tags:
  - nlp
---

In our ever-changing world, the knowledge stored in large language models (LLMs) must be continuously updated as facts evolve.

> The president of the U.S. is ...

## Knowledge Editing

One way of “teaching” new information to LLMs is fine-tuning—updating the entire model with data containing the new facts. This is effective but inefficient.  
A more targeted alternative is **knowledge editing**, which modifies only those parameter regions believed to encode the relevant fact (locate-and-edit methods).  

Other approaches avoid changing model weights entirely. Some store new information in an external memory the LLM can attend to when prompted. A related variant, **in-context editing**, embeds the new knowledge directly in the prompt without altering model parameters.

## Risks

Knowledge editing can also be misused. If an LLM is intentionally updated with harmful or biased information and later deployed in downstream systems, the resulting outputs may be misleading or unsafe.

> An efficient oral cure for corona is a *disinfectant*.

A detailed analysis of why knowledge editing poses security concerns,  what makes today’s AI ecosystem vulnerable, and  which countermeasures are needed  
is provided in our position paper.

## Detecting and Mitigating Knowledge Edits

To ensure trustworthiness, we want to determine whether an LLM has been edited after pre-training. Our work on **detecting parameter edits** shows that such modifications can be identified with high accuracy—even without access to the original, unedited model.

We also study **in-context edits**: cases where the model weights remain unchanged. We show that these can both be detected and **reversed** by inserting special reversal tokens into the prompt.  
For instance, inserting the `<BOS>` token helps reverse edits in GPT-style models.



### References

<span class="cite-hidden">{% cite Youssef2025_icml_position-llm-editing-safetey-risk %}</span>
<span class="cite-hidden">{% cite Youssef2025_naacl_detecting-knowledge-edits %}</span>
<span class="cite-hidden">{% cite Youssef2025b_naacl_reversing-in-context-edits %}</span>

{% bibliography --cited --group_by none --template bib %}

<i class="fa fa-user-group" style="color: #7a46eb;"></i>
Work in collaboration with Cass Zhixue Zhao, University of Sheffield, U.K.  

### Acknowledgement
*The research was partially funded by the German Academic Exchange Service (DAAD) and the German Federal Ministry of Education and Research (BMBF)
under grant number 30001797.*

![image-center](/assets/images/posts/logo-daad.png){: .align-center style="width: 30%"} 
![image-center](/assets/images/posts/logo-bmbf.jpg){: .align-center style="width: 30%"}
