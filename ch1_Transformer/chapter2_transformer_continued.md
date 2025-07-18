# Chapter 2: Transformer Continued


## Tokenization:

Andrej Karpathy Tutorial: https://www.youtube.com/watch?v=zduSFxRajkE&t=57s

Some notes recommended by William Brown's Generative AI Handbook (Chapter 13): https://genai-handbook.github.io/

Some key aspects of tokenization:</br>
(1) A lot of errors can be traced back to tokenization, including GPT's different performance on different languages </br>
(2) Words need to be represented as integers (typically utf-8 encoding) </br>
(3) Use BPE (byte pair encoding) algorithm to encode the words, high frequency byte pairs are grouped together into a single token, the benefit of this is within the same context length, now the attention mechanism can see more text (more context, better learning) </br>
(4) ChatGPT also uses special tokens and regular expression to break words down and then apply BPE </br>



## Positional Encoding:

Some notes recommended by William Brown's Generative AI Handbook (Chapter 14): https://genai-handbook.github.io/

## Bert:

Video (in Chinese): https://www.bilibili.com/video/BV1PL411M7eQ/?spm_id_from=333.337.search-card.all.click&vd_source=75e16b30403690b6ad4ccdb9c2dbde46

Summary:
Bert uses a bidirectional structure. It gives you context before and after a token and train the model to infer what the masked token is. It uses transfomer as the architecture. Its training contains two phases: (1) pretraining on large corpus of document data (2) fine-tuning. During training, it is trained to solve two tasks: (1) given context, predict what the masked token is, (2) given two sentences A and B, determine whether B is the next sentence after A. 

Bert's historical importance is showing a deep neural network architecture is capable of performing well in a wide range of NLP tasks. However, since Bert's bidirectional structure, it is not good at performing autoregressive generation or machine translation. 


## ViT:

Video: https://www.bilibili.com/video/BV15P4y137jb/?spm_id_from=333.337.search-card.all.click&vd_source=75e16b30403690b6ad4ccdb9c2dbde46


