
---
layout: post
title: "RAG and other elements in the world of Natural Language Processing"
date: 2024-08-16 10:24:00 +0900
author: Tri Thanh
categories: AI Engineer, Researching
---

## Author: Tri Thanh

Natural Language Processing (NLP) is one of the two largest fields within Artificial Intelligence (AI). The advances of Large Language Models (LLMs) have unlocked significant potential in this domain, particularly in downstream tasks such as chatbots, translation, question answering, and more. However, direct application of LLMs in production has revealed inherent weaknesses that adversely affect task performance. These weaknesses include difficulties in expanding or revising memory, challenges in providing clear explanations for their predictions, and the potential to produce "hallucinations" [[1]](#1).
To address these limitations, the Retrieval-Augmented Generation (RAG) model [[1]](#2) was introduced, emerging as the state-of-the-art (SOTA) approach in NLP-related tasks. Additionally, concepts like BM25 Encoder [[2]](#1) and Hybrid Search [[3]](#1) have become essential tools in the implementation and effectiveness of RAG.

# Retrieval-Augmented Generation (RAG)

Retrieval-Augmented Generation (RAG) is a method designed to enhance the efficiency of retrieving information from a query before processing it through Large Language Models (LLMs) to deliver the desired information to users. RAG comprises two main components: the Retriever and the Generator. The objectives of these components are as follows:

-   **Retriever**: This component functions as an extraction mechanism, gathering relevant information related to the query, such as context, necessary data, and other associated details.
   
-   **Generator**: Typically an LLM, the Generator's role is to produce information based on the extractions provided by the Retriever.

Together, the Retriever and Generator address challenges faced by previous solutions that relied solely on LLMs, thereby enhancing the practical applicability of LLMs in real-world scenarios.
![RAG process Overview](https://drive.google.com/file/d/14WsVBTd940YEvRttjnYT-gUA97WMSpwG/view?usp=drive_link)


# BM25 Encoder

The BM25 Encoder is an advanced implementation of the BM25 algorithm, which is widely used in information retrieval systems to rank documents based on their relevance to a query. BM25 itself is a probabilistic retrieval function that belongs to the family of bag-of-words retrieval models, particularly effective in search engines and document retrieval systems.

## Mechanism

BM25 scores each document based on the sum of the relevance of each query term. It assigns higher relevance scores to documents that contain the query terms with higher frequency, but it also applies diminishing returns to very frequent terms, ensuring that a single word repeated many times doesn't overly influence the score.

## Key Concepts

-   **Term Frequency (TF)**: The number of times a term appears in a document.
-   **Inverse Document Frequency (IDF)**: A measure of how important a term is across a set of documents. It helps to downweight common terms that appear in many documents.
-   **Document Length Normalization**: Adjusts the score based on the length of the document, giving shorter documents a higher score for the same query term frequency.


# Pinecone Hybrid Search


Pinecone Hybrid Search was developed with the goal of combining two fundamental search methods: Dense Search and Sparse Search. This combination seeks to leverage the strengths of both approaches while mitigating their inherent weaknesses. Specifically:

-   **Dense Search**: Exhibits higher performance in tasks within domains that have been fine-tuned. However, it performs poorly in tasks outside of these fine-tuned domains and requires large datasets and lengthy training times for fine-tuning.
-   **Sparse Search**: Adapts well to tasks outside of the fine-tuned domains and can effectively extract context relevant to the query. However, it tends to underperform compared to embedding models in domain-specific tasks that have been fine-tuned.
   
Pinecone Hybrid Search successfully integrates the advantages of both Dense and Sparse Search, providing superior retrieval capabilities compared to using either method alone.

# Summary
These terms refer to methods that are commonly used in the processing of NLP tasks today. Additionally, there are numerous other methods and libraries that support these tasks, which will be discussed in subsequent articles.

## References


<a id="1">[1]</a> Lewis, P., Perez, E., Piktus, A., Petroni, F., Karpukhin, V., Goyal, N., ... & Kiela, D. (2020). Retrieval-augmented generation for knowledge-intensive nlp tasks. _Advances in Neural Information Processing Systems_, _33_, 9459-9474.
<a id="2">[2]</a> Robertson, S. E., & Walker, S. (1994). Some simple effective approximations to the 2-poisson model for probabilistic weighted retrieval. In _SIGIR’94: Proceedings of the Seventeenth Annual International ACM-SIGIR Conference on Research and Development in Information Retrieval, organised by Dublin City University_ (pp. 232-241). Springer London.
<a id="3">[3]</a> https://www.pinecone.io/learn/hybrid-search-intro/