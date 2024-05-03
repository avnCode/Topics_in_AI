# Topics_in_AI
This paper aims to propose novel techniques for evaluating the truthfulness of large language models
(LLMs) without relying on golden answers. We introduce a new metric, the Negative Sample
Difference (NSD) score, which demonstrates a high correlation with human scores. Our key idea
is to invert the evaluation problem: while it is difficult to generate correct answers for LLM, it is
easier to generate set of wrong answers shown.

Hence ,we employ another LLM, Google’s Gemini 1.5 pro(3 ), to generate a set of
intentionally incorrect answers along with their corresponding corrected versions. These pairs are be
utilized to evaluate our main LLM, Llama 3 - 8b.

Dataset Link:

Closed Book QA: https://huggingface.co/datasets/avnishkr/topics_in_ai

NSD dataset: https://huggingface.co/datasets/avnishkr/negative_samples_dataset
