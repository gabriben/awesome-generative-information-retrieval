[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)

# awesome-generative-information-retrieval

Recently, conversational models (Galactica, YOU.com, perplexity.ai) started to be able to access the web or backup their claims with sources (a.k.a. attribution). These chatbots are thus arguably information retrieval machines, competing against or even substituing traditional search engines. We would like to dedicate a space to these models but also to the more general field of generative information retrieval. We tentatively devide the field in two main topics: **Grounded Answer Generation** and **Generative Document Retrieval**. We also include generative recommendation, generative grounded summarization etc.

Pull-requests welcome!

# Table of Contents

- [Live Generative Retrieval](#live-generative-retrieval)
- [Blog Posts](#blog-posts)
- [Epistemology Papers](#epistemoplogy-papers)
- [Grounded Answer Generation](#grounded-answer-generation)
  - [Multimodal](#multimodal)
- [Generative Document Retrieval](#generative-document-retrieval)
  - [Indexing Strategy](#indexing-strategy)
  - [Identifier Design](#identifier-design)
  - [Applications](#applications)
- [Generative Recommendation](#generative-recommendation)
- [Summarization](#summarization)

## Live Generative Retrieval

Although some of these are not accompanied by a paper, they might be useful to other Generative IR researchers for empirical studies or interface design considerations.

**Sparrow**  
[not released] [[paper](#paper-sparrow)]

**DocAsker**  
Jan 2023 [[live](https://www.docasker.com/)]

**YOU.com**  
Dec 2023 [[live](https://you.com/)]

**BlenderBot**  
Aug 2022 [[live (USA)](https://geo-not-available.blenderbot.ai/)] [[model weights](https://parl.ai/docs/zoo.html)] [[code](https://github.com/facebookresearch/ParlAI/blob/main/projects/bb3/agents/README.md)] [[paper1](#paper-blenderbot)] [[paper2](#paper-blenderbot-hf)]

**PHIND**  
date? [[live](https://phind.com/)]

**Perplexity**  
date? [[live](https://www.perplexity.ai/)]

**Galactica**  
date? [[demo](https://galactica.org/explore/)] [[API](https://github.com/paperswithcode/galai)] [[paper](#paper-galactica)]

**Elicit**  
date? [[live](https://elicit.org/)]

**ZetaAlpha**  
date? [[live](https://search.zeta-alpha.com/)]  
uses OpenAI API

Honorable mentions of **Claude** [private beta] [[paper](#paper-constiutional-ai)] and **ChatGPT** [[live](https://openai.com/blog/chatgpt/)] that are borderline retrieval models (hallucinate a lot and don't cite their sources for now)

## Blog Posts

**What Makes a Dialog Agent Useful?**  
*Nazneen Rajani, Nathan Lambert, Victor Sanh, Thomas Wolf*  
Hugging Face Blog – Jan 2023 [[link](https://huggingface.co/blog/dialog-agents)]

## Epistemology Papers

**Rethinking Search: Making Domain Experts out of Dilettantes**  
*Donald Metzler, Yi Tay, Dara Bahri, Marc Najork*  
SIGIR Forum 2021 – May 2021 [[paper](https://arxiv.org/pdf/2105.02274.pdf)]  

**Conversational Information Seeking. An Introduction to Conversational Search, Recommendation, and Question Answering**  
*Hamed Zamani, Johanne R. Trippas, Jeff Dalton and Filip Radlinski*  
arXiv – Jan 2023 [[paper](https://www.sciencedirect.com/science/article/pii/S0956713521008355)]

## Grounded Answer Generation

Could be subdivided into something like retrieval-enhanced-LLMs and attribution-for-conversations.

**REPLUG: Retrieval-Augmented Black-Box Language Models**  
*Weijia Shi, Sewon Min, Michihiro Yasunaga, Minjoon Seo, Rich James, Mike Lewis, Luke Zettlemoyer, Wen-tau Yih*  
arXiv – Jan 2023 [[paper](https://arxiv.org/abs/2301.12652)]

**In-Context Retrieval-Augmented Language Models**  
*Ori Ram, Yoav Levine, Itay Dalmedigos, Dor Muhlgay, Amnon Shashua, Kevin Leyton-Brown, Yoav Shoham*  
AI21 Labs – Jan 2023 [[paper](https://uploads-ssl.webflow.com/60fd4503684b466578c0d307/63c6c20dec4479564db21819_NEW_In_Context_Retrieval_Augmented_Language_Models.pdf)] [[code](https://github.com/AI21Labs/in-context-ralm)]

**AtMan: Understanding Transformer Predictions Through Memory Efficient Attention Manipulation**  
*Hamed Zamani, Johanne R. Trippas, Jeff Dalton and Filip Radlinski*  
arXiv – Jan 2023 [[paper](https://arxiv.org/pdf/2301.08110.pdf)]  

**Attributed Question Answering: Evaluation and Modeling for Attributed Large Language Models**  
*Bernd Bohnet, Vinh Q. Tran, Pat Verga, Roee Aharoni, Daniel Andor, Livio Baldini Soares, Jacob Eisenstein, Kuzman Ganchev, Jonathan Herzig, Kai Hui, Tom Kwiatkowski, Ji Ma, Jianmo Ni, Tal Schuster, William W. Cohen, Michael Collins, Dipanjan Das, Donald Metzler, Slav Petrov, Kellie Webster*  
arXiv – Dec 2022 [[paper](https://arxiv.org/abs/2212.08037)]

<a name="paper-galactica"></a>
**Galactica: A Large Language Model for Science**  
*Ross Taylor, Marcin Kardas, Guillem Cucurull,
Thomas Scialom, Anthony Hartshorn, Elvis Saravia,
Andrew Poulton, Viktor Kerkez, Robert Stojnic*
Galactica.org – 2022 [[paper](https://galactica.org/static/paper.pdf)]

**Recitation-Augmented Language Models**  
*Anonymous*  
ICLR 2023 – Sep 2022 [[paper](https://openreview.net/forum?id=-cqvvvb-NkI)]

**Generate rather than Retrieve: Large Language Models are Strong Context Generators**  
*Wenhao Yu1, Dan Iter2, Shuohang Wang2, Yichong Xu2, Mingxuan Ju1, Soumya Sanyal3, Chenguang Zhu2, Michael Zeng2, Meng Jiang1*  
ICLR 2023 – Sep 2022 [[paper](https://openreview.net/forum?id=fB0hRu9GZUS)]

<a name="paper-sparrow"></a>
**Improving alignment of dialogue agents via targeted human judgements**  
*Amelia Glaese, Nat McAleese, Maja Trębacz, John Aslanides, Vlad Firoiu, Timo Ewalds, Maribeth Rauh, Laura Weidinger, Martin Chadwick, Phoebe Thacker, Lucy Campbell-Gillingham, Jonathan Uesato, Po-Sen Huang, Ramona Comanescu, Fan Yang, Abigail See, Sumanth Dathathri, Rory Greig, Charlie Chen, Doug Fritz, Jaume Sanchez Elias, Richard Green, Soňa Mokrá, Nicholas Fernando, Boxi Wu, Rachel Foley, Susannah Young, Iason Gabriel, William Isaac, John Mellor, Demis Hassabis, Koray Kavukcuoglu, Lisa Anne Hendricks, Geoffrey Irving*  
arXiv – Sep 2022 [[paper](https://arxiv.org/pdf/2209.14375.pdf)]

<a name="paper-blenderbot"></a>
**BlenderBot 3: a deployed conversational agent that continually learns to responsibly engage**
*Kurt Shuster, Jing Xu, Mojtaba Komeili, Da Ju, Eric Michael Smith, Stephen Roller, Megan Ung, Moya Chen, Kushal Arora, Joshua Lane, Morteza Behrooz, William Ngan, Spencer Poff, Naman Goyal, Arthur Szlam, Y-Lan Boureau, Melanie Kambadur, Jason Weston*
arXiv – Aug 2022 [[paper](https://arxiv.org/abs/2208.03188)]

**WebGPT: Browser-assisted question-answering with human feedback**  
*Reiichiro Nakano, Jacob Hilton, Suchir Balaji, Jeff Wu, Long Ouyang, Christina Kim, Christopher Hesse, Shantanu Jain, Vineet Kosaraju, William Saunders, Xu Jiang, Karl Cobbe, Tyna Eloundou, Gretchen Krueger, Kevin Button, Matthew Knight, Benjamin Chess, John Schulman*  
arXiv – Dec 2021 [[paper](https://arxiv.org/abs/2112.09332)]

**Improving language models by retrieving from trillions of tokens**  
*Sebastian Borgeaud, Arthur Mensch, Jordan Hoffmann, Trevor Cai, Eliza Rutherford, Katie Millican, George van den Driessche, Jean-Baptiste Lespiau, Bogdan Damoc, Aidan Clark, Diego de Las Casas, Aurelia Guy, Jacob Menick, Roman Ring, Tom Hennigan, Saffron Huang, Loren Maggiore, Chris Jones, Albin Cassirer, Andy Brock, Michela Paganini, Geoffrey Irving, Oriol Vinyals, Simon Osindero, Karen Simonyan, Jack W. Rae, Erich Elsen, Laurent Sifre*  
arXiv – Dec 2021 [[paper](https://arxiv.org/abs/2112.04426)]

**Recipes for Building an Open-Domain Chatbot**  
*Stephen Roller, Emily Dinan, Naman Goyal, Da Ju, Mary Williamson, Yinhan Liu, Jing Xu, Myle Ott, Eric Michael Smith, Y-Lan Boureau, Jason Weston*  
EACL 2021 – Apr 2021 [[paper](https://aclanthology.org/2021.eacl-main.24.pdf)]

**BERT-kNN: Adding a kNN Search Component to Pretrained Language Models for Better QA**  
*Nora Kassner, Hinrich Schütze*  
EMNLP 2020 – Nov 2020 [[paper](https://aclanthology.org/2020.findings-emnlp.307.pdf)]

**Generalization through Memorization: Nearest Neighbor Language Models**\
*Urvashi Khandelwal, Omer Levy, Dan Jurafsky, Luke Zettlemoyer, Mike Lewis*  
ICLR 2020 – Sep 2019 [[paper](https://openreview.net/forum?id=HklBjCEKvH)] [[code](https://github.com/urvashik/knnlm)]

**A Hybrid Retrieval-Generation Neural Conversation Model**  
*Liu Yang, Junjie Hu, Minghui Qiu, Chen Qu, Jianfeng Gao, W. Bruce Croft, Xiaodong Liu, Yelong Shen, Jingjing Liu*  
arXiv – Apr 2019 [[paper](https://arxiv.org/abs/1904.09068)]

### Reinforcement Learning

<a name="paper-constiutional-ai"></a>
**Constitutional AI: Harmlessness from AI Feedback**  
*Yuntao Bai, Saurav Kadavath, Sandipan Kundu, Amanda Askell, Jackson Kernion,
Andy Jones, Anna Chen, Anna Goldie, Azalia Mirhoseini, Cameron McKinnon,
Carol Chen, Catherine Olsson, Christopher Olah, Danny Hernandez, Dawn Drain,
Deep Ganguli, Dustin Li, Eli Tran-Johnson, Ethan Perez, Jamie Kerr, Jared Mueller,
Jeffrey Ladish, Joshua Landau, Kamal Ndousse, Kamile Lukosiute, Liane Lovitt,
Michael Sellitto, Nelson Elhage, Nicholas Schiefer, Noemi Mercado, Nova DasSarma,
Robert Lasenby, Robin Larson, Sam Ringer, Scott Johnston, Shauna Kravec,
Sheer El Showk, Stanislav Fort, Tamera Lanham, Timothy Telleen-Lawton, Tom Conerly,
Tom Henighan, Tristan Hume, Samuel R. Bowman, Zac Hatfield-Dodds, Ben Mann,
Dario Amodei, Nicholas Joseph, Sam McCandlish, Tom Brown, Jared Kaplan*
Anthropic.com – Dec 2022 [[paper](https://www.anthropic.com/constitutional.pdf)]

<a name="paper-blenderbot-hf"></a>
**Learning New Skills after Deployment: Improving open-domain internet-driven dialogue with human feedback**  
*Jing Xu, Megan Ung, Mojtaba Komeili, Kushal Arora, Y-Lan Boureau, Jason Weston*  
arXiv – Aug 2022 [[paper](https://arxiv.org/abs/2208.03270)]

### Multimodal

**Retrieval-Augmented Multimodal Language Modeling**  
*Michihiro Yasunaga, Armen Aghajanyan, Weijia Shi, Rich James, Jure Leskovec, Percy Liang, Mike Lewis, Luke Zettlemoyer, Wen-tau Yih*  
arXiv – Nov 2022 [[paper](https://arxiv.org/pdf/2211.12561.pdf)]

## Generative Document Retrieval

For this section, we reuse the content of [awesome-generative-retrieval-models](https://github.com/Chriskuei/awesome-generative-retrieval-models) and give full credit to [Chriskuei](https://github.com/Chriskuei)!

### Indexing Strategy

**DSI++: Updating Transformer Memory with New Documents**  
*Sanket Vaibhav Mehta, Jai Gupta, Yi Tay, Mostafa Dehghani, Vinh Q. Tran, Jinfeng Rao, Marc Najork, Emma Strubell, Donald Metzler*  
arXiv – Dec 2022 [[paper](https://arxiv.org/abs/2212.09744)]

**CodeDSI: Differentiable Code Search**  
*Usama Nadeem, Noah Ziems, Shaoen Wu*  
arXiv – Oct 2022 [[paper](https://arxiv.org/abs/2210.00328)]

**Transformer Memory as a Differentiable Search Index**  
*Yi Tay, Vinh Q. Tran, Mostafa Dehghani, Jianmo Ni, Dara Bahri, Harsh Mehta, Zhen Qin, Kai Hui, Zhe Zhao, Jai Gupta, Tal Schuster, William W. Cohen, Donald Metzler*  
Neurips 2022 – Oct 2022 [[paper](https://openreview.net/forum?id=Vu-B0clPfq)] [[Video](https://www.youtube.com/watch?v=qlB0TPBQ7YY)] 

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
*Nicola De Cao, Gautier Izacard, Sebastian Riedel, Fabio Petroni*  
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
*Jiangui Chen, Ruqing Zhang, Jiafeng Guo, Yixing Fan, Xueqi Cheng*  
SIGIR 2022 [[paper](https://dl.acm.org/doi/pdf/10.1145/3477495.3531827)] [[Code](https://github.com/Chriskuei/GERE)]

**Generative Multi-hop Retrieval**  
*Hyunji Lee, Sohee Yang, Hanseok Oh, Minjoon Seo*  
Arxiv – Apr 2022 [[paper](https://arxiv.org/pdf/2204.13596.pdf)]


## Generative Recommendation

**Generative Slate Recommendation with Reinforcement Learning**  
*Romain Deffayet, Thibaut Thonet, Jean-Michel Renders, and Maarten de Rijke*  
WSDM 2023 – [[paper](https://arxiv.org/abs/2301.08632)]

## Summarization

**Learning to summarize with human feedback**  
*Nisan Stiennon, Long Ouyang, Jeff Wu, Daniel M. Ziegler, Ryan Lowe, Chelsea Voss, Alec Radford, Dario Amodei, Paul Christiano*  
NeurIPS 2020 – Sep 2020 [[paper](https://proceedings.neurips.cc/paper/2020/file/1f89885d556929e98d3ef9b86448f951-Paper.pdf)]
