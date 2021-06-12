# Sentiment_Analysis_BERT:

## Overview:

**BERT**, which stands for Bidirectional Encoder Representations from Transformers, is a neural network-based technique for natural language processing pre-training.

BERT builds on top of a number of clever ideas that have been bubbling up in the NLP community recently – including but not limited to Semi-supervised Sequence Learning (by Andrew Dai and Quoc Le), ELMo (by Matthew Peters and researchers from AI2 and UW CSE), ULMFiT (by fast.ai founder Jeremy Howard and Sebastian Ruder), the OpenAI transformer (by OpenAI researchers Radford, Narasimhan, Salimans, and Sutskever), and the Transformer (Vaswani et al).

## Model Architecture:
The paper presents two model sizes for BERT:

* BERT BASE – Comparable in size to the OpenAI Transformer in order to compare performance
* BERT LARGE – A ridiculously huge model which achieved the state of the art results reported in the paper

![Image of BERT](https://github.com/janmejaybhoi/Sentiment_Analysis_Transformers/blob/main/img/bert-base-bert-large-encoders.png)

Both BERT model sizes have a large number of encoder layers (which the paper calls Transformer Blocks) – twelve for the Base version, and twenty four for the Large version. These also have larger feedforward-networks (768 and 1024 hidden units respectively), and more attention heads (12 and 16 respectively) than the default configuration in the reference implementation of the Transformer in the initial paper (6 encoder layers, 512 hidden units, and 8 attention heads).
