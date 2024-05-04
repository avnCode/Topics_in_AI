# Blind LLM Truthfulness Assessment(BLTA) :
This paper aims to propose novel techniques for evaluating the truthfulness of large language models
(LLMs) without relying on golden answers. We introduce a new metric, the Negative Sample
Difference (NSD) score, which demonstrates a high correlation with human scores. Our key idea
is to invert the evaluation problem: while it is difficult to generate correct answers for LLM, it is
easier to generate a set of wrong answers shown.

NSD Technique:

![image](https://github.com/avnCode/Topics_in_AI/assets/111170719/96ec8318-d1c3-46b3-8b10-9d5b2837e61e)




Hence, we employ another LLM, Google’s Gemini 1.5 pro(3 ), to generate a set of
intentionally incorrect answers along with their corresponding corrected versions. These pairs are be
utilized to evaluate our main LLM, Llama 3 - 8b.



1)llama2_Inference.ipynb 
This is the code to generate responses of recently launched llama 3-8b on a subset of the TruthFulQA dataset. 

2)Dataset_Creation.ipynb 
This is the code for creating the negative sample datasets using one of the state-of-the-art Langauge Model Google's Gemini-1.5-pro. The dataset created has been uploaded on Hugging Face and is publicly available. 

3) NSD_Scores.ipynb
This is the main code for evaluating the llama-3 using our approach where we calculate the embeddings using a sentence transformer and then use NSD formulation to calculate the scores.

4) Correlation_Scores.ipynb : 
In this code, we first have to calculate the BeRT scores (famous unsupervised evaluation method) and then compare them with NSD Scores based on correlation with human scores.


Human_Evaluation_Scores.xlsx : 

This excel file contains the human scores by three different humans, we then have to average them to get the final scores used for correlation purpose. 

Dataset Link:

Closed Book QA: https://huggingface.co/datasets/avnishkr/topics_in_ai

NSD dataset: https://huggingface.co/datasets/avnishkr/negative_samples_dataset
