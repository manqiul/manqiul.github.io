---
layout: post
title: Paper Reading - NLP Word Representation
date: 2021-12-13 08:40:16
description: Paper reading notes for LSA, Skip-gram, GloVe, ELMo and BERT.
tags: NLP
categories: PaperReading
toc: true
---

# Distributed representations 1: Word embedding

## Distributed Representations of Words and Phrases and their Compositionality

Before we advance to distributed representations of words, we first need to understand the "sparse representations"

### Understanding Sparse Representations

Examples:

1. One-hot encoding
2. Bag of words: without order information; representation: a length N vector, N is size of vocabulary. Can be represented as Binary Matrix, Count Matrix or TF-IDF Matrix. Can from bag of words to bag of grams.

{% include figure.html path="assets/img/tfidf.png" class="img-fluid rounded z-depth-1" %}

Drawbacks:

1. not captureing sematic correlations
2. vectors are sprse and high-dimensional

Source: DLT lecture notes by Chao Zhang, Georgia Tech

### Understanding Dimension Reduction and Topic Modeling

- Latent Semantic Analysis
  - Using SVD, mapping data into low-dimensional representation by only selecting top k topics
  - Source: [LSA Youtube](https://www.youtube.com/playlist?list=PLroeQp1c-t3qwyrsq66tBxfR6iX6kSslt)

### Understanding word embedding

- word2vec[co-occurrence statistics], Local context window methods
  - CBoW: use a window to predict center word
  - SkipGarm: use center word to predict surrounding words
    - Two layer NN,two weight matrix. each time we will pass one center word, and each word need to be forward pass for k times.
    - the hidden layer doesn't use any activation function, which is directly passed to the output layer. The output layer using softmax probablility, get the word with the highest prob and compare to the output word's on-hot encoding.
- Objective: find word representations that are useful for predicting the surrounding words.

{% include figure.html path="assets/img/wordembe.png" class="img-fluid rounded z-depth-1" %}

source: [skip-gram](https://towardsdatascience.com/skip-gram-nlp-context-words-prediction-algorithm-5bbf34f84e0c), [skip-gram youtube](https://www.youtube.com/watch?v=pOqz6KuvLV8), [paper link](https://arxiv.org/pdf/1301.3781.pdf)

### About this Paper

This paper mainly discussed the extensions of Skip-gram model. First is to use hierarchical softmax to reduce computational complexity. Second is to use negative sampling to reduce noise. Third is to subsampling the frequent word like "a", "the".

source: [word embedding glove](https://jonathan-hui.medium.com/nlp-word-embedding-glove-5e7f523999f6)

## GloVe: Global Vectors for Word Representation

First this paper discussed the drawbacks of LSA and local context window methods:

- LSA: poorly on the word analogy task
- Local context window: poorly utilize statistics of corpus(such as global co-occurrence counts)
- And then it introduces the GloVe:

{% include figure.html path="assets/img/glove.png" class="img-fluid rounded z-depth-1" %}

source: [glove youtube](https://www.youtube.com/watch?v=QoUYlxl1RGI), [glove medium](https://jonathan-hui.medium.com/nlp-word-embedding-glove-5e7f523999f6), [glove csdn](https://blog.csdn.net/coderTC/article/details/73864097)

# Distributed Representation 2: Deep Contextual Representation

## Deep contextualized word representations (ELMo)

[ELMo](https://www.analyticsvidhya.com/blog/2019/03/learn-to-use-elmo-to-extract-features-from-text/)

[ELMo youtube](https://www.youtube.com/watch?v=YZerhaFMPTw&t=366s)

{% include figure.html path="assets/img/elmo.png" class="img-fluid rounded z-depth-1" %}

## BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding

[BERT youtube](https://www.youtube.com/watch?v=xI0HHN5XKDo)

{% include figure.html path="assets/img/BERT1.png" class="img-fluid rounded z-depth-1" %}

{% include figure.html path="assets/img/BERT2.png" class="img-fluid rounded z-depth-1" %}

{% include figure.html path="assets/img/BERT3.png" class="img-fluid rounded z-depth-1" %}

{% include figure.html path="assets/img/BERT4.png" class="img-fluid rounded z-depth-1" %}

{% include figure.html path="assets/img/BERT5.png" class="img-fluid rounded z-depth-1" %}

{% include figure.html path="assets/img/BERT6.png" class="img-fluid rounded z-depth-1" %}

{% include figure.html path="assets/img/BERT7.png" class="img-fluid rounded z-depth-1" %}
