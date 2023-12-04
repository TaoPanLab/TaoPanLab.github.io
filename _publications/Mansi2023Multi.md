---
layout: publication
publication: true
key: Mansi2023Multi
redirect: https://msakarvadia.github.io/memory_injections/
---

## Abstract
Answering multi-hop reasoning questions requires retrieving and synthesizing information from diverse sources. Large Language Models (LLMs) struggle to perform such reasoning consistently. Here we propose an approach to pinpoint and rectify multi-hop reasoning failures through targeted memory injections on LLM attention heads. First, we analyze the per-layer activations of GPT-2 models in response to single and multi-hop prompts. We then propose a mechanism that allows users to inject pertinent prompt-specific information, which we refer to as "memories," at critical LLM locations during inference. By thus enabling the LLM to incorporate additional relevant information during inference, we enhance the quality of multi-hop prompt completions. We show empirically that a simple, efficient, and targeted memory injection into a key attention layer can often increase the probability of the desired next token in multi-hop tasks, by up to 424%.


{% include video.html title="Video Presentation" url="https://www.youtube.com/embed/VyXQHdrcj2Q?si=TGILiKGcnWTqgfpz" %}

## Call for Collaboration 
If this work is interesting to you and you would like to collaborate, please feel free to reach out to <a href="mailto: sakarvadia@uchicago.edu">sakarvadia@uchicago.edu</a>. Some ideas we are excited about are (but not limited to):
* Automating memory selections from external knowledge sources (e.g. knowledge graphs, vector databases)
* Erasing memories during model inference
* Applying memory injections to additional model architectures

