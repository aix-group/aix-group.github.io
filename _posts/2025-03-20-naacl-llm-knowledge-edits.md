---
title: "Knowledge Editing in Large Language Models (NAACL'25)"
last_modified_at: 2025-03-20T16:20:02-05:00
categories:
  - blog
tags:
  - publication
  - natural language processing
---


In our ever-changing world, knowledge of language models (LLMs) needs to be constantly updated. 
Facts change and LLMs need to reflect this.

> The president of the U.S. is ...

## Knowledge Editing

One way of 'teaching' new knowledge to LLMs is fine-tuning, i.e. training on the new facts to overwrite the old facts. But this is very inefficient. More recently, another set of methods has emerged: knowledge editing methods. These methods identify where the knowledge is stored in the LLM parameters and then only adapt these parameters (locate-and-edit methods).  Another possibility is to store the new knowledge in a separate memory and to make the LLM refer to this memory when the prompt refers to it. A special version of this is in-context editing, where the knowledge is simply added to the prompt.


## Risks

But what if a language model is updated with malicious intent? What if, for example, biases or misinformation are introduced? And then these LLMs are uploaded to platforms and used in applications? 

> An efficient oral cure for corona is a *disinfectant*. 

For details on i) why knowledge editing methods are interesting for malicious use cases, ii) what makes the AI ecosystem vulnerable, and iii) what countermeasures should be taken to secure the AI ecosystem, see the following paper.


<i class="fa fa-book-reader" style="font-size:12px;color: #7a46eb;"></i> {% reference youssef2025positioneditinglargelanguage --file preprints  %} [PDF](https://arxiv.org/abs/2502.02958) 


## Detecting and Mitigating Knowledge Edits

For a given LLM, we want to know if it has been edited after pre-training. We could then verify whether the edit is justified, and reverse it. 

In our paper, we show that detecting edits to model parameters is possible with high accuracy, and that one not necessarily need the original (unedited) LLM to do so.

<i class="fa fa-book-reader" style="font-size:12px;color: #7a46eb;"></i> {% reference Youssef2025_naacl_detecting-knowledge-edits  %} [PDF](https://aclanthology.org/2025.naacl-long.492.pdf) 

We further find that in-context edits, where model parameters are not changed, can be detected, and that such edits can be reversed by inserting special reversal tokens. 
For instance, inserting the <BOS> token in the prompt helps reverse edits in GPT-models.

<i class="fa fa-book-reader" style="font-size:12px;color: #7a46eb;"></i> {% reference Youssef2025b_naacl_reversing-in-context-edits   %} [PDF](https://aclanthology.org/2025.naacl-long.630.pdf) 

---

*<i class="fa fa-user-group" style="color: #7a46eb;"></i> Work in collaboration with Cass Zhixue Zhao, University of Sheffield, U.K. 
 <i class="fa fa-link" style="color: #7a46eb;"></i>[Website]( https://casszhao.github.io/cass/)*


*The research was partially funded by the German Academic Exchange Service (DAAD) and the German Federal Ministry of Education and Research (BMBF)
under grant number 30001797.*

![image-center](/assets/images/posts/logo-daad.png){: .align-center style="width: 30%"} ![image-center](/assets/images/posts/logo-bmbf.jpg){: .align-center style="width: 30%"}



