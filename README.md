[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)

# awesome-generative-information-retrieval

Recently, conversational models (Galactica, YOU.com, perplexity.ai) started to be able to access the web or backup their claims with sources (a.k.a. attribution). These chatbots are thus arguably information retrieval machines, competing against or even substituing traditional search engines. We would like to dedicate a space to these models but also to the more general field of generative information retrieval. This includes the neighbouring topic of generative document retrieval, generative recommendation, ...

# Table of Contents

- [Epistemology Papers](#epistemoplogy-papers)
- [Generative Answer Retrieval](#generative-answer-retrieval)
  - [Multimodal](#multimodal)
- [Generative Document Retrieval](#generative-document-retrieval)
  - [Indexing Strategy](#indexing-strategy)
  - [Identifier Design](#identifier-design)
  - [Applications](#applications)
  - [Generative Recommendation](#generative-recommendation)

## Blog Posts

## Live Generative Retrieval

**Character.AI**
[[link](https://book.character.ai/character-book/welcome-to-character-book)]

**DocAsker**  
Jan 2023 [[link](https://www.docasker.com/)]

## Epistemoplogy Papers

**Rethinking Search: Making Domain Experts out of Dilettantes**  
*Metzler et al.*  
SIGIR Forum 2021 [[paper](https://arxiv.org/pdf/2105.02274.pdf)]  

**Conversational Information Seeking. An Introduction to Conversational Search, Recommendation, and Question Answering**  
*Hamed Zamani, Johanne R. Trippas, Jeff Dalton and Filip Radlinski*  
arXiv – Jan 2023 [[paper](https://www.sciencedirect.com/science/article/pii/S0956713521008355)]

## Generative Answer Retrieval

**REPLUG: Retrieval-Augmented Black-Box Language Models**  
*Weijia Shi, Sewon Min, Michihiro Yasunaga, Minjoon Seo, Rich James, Mike Lewis, Luke Zettlemoyer, Wen-tau Yih*  
arXiv – Jan 2023 [[paper](https://arxiv.org/abs/2301.12652)]

**In-Context Retrieval-Augmented Language Models**  
*Ori Ram, Yoav Levine, Itay Dalmedigos, Dor Muhlgay, Amnon Shashua, Kevin Leyton-Brown, Yoav Shoham*  
AI21 Labs – Jan 2023 [[paper](https://uploads-ssl.webflow.com/60fd4503684b466578c0d307/63c6c20dec4479564db21819_NEW_In_Context_Retrieval_Augmented_Language_Models.pdf)] [[code](https://github.com/AI21Labs/in-context-ralm)]

**AtMan: Understanding Transformer Predictions Through Memory Efficient Attention Manipulation**  
*Hamed Zamani, Johanne R. Trippas, Jeff Dalton and Filip Radlinski*  
arXiv – Jan 2023 [[paper](https://arxiv.org/pdf/2301.08110.pdf)]  

**Recitation-Augmented Language Models**  
*Anonymous*  
ICLR 2023 – Sep 2022 [[paper](https://openreview.net/forum?id=-cqvvvb-NkI)]

**Improving language models by retrieving from trillions of tokens**  
*Sebastian Borgeaud, Arthur Mensch, Jordan Hoffmann, Trevor Cai, Eliza Rutherford, Katie Millican, George van den Driessche, Jean-Baptiste Lespiau, Bogdan Damoc, Aidan Clark, Diego de Las Casas, Aurelia Guy, Jacob Menick, Roman Ring, Tom Hennigan, Saffron Huang, Loren Maggiore, Chris Jones, Albin Cassirer, Andy Brock, Michela Paganini, Geoffrey Irving, Oriol Vinyals, Simon Osindero, Karen Simonyan, Jack W. Rae, Erich Elsen, Laurent Sifre*  
arXiv – Dec 2021 [[paper](https://arxiv.org/abs/2112.04426)]

### Multimodal

**Retrieval-Augmented Multimodal Language Modeling**  
*Michihiro Yasunaga, Armen Aghajanyan, Weijia Shi, Rich James, Jure Leskovec, Percy Liang, Mike Lewis, Luke Zettlemoyer, Wen-tau Yih*  
arXiv – Nov 2022 [[paper](https://arxiv.org/pdf/2211.12561.pdf)]

## Generative Document Retrieval

For this section, we reuse the content of [awesome-generative-retrieval-models](https://github.com/Chriskuei/awesome-generative-retrieval-models) and give full credit to [Chriskuei](https://github.com/Chriskuei)!

### Indexing Strategy

**Transformer Memory as a Differentiable Search Index**  
*Tay et al.*  
Arxiv 2022 [[paper](https://arxiv.org/abs/2202.06991)] [[Video](https://www.youtube.com/watch?v=qlB0TPBQ7YY)] 

**CorpusBrain: Pre-train a Generative Retrieval Model for Knowledge-Intensive Language Tasks**  
*Chen et al.*  
CIKM 2022 [[paper](https://arxiv.org/abs/2208.07652)] [[Code](https://github.com/ict-bigdatalab/CorpusBrain)] 

**A Neural Corpus Indexer for Document Retrieval**  
*Wang et al.*  
Arxiv 2022 [[paper](https://arxiv.org/abs/2206.02743)]

**Bridging the Gap Between Indexing and Retrieval for Differentiable Search Index with Query Generation**  
*Zhuang et al.*  
Arxiv 2022 [[paper](https://arxiv.org/abs/2206.10128)] [[Code](https://github.com/ArvinZhuang/DSI-transformers)]

### Identifier Design

**Autoregressive Entity Retrieval**  
*Cao et al*  
ICLR 2021 [[paper](https://arxiv.org/pdf/2010.00904.pdf)] [[Code](https://github.com/facebookresearch/GENRE)]

**Autoregressive Search Engines: Generating Substrings as Document Identifiers**  
*Bevilacqua et al.*  
Arxiv 2022 [[paper](https://arxiv.org/pdf/2204.10628.pdf)] [[Code](https://github.com/facebookresearch/SEAL)]

**DynamicRetriever: A Pre-training Model-based IR System with Neither Sparse nor Dense Index**  
*Zhou et al*  
Arxiv 2022 [[paper](https://arxiv.org/pdf/2203.00537.pdf)]

**Ultron: An Ultimate Retriever on Corpus with a Model-based Indexer**  
*Zhou et al*  
Arxiv 2022 [[paper](https://arxiv.org/pdf/2208.09257.pdf)]

### Applications

**GERE: Generative Evidence Retrieval for Fact Verification**  
*Chen et al*  
SIGIR 2022 [[paper](https://dl.acm.org/doi/pdf/10.1145/3477495.3531827)] [[Code](https://github.com/Chriskuei/GERE)]

**Generative Multi-hop Retrieval**  
*Lee et al*  
Arxiv 2022 [[paper](https://arxiv.org/pdf/2204.13596.pdf)]


## Generative Recommendation

