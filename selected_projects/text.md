---
title: "Learning representation of text"
permalink: /selected_projects/text_representation/
author_profile: true
---

I'm interested in learning data representations of text in both traditional and social media (i.e., user-generated content) for text understanding and generation. I'm interested in both distributional approaches (e.g., statistical topic model LDA) and distributed approaches (e.g., text embedding through neural networks).

Distributional approaches: statistical topic model LDA
======
During my Ph.D study, I've been working on statistical topic models for text modeling. Statistical topic models such as LDA have been very popular for text modeling due to its simplicity, effectiveness and interpretability. They have been applied to a vast variety of dat sets, contexts, and tasks to varying degrees of success. However, to date there is almost no formal theory explicating LDA's behavior. We systematically study the limiting factors of topic modeling. We present theorems elucidating the posterior contraction rates of the topics as the amount of data increases, and a thorough supporting empirical study using both synthetic and real-world data. Based on these results, we provide practical guidance on how to identify suitable data sets for topic models, and how to specify particular model parameters (Tang et al. 2014).

In the case of conducting topic modeling on user-generated content, in which the lengths of the documents are very short, the vocabulary size is very large, we propose to use the context information (e.g., user, time, location) information to complement the data sparsity. We define different types of contexts as different partitions of the corpus, forming multiple views of the data. We propose a multi-view topic modeling approach to infer both the consensus topics across multiple views and view-specific topics (Tang et al. 2013).

Distributed approaches: neural approaches
======
Recently, I'm very interested in the distributed representations of text,  which are attracting a lot of attention recently in both machine learning and natural language processing communities. The goal is to learning the representations of text of different levels of granularities such as words, phrases, sentences and documents. We've studied both unsupervised and semi-supervised text embeddings.

**Unsupervised text embeddings.** We propose to learn unsupervised text embeddings through embedding different types of text networks, which encode different levels of word co-occurrence information (Tang et al. 2015). Specifically, given a text corpus, we construct the word-word network, which encodes the local-context level word co-occurrences and the word-document network, which encodes the document-level word co-occurrences.  The embeddigns of words and documents are obtained by embedding the two networks thorough our proposed network embedding model LINE (Tang et al. 2015). Experimental results show that the word embeddings learned through embedding the word-word co-occurrence network with LINE outperform Skipgram, and our approach is much more efficient on large-scale data sets.  The embeddings of documents learned through embedding the word-document network outperform the ParagraphVec.

**Semi-supervised text embeddings.** Besides unsupervised text embeddings, we also study the semis-supervised text embeddings (Tang et al. 2015). Take the text categorization as an example, we encode the supervised information as a word-category network and the unsupervised information as word-word and word-document networks. By jointly embedding the three networks, we are able to exploit both unsupervised and supervised information and learn semi-supervised text embeddings.

Though the text embeddings learned by the above approaches work pretty well in various applications, they ignore the order of the words, which are very important in some applications. Currently, I'm also very interested in the sequence model recurrent neural networks (RNN) . I'm interested in developing generative models for text understanding and generation. 

Publications:
======
* **Jian Tang,** Meng Qu and Qiaozhu Mei. [PTE: Predictive Text Embedding through Large-scale Heterogeneous Text Networks](https://arxiv.org/abs/1508.00200). In KDD'15.
* **Jian Tang,** Meng Qu, Mingzhe Wang, Ming Zhang, Jun Yan and  Qiaozhu Mei. [LINE: Large-scale Information Network Embedding](https://arxiv.org/abs/1503.03578). In WWW'15. <span style="color:red">(Most cited paper of WWW'15)</span>
* **Jian Tang,** Ming Zhang, and Qiaozhu Mei. [One theme in all views: Modeling consensus topics in multiple contexts](https://dl.acm.org/citation.cfm?id=2487682). In KDD'13
* **Jian Tang,** Zhaoshi Meng, XuanLong Nguyen, Qiaozhu Mei and Ming Zhang. [Understanding the limiting factors of topic modeling via posterior contraction analysis](http://proceedings.mlr.press/v32/tang14.pdf). In proceedings of the 31st International Conference on Machine Learning (ICML), Beijing, June 2014. <span style='color:red'>(Best paper award, 1/1500)</span>
* **Jian Tang,** Ming Zhang, and Qiaozhu Mei. ["Look Ma, No Hands!" A parameter-free topic model](https://arxiv.org/abs/1409.2993). 2014.
