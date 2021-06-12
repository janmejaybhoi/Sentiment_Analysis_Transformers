# Sentiment_Analysis_BERT:
![Image of BERT](https://github.com/janmejaybhoi/Sentiment_Analysis_Transformers/blob/main/img/bert.png)
## Overview:

**BERT**, which stands for Bidirectional Encoder Representations from Transformers, is a neural network-based technique for natural language processing pre-training.
It is designed to pre-train deep bidirectional representations from unlabeled text by jointly conditioning on both left and right context. As a result, the pre-trained BERT model can be fine-tuned with just one additional output layer to create state-of-the-art models for a wide range of NLP tasks.

BERT builds on top of a number of clever ideas that have been bubbling up in the NLP community recently – including but not limited to Semi-supervised Sequence Learning (by Andrew Dai and Quoc Le), ELMo (by Matthew Peters and researchers from AI2 and UW CSE), ULMFiT (by fast.ai founder Jeremy Howard and Sebastian Ruder), the OpenAI transformer (by OpenAI researchers Radford, Narasimhan, Salimans, and Sutskever), and the Transformer (Vaswani et al).

## Model Architecture:
The paper presents two model sizes for BERT:

* BERT BASE – Comparable in size to the OpenAI Transformer in order to compare performance
* BERT LARGE – A ridiculously huge model which achieved the state of the art results reported in the paper

![Image of BERT](https://github.com/janmejaybhoi/Sentiment_Analysis_Transformers/blob/main/img/bert-base-bert-large-encoders.png)

Both BERT model sizes have a large number of encoder layers (which the paper calls Transformer Blocks) – twelve for the Base version, and twenty four for the Large version. These also have larger feedforward-networks (768 and 1024 hidden units respectively), and more attention heads (12 and 16 respectively) than the default configuration in the reference implementation of the Transformer in the initial paper (6 encoder layers, 512 hidden units, and 8 attention heads).

### Model Input and Output:

The first input token is supplied with a special [CLS] token for reasons that will become apparent later on. CLS here stands for Classification.

Just like the vanilla encoder of the transformer, BERT takes a sequence of words as input which keep flowing up the stack. Each layer applies self-attention, and passes its results through a feed-forward network, and then hands it off to the next encoder.

Each position outputs a vector of size hidden_size (768 in BERT Base). For the sentence classification purpose, we focus on the output of only the first position (that we passed the special [CLS] token to).

![Image of BERT](https://github.com/janmejaybhoi/Sentiment_Analysis_Transformers/blob/main/img/bert-output-vector.png)

### Task specific-Models:
The BERT paper shows a number of ways to use BERT for different tasks.
![Image of BERT](https://github.com/janmejaybhoi/Sentiment_Analysis_Transformers/blob/main/img/bert-tasks.png)
