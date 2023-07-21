# awesome-generative-information-retrieval [![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)

Recently, conversational models (Galactica, YOU.com, perplexity.ai) started to be able to access the web or backup their claims with sources (a.k.a. attribution). These chatbots are thus arguably information retrieval machines, competing against or even substituing traditional search engines. We would like to dedicate a space to these models but also to the more general field of generative information retrieval. We tentatively devide the field in two main topics: **Grounded Answer Generation** and **Generative Document Retrieval**. We also include generative recommendation, generative grounded summarization etc.

Pull-requests welcome!

# Table of Contents

- [Live Generative Retrieval](#live-generative-retrieval)
- [Blog Posts](#blog-posts)
- [Datasets](#datasets)
- [Tools](#tools)
- [Evaluation](#evaluation)
- [Workshops](#workshops)
- [Epistemology Papers](#epistemoplogy-papers)
- [Grounded Answer Generation](#grounded-answer-generation)
  - [Retrieval-Enhanced LLM](#retrieval-enhanced-llm)  
  - [LLM Memory Manipulation](#llm-memory-manipulation)
  - [Reinforcement Learning](#reinforcement-learning)
  - [Multimodal](#multimodal)
  - [Prompting](#prompting)
  - [Generate Code](#generate-code)
  - [Latent LLM Knowledge](#latent-llm-knowledge)
- [Generative Document Retrieval](#generative-document-retrieval)
  - [Generate a Document ID as an identifier](#generate-a-document-id-as-an-identifier)
  - [Generate a string as an identifier](#generate-a-string-as-an-identifier)
  - [Applications](#applications)
- [Summarization](#summarization)
- [Generative Recommendation](#generative-recommendation)
- [Knowledge Graph Generation](#knowledge-graph-generation)

## Live Generative Retrieval

Although some of these are not accompanied by a paper, they might be useful to other Generative IR researchers for empirical studies or interface design considerations.

⚡️
**factiverse** Jun 2023 [[live](https://editor.factiverse.ai/)] ⚡️
**devmarizer** Mar 2023 [[live](https://devmarizer.firebaseapp.com/)] ⚡️
**TaxGenius** Mar 2023 [[live](https://www.taxgenius.app/)] ⚡️
**doc-gpt** Mar 2023 [[live](https://pineappleexpress808-doc-gpt-doc-gpt-q0823l.streamlit.app/)] ⚡️
**book-gpt** Feb 2023 [[live](https://github.com/fraserxu/book-gpt)] ⚡️
**Neeva** Feb 2023 [[live](https://neeva.com/)] ⚡️
**Golden Retriever** Feb 2023 [[live](https://golden.com/ai)] ⚡️
**Bing – Prometheus** Feb 2023 [[waitlist](https://www.bing.com/)] ⚡️
**Google – Bard** Feb 2023 [only in certain countries] ⚡️
**Paper QA** Feb 2023 [[code](https://github.com/whitead/paper-qa)] [[demo](https://huggingface.co/spaces/whitead/paper-qa)] ⚡️
**DocsGPT** Feb 2023 [[live](https://docsgpt.arc53.com/)] [[code](https://github.com/arc53/docsgpt)] ⚡️
**DocAsker** Jan 2023 [[live](https://www.docasker.com/)] ⚡️
**Lexii.ai** Jan 2023 [[live](https://lexii.ai/)] ⚡️
**YOU.com** Dec 2022 [[live](https://you.com/)] ⚡️
**arXivGPT** Dec 2022 [[Chrome extension](https://github.com/hunkimForks/chatgpt-arxiv-extension)] ⚡️
**GPT Index** Nov 2022 [[API](https://github.com/jerryjliu/gpt_index)] ⚡️
**BlenderBot** Aug 2022 [[live (USA)](https://geo-not-available.blenderbot.ai/)] [[model weights](https://parl.ai/docs/zoo.html)] [[code](https://github.com/facebookresearch/ParlAI/blob/main/projects/bb3/agents/README.md)] [[paper1](#paper-blenderbot)] [[paper2](#paper-blenderbot-hf)] ⚡️
**PHIND** date? [[live](https://phind.com/)] ⚡️
**Perplexity** date? [[live](https://www.perplexity.ai/)] ⚡️
**Galactica** date? [[demo](https://galactica.org/explore/)] [[API](https://github.com/paperswithcode/galai)] [[paper](#paper-galactica)] ⚡️
**Elicit** date? [[live](https://elicit.org/)] ⚡️
**ZetaAlpha** date? [[live](https://search.zeta-alpha.com/)] uses OpenAI API 

Under development: 
⚡️
**Open-Assistant** [open source] [[code](https://github.com/LAION-AI/Open-Assistant)] ⚡️
**Transformer Reinforcement Learning** [open source] [[code](https://github.com/lvwerra/trl)] ⚡️
**Sparrow** [[paper](#paper-sparrow)]

Honorable mentions of **Claude** [private beta] [[paper](#paper-constiutional-ai)] and **ChatGPT** [[live](https://openai.com/blog/chatgpt/)] that are borderline retrieval models (hallucinate a lot and don't cite their sources for now)

See [PowerdByGPT](https://www.poweredbygpt.co/) for more.

## Blog Posts

**What Makes a Dialog Agent Useful?**  
*Nazneen Rajani, Nathan Lambert, Victor Sanh, Thomas Wolf*  
Hugging Face Blog – Jan 2023 [[link](https://huggingface.co/blog/dialog-agents)]

**Forecasting potential misuses of language models for disinformation campaigns and how to reduce risk**  
*Josh A. Goldstein, Girish Sastry, Micah Musser, Renée DiResta, Matthew Gentzel, Katerina Sedova*  
OpenAI Blog – Jan 2023 [[link](https://openai.com/research/forecasting-misuse)]

## Datasets

**ChatGPT-RetrievalQA**  
*Arian Askari, Mohammad Aliannejadi, Evangelos Kanoulas, Suzan Verberne*  
Github – Feb 2023 [[code](https://github.com/arian-askari/ChatGPT-RetrievalQA)]

**KAMEL : Knowledge Analysis with Multitoken Entities in Language Models**  
*Jan-Christoph Kalo, Leandra Fichtel*  
AKBC 22 – [[paper](https://www.akbc.ws/2022/assets/pdfs/15_kamel_knowledge_analysis_with_.pdf)]

**TruthfulQA: Measuring How Models Mimic Human Falsehoods**  
*Stephanie Lin, Jacob Hilton, Owain Evans*  
arXiv – Sep 2021 [[paper](https://arxiv.org/pdf/2109.07958.pdf)] [[code](https://github.com/sylinrl/TruthfulQA)]

**Complex Answer Retrieval**  
*Laura Dietz, Manisha Verma, Filip Radlinski, Nick Craswell, Ben Gamari, Jeff Dalton, John  Foley*  
TREC – 2017-2019 [[link](http://trec-car.cs.unh.edu/)]

## Tools

**PrimeQA: The Prime Repository for State-of-the-Art Multilingual Question Answering Research and Development**  
*Avirup Sil, Jaydeep Sen, Bhavani Iyer, Martin Franz, Kshitij Fadnis, Mihaela Bornea, Sara Rosenthal, Scott McCarley, Rong Zhang, Vishwajeet Kumar, Yulong Li, Md Arafat Sultan, Riyaz Bhat, Radu Florian, Salim Roukos*  
arXiv – Jan 2023 [[paper](https://arxiv.org/abs/2301.09715)] [[code](https://github.com/primeqa/primeqa)]

## Evaluation

**FACTSCORE: Fine-grained Atomic Evaluation of Factual Precision in Long Form Text Generation**  
*Sewon Min, Kalpesh Krishna, Xinxi Lyu, Mike Lewis, Wen-tau Yih, Pang Wei Koh, Mohit Iyyer, Luke Zettlemoyer, Hannaneh Hajishirzi1*  
Pypi – May 2023 [[paper](https://martiansideofthemoon.github.io/assets/factscore.pdf)] [[code](https://pypi.org/project/factscore/#description)]

**FACTKB: Generalizable Factuality Evaluation using Language Models Enhanced with Factual Knowledge**  
*Shangbin Feng, Vidhisha Balachandran, Yuyang Bai, Yulia Tsvetkov*  
arXiv – May 2023 [[paper](https://arxiv.org/abs/2305.08281)] [[code](https://github.com/BunsenFeng/FactKB)]

**Evaluating Verifiability in Generative Search Engines**  
*Nelson F. Liu, Tianyi Zhang, Percy Liang*  
arXiv – April 2023 [[paper](https://arxiv.org/abs/2304.09848)] [[code](https://github.com/nelson-liu/evaluating-verifiability-in-generative-search-engines)]

## Workshops

**First Workshop on Generative Information Retrieval**  
*Gabriel Bénédict, Ruqing Zhang, Donald Metzler*  
SIGIR 23 – Jul 2023 [[link](https://coda.io/@sigir/gen-ir)]

## Epistemology Papers

**The False Promise of Imitating Proprietary LLMs**  
*Arnav Gudibande, Eric Wallace, Charlie Snell, Xinyang Geng, Hao Liu, Pieter Abbeel, Sergey Levine, Dawn Song*  
arXiv – May 2023 [[paper](https://arxiv.org/abs/2305.15717)]

**Generative Recommendation: Towards Next-generation Recommender Paradigm**  
*Fengji Zhang, Bei Chen, Yue Zhang, Jin Liu, Daoguang Zan, Yi Mao, Jian-Guang Lou, Weizhu Chen*  
arXiv – April 2023 [[paper](https://arxiv.org/pdf/2304.03516.pdf)]

**Augmented Language Models: a Survey**  
*Grégoire Mialon, Roberto Dessì, Maria Lomeli, Christoforos Nalmpantis, Ram Pasunuru, Roberta Raileanu, Baptiste Rozière, Timo Schick, Jane Dwivedi-Yu, Asli Celikyilmaz, Edouard Grave, Yann LeCun, Thomas Scialom*  
arXiv – Feb 2023 [[paper](https://arxiv.org/pdf/2302.07842.pdf)]

**Generative Language Models and Automated Influence Operations: Emerging Threats and Potential Mitigations**  
*Josh A. Goldstein, Girish Sastry, Micah Musser, Renee DiResta, Matthew Gentzel, Katerina Sedova*  
arXiv – Jan 2023 [[paper](https://arxiv.org/pdf/2301.04246.pdf)]

**Conversational Information Seeking. An Introduction to Conversational Search, Recommendation, and Question Answering**  
*Hamed Zamani, Johanne R. Trippas, Jeff Dalton and Filip Radlinski*  
arXiv – Jan 2023 [[paper](https://www.sciencedirect.com/science/article/pii/S0956713521008355)]

**Facts**  
*Kevin Mulligan and Fabrice Correia*  
The Stanford Encyclopedia of Philosophy – Winter 2021 [[url](https://plato.stanford.edu/archives/win2021/entries/facts/)]

**Truthful AI: Developing and governing AI that does not lie**  
*Owain Evans, Owen Cotton-Barratt, Lukas Finnveden, Adam Bales, Avital Balwit, Peter Wills, Luca Righetti, William Saunders*  
arXiv – Oct 2021 [[paper](https://arxiv.org/pdf/2110.06674.pdf)]

**Rethinking Search: Making Domain Experts out of Dilettantes**  
*Donald Metzler, Yi Tay, Dara Bahri, Marc Najork*  
SIGIR Forum 2021 – May 2021 [[paper](https://arxiv.org/pdf/2105.02274.pdf)]  

## Grounded Answer Generation


**Attributed Question Answering: Evaluation and Modeling for Attributed Large Language Models**  
*Bernd Bohnet, Vinh Q. Tran, Pat Verga, Roee Aharoni, Daniel Andor, Livio Baldini Soares, Jacob Eisenstein, Kuzman Ganchev, Jonathan Herzig, Kai Hui, Tom Kwiatkowski, Ji Ma, Jianmo Ni, Tal Schuster, William W. Cohen, Michael Collins, Dipanjan Das, Donald Metzler, Slav Petrov, Kellie Webster*  
arXiv – Dec 2022 [[paper](https://arxiv.org/abs/2212.08037)]


### Retrieval-Enhanced LLM 
(external grounding/retrieval at inference time)

**WebGLM: Towards An Efficient Web-Enhanced Question Answering System with Human Preferences**  
*Xiao Liu, Hanyu Lai, Hao Yu, Yifan Xu, Aohan Zeng, Zhengxiao Du, Peng Zhang, Yuxiao Dong, Jie Tang*  
arXiv – Jun 2023 [[paper](https://arxiv.org/abs/2306.07906)]


**RET-LLM: Towards a General Read-Write Memory for Large Language Models**  
*Ali Modarressi, Ayyoob Imani, MOhsen Fayyaz, Hinrich Schutze*  
arXiv – May 2023 [[paper](https://arxiv.org/abs/2305.14322)]

**Gorilla: Large Language Model Connected with Massive APIs**  
*Shishir G. Patil, Tianjun Zhang, Xin Wang, Joseph E. Gonzalez*  
arXiv – May 2023 [[paper](https://arxiv.org/abs/2305.15334)] [[code](https://github.com/ShishirPatil/gorilla)]

**Active Retrieval Augmented Generation**  
*Zhengbao Jiang, Frank F. Xu, Luyu Gao, Zhiqing Sun, Qian Liu, Jane Dwivedi-Yu, Yiming Yang, Jamie Callan, Graham Neubig*  
arXiv – May 2023 [[paper](https://arxiv.org/abs/2305.06983)] [[code](https://github.com/jzbjyb/FLARE)]

**Shall We Pretrain Autoregressive Language Models with Retrieval? A Comprehensive Study**  
*Boxin Wang, Wei Ping, Peng Xu, Lawrence McAfee, Zihan Liu, Mohammad Shoeybi, Yi Dong, Oleksii Kuchaiev, Bo Li, Chaowei Xiao, Anima Anandkumar, Bryan Catanzaro*  
arXiv – Apr 2023 [[paper](https://arxiv.org/abs/2304.06762)] [[code](https://github.com/NVIDIA/Megatron-LM#retro)]

**Check Your Facts and Try Again: Improving Large Language Models with External Knowledge and Automated Feedback**  
*Baolin Peng, Michel Galley, Pengcheng He, Hao Cheng, Yujia Xie, Yu Hu, Qiuyuan Huang, Lars Liden, Zhou Yu, Weizhu Chen, Jianfeng Gao*  
arXiv – Feb 2023 [[paper](https://arxiv.org/abs/2302.12813)] [[code](https://github.com/pengbaolin/LLM-Augmenter)]

**Toolformer: Language Models Can Teach Themselves to Use Tools**  
*Timo Schick, Jane Dwivedi-Yu, Roberto Dessì, Roberta Raileanu, Maria Lomeli, Luke Zettlemoyer, Nicola Cancedda, Thomas Scialom*  
arXiv – Feb 2023 [[paper](https://arxiv.org/abs/2302.04761)]

**REPLUG: Retrieval-Augmented Black-Box Language Models**  
*Weijia Shi, Sewon Min, Michihiro Yasunaga, Minjoon Seo, Rich James, Mike Lewis, Luke Zettlemoyer, Wen-tau Yih*  
arXiv – Jan 2023 [[paper](https://arxiv.org/abs/2301.12652)]

**In-Context Retrieval-Augmented Language Models**  
*Ori Ram, Yoav Levine, Itay Dalmedigos, Dor Muhlgay, Amnon Shashua, Kevin Leyton-Brown, Yoav Shoham*  
AI21 Labs – Jan 2023 [[paper](https://uploads-ssl.webflow.com/60fd4503684b466578c0d307/63c6c20dec4479564db21819_NEW_In_Context_Retrieval_Augmented_Language_Models.pdf)] [[code](https://github.com/AI21Labs/in-context-ralm)]

**Recipes for Building an Open-Domain Chatbot**  
*Stephen Roller, Emily Dinan, Naman Goyal, Da Ju, Mary Williamson, Yinhan Liu, Jing Xu, Myle Ott, Eric Michael Smith, Y-Lan Boureau, Jason Weston*  
EACL 2021 – Apr 2021 [[paper](https://aclanthology.org/2021.eacl-main.24.pdf)]

**AtMan: Understanding Transformer Predictions Through Memory Efficient Attention Manipulation**  
*Hamed Zamani, Johanne R. Trippas, Jeff Dalton and Filip Radlinski*  
arXiv – Jan 2023 [[paper](https://arxiv.org/pdf/2301.08110.pdf)]  

**Demonstrate-Search-Predict: Composing retrieval and language models for knowledge-intensive NLP**
*Omar Khattab, Keshav Santhanam, Xiang Lisa Li, David Hall, Percy Liang, Christopher Potts, Matei Zaharia*  
arXiv – Dec 2022 [[paper](https://arxiv.org/pdf/2212.14024.pdf)]

**Improving language models by retrieving from trillions of tokens**  
*Sebastian Borgeaud, Arthur Mensch, Jordan Hoffmann, Trevor Cai, Eliza Rutherford, Katie Millican, George van den Driessche, Jean-Baptiste Lespiau, Bogdan Damoc, Aidan Clark, Diego de Las Casas, Aurelia Guy, Jacob Menick, Roman Ring, Tom Hennigan, Saffron Huang, Loren Maggiore, Chris Jones, Albin Cassirer, Andy Brock, Michela Paganini, Geoffrey Irving, Oriol Vinyals, Simon Osindero, Karen Simonyan, Jack W. Rae, Erich Elsen, Laurent Sifre*  
arXiv – Dec 2021 [[paper](https://arxiv.org/abs/2112.04426)]

**WebGPT: Browser-assisted question-answering with human feedback**  
*Reiichiro Nakano, Jacob Hilton, Suchir Balaji, Jeff Wu, Long Ouyang, Christina Kim, Christopher Hesse, Shantanu Jain, Vineet Kosaraju, William Saunders, Xu Jiang, Karl Cobbe, Tyna Eloundou, Gretchen Krueger, Kevin Button, Matthew Knight, Benjamin Chess, John Schulman*  
arXiv – Dec 2021 [[paper](https://arxiv.org/abs/2112.09332)]

**BERT-kNN: Adding a kNN Search Component to Pretrained Language Models for Better QA**  
*Nora Kassner, Hinrich Schütze*  
EMNLP 2020 – Nov 2020 [[paper](https://aclanthology.org/2020.findings-emnlp.307.pdf)]

**REALM: Retrieval-Augmented Language Model Pre-Training**  
*Kelvin Guu, Kenton Lee, Zora Tung, Panupong Pasupat, Ming-Wei Chang*  
ICML 2020 – Jul 2020 [[paper](https://arxiv.org/abs/2002.08909)]

**A Hybrid Retrieval-Generation Neural Conversation Model**  
*Liu Yang, Junjie Hu, Minghui Qiu, Chen Qu, Jianfeng Gao, W. Bruce Croft, Xiaodong Liu, Yelong Shen, Jingjing Liu*  
arXiv – Apr 2019 [[paper](https://arxiv.org/abs/1904.09068)]

### LLM Memory Manipulation 
(internal grounding at inference time)

**Inspecting and Editing Knowledge Representations in Language Models**  
*Evan Hernandez, Belinda Z. Li, Jacob Andreas*  
arXiv – April 2023 [[paper](https://arxiv.org/abs/2304.00740)] [[code](https://github.com/evandez/REMEDI)]

**Discovering Latent Knowledge in Language Models Without Supervision**  
*Collin Burns, Haotian Ye, Dan Klein, Jacob Steinhardt*  
ICLR 23 – Feb 2023 [[paper](https://openreview.net/pdf?id=ETKGuby0hcs)] [[code](https://github.com/collin-burns/discovering_latent_knowledge)]

<a name="paper-galactica"></a>
**Galactica: A Large Language Model for Science**  
*Ross Taylor, Marcin Kardas, Guillem Cucurull,
Thomas Scialom, Anthony Hartshorn, Elvis Saravia,
Andrew Poulton, Viktor Kerkez, Robert Stojnic*  
Galactica.org – 2022 [[paper](https://galactica.org/static/paper.pdf)]

<a name="paper-blenderbot"></a>
**BlenderBot 3: a deployed conversational agent that continually learns to responsibly engage**  
*Kurt Shuster, Jing Xu, Mojtaba Komeili, Da Ju, Eric Michael Smith, Stephen Roller, Megan Ung, Moya Chen, Kushal Arora, Joshua Lane, Morteza Behrooz, William Ngan, Spencer Poff, Naman Goyal, Arthur Szlam, Y-Lan Boureau, Melanie Kambadur, Jason Weston*  
arXiv – Aug 2022 [[paper](https://arxiv.org/abs/2208.03188)]

**Generate rather than Retrieve: Large Language Models are Strong Context Generators**  
*Wenhao Yu, Dan Iter, Shuohang Wang, Yichong Xu, Mingxuan Ju, Soumya Sanyal, Chenguang Zhu, Michael Zeng, Meng Jiang*  
ICLR 2023 – Sep 2022 [[paper](https://openreview.net/forum?id=fB0hRu9GZUS)]

**Recitation-Augmented Language Models**  
*Zhiqing Sun, Xuezhi Wang, Yi Tay, Yiming Yang, Denny Zhou*  
ICLR 2023 – Sep 2022 [[paper](https://openreview.net/forum?id=-cqvvvb-NkI)]

<a name="paper-sparrow"></a>
**Improving alignment of dialogue agents via targeted human judgements**  
*Amelia Glaese, Nat McAleese, Maja Trębacz, John Aslanides, Vlad Firoiu, Timo Ewalds, Maribeth Rauh, Laura Weidinger, Martin Chadwick, Phoebe Thacker, Lucy Campbell-Gillingham, Jonathan Uesato, Po-Sen Huang, Ramona Comanescu, Fan Yang, Abigail See, Sumanth Dathathri, Rory Greig, Charlie Chen, Doug Fritz, Jaume Sanchez Elias, Richard Green, Soňa Mokrá, Nicholas Fernando, Boxi Wu, Rachel Foley, Susannah Young, Iason Gabriel, William Isaac, John Mellor, Demis Hassabis, Koray Kavukcuoglu, Lisa Anne Hendricks, Geoffrey Irving*  
arXiv – Sep 2022 [[paper](https://arxiv.org/pdf/2209.14375.pdf)]

**LaMDA: Language Models for Dialog Applications**  
*Romal Thoppilan, Daniel De Freitas, Jamie Hall, Noam Shazeer, Apoorv Kulshreshtha, Heng-Tze Cheng, Alicia Jin, Taylor Bos, Leslie Baker, Yu Du, YaGuang Li, Hongrae Lee, Huaixiu Steven Zheng, Amin Ghafouri, Marcelo Menegali, Yanping Huang, Maxim Krikun, Dmitry Lepikhin, James Qin, Dehao Chen, Yuanzhong Xu, Zhifeng Chen, Adam Roberts, Maarten Bosma, Vincent Zhao, Yanqi Zhou, Chung-Ching Chang, Igor Krivokon, Will Rusch, Marc Pickett, Pranesh Srinivasan, Laichee Man, Kathleen Meier-Hellstern, Meredith Ringel Morris, Tulsee Doshi, Renelito Delos Santos, Toju Duke, Johnny Soraker, Ben Zevenbergen, Vinodkumar Prabhakaran, Mark Diaz, Ben Hutchinson, Kristen Olson, Alejandra Molina, Erin Hoffman-John, Josh Lee, Lora Aroyo, Ravi Rajakumar, Alena Butryna, Matthew Lamm, Viktoriya Kuzmina, Joe Fenton, Aaron Cohen, Rachel Bernstein, Ray Kurzweil, Blaise Aguera-Arcas, Claire Cui, Marian Croak, Ed Chi, Quoc Le*  
arXiv – Jan 2022 [[paper](https://arxiv.org/abs/2201.08239)]

**Language Models As or For Knowledge Bases**  
*Simon Razniewski, Andrew Yates, Nora Kassner, Gerhard Weikum*  
DL4KG 2021 – Oct 2021 [[paper](https://arxiv.org/pdf/2110.04888.pdf)]

**Generalization through Memorization: Nearest Neighbor Language Models**\
*Urvashi Khandelwal, Omer Levy, Dan Jurafsky, Luke Zettlemoyer, Mike Lewis*  
ICLR 2020 – Sep 2019 [[paper](https://openreview.net/forum?id=HklBjCEKvH)] [[code](https://github.com/urvashik/knnlm)]

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

**RAMM: Retrieval-augmented Biomedical Visual Question Answering with Multi-modal Pre-training**  
*Zheng Yuan, Qiao Jin, Chuanqi Tan, Zhengyun Zhao, Hongyi Yuan, Fei Huang, Songfang Huang*  
arXiv – Mar 2023 [[paper](https://arxiv.org/abs/2303.00534)]

### Prompting

**ReAct: Synergizing Reasoning and Acting in Language Models**  
*Shunyu Yao, Jeffrey Zhao, Dian Yu, Nan Du, Izhak Shafran, Karthik Narasimhan, Yuan Cao*  
arXiv – Oct 2022 [[paper](https://arxiv.org/abs/2210.03629)]

### Generate Code

**RepoCoder: Repository-Level Code Completion Through Iterative Retrieval and Generation**  
*Fengji Zhang, Bei Chen, Yue Zhang, Jin Liu, Daoguang Zan, Yi Mao, Jian-Guang Lou, Weizhu Chen*  
arXiv – Mar 2023 [[paper](https://arxiv.org/pdf/2303.12570.pdf)]

**DocPrompting: Generating Code by Retrieving the Docs**  
*Shuyan Zhou, Uri Alon, Frank F. Xu, Zhiruo Wang, Zhengbao Jiang, Graham Neubig*  
ICLR 23 – Jul 2022 [[paper](https://arxiv.org/abs/2207.05987)] [[code](https://github.com/shuyanzhou/docprompting)] [[data](https://github.com/shuyanzhou/docprompting#data)]

## Generative Document Retrieval

We jump-started this section by reusing the content of [awesome-generative-retrieval-models](https://github.com/Chriskuei/awesome-generative-retrieval-models) and give full credit to [Chriskuei](https://github.com/Chriskuei) for that! We now have added some content on top.

### Generate a Document ID as an identifier

**Learning to Rank in Generative Retrieval**  
*Yongqi Li, Nan Yang, Liang Wang, Furu Wei, Wenjie Li*  
arXiv – Jun 2023 [[paper](https://arxiv.org/abs/2306.15222)]

**Large Language Models are Built-in Autoregressive Search Engines**  
*Noah Ziems, Wenhao Yu, Zhihan Zhang, Meng Jiang*  
ACL Findings 2023 – May 2023 [[paper](https://arxiv.org/abs/2305.09612)]

**Multiview Identifiers Enhanced Generative Retrieval**  
*Yongqi Li, Nan Yang, Liang Wang, Furu Wei, Wenjie Li*  
ACL 2023 – May 2023 [[paper](https://arxiv.org/abs/2305.16675)]

**How Does Generative Retrieval Scale to Millions of Passages?**  
*Ronak Pradeep, Kai Hui, Jai Gupta, Adam D. Lelkes, Honglei Zhuang, Jimmy Lin, Donald Metzler, Vinh Q. Tran*  
arXiv – May 2023 [[paper](https://arxiv.org/abs/2305.11841)]

**TOME: A Two-stage Approach for Model-based Retrieval**<br> 
*Ruiyang Ren, Wayne Xin Zhao, Jing Liu, Hua Wu, Ji-Rong Wen, Haifeng Wang* <br>
ACL 2023 - May 2023 [[paper](https://arxiv.org/abs/2305.11161)] 

**Understanding Differential Search Index for Text Retrieval**<br> 
*Xiaoyang Chen, Yanjiang Liu, Ben He, Le Sun, Yingfei Sun* <br>
ACL Findings 2023 - May 2023 [[paper](https://arxiv.org/abs/2305.02073)] 

**Learning to Tokenize for Generative Retrieval**  
*Weiwei Sun, Lingyong Yan, Zheng Chen, Shuaiqiang Wang, Haichao Zhu, Pengjie Ren, Zhumin Chen, Dawei Yin, Maarten de Rijke, Zhaochun Ren*  
arXiv – Apr 2023 [[paper](https://arxiv.org/abs/2304.04171)]

**DynamicRetriever: A Pre-trained Model-based IR System Without an Explicit Index**  
*Yu-Jia Zhou, Jing Yao, Zhi-Cheng Dou, Ledell Wu, Ji-Rong Wen*  
Machine Intelligence Research – Jan 2023 [[paper](https://link.springer.com/article/10.1007/s11633-022-1373-9)]

**DSI++: Updating Transformer Memory with New Documents**  
*Sanket Vaibhav Mehta, Jai Gupta, Yi Tay, Mostafa Dehghani, Vinh Q. Tran, Jinfeng Rao, Marc Najork, Emma Strubell, Donald Metzler*  
arXiv – Dec 2022 [[paper](https://arxiv.org/abs/2212.09744)]

**CodeDSI: Differentiable Code Search**  
*Usama Nadeem, Noah Ziems, Shaoen Wu*  
arXiv – Oct 2022 [[paper](https://arxiv.org/abs/2210.00328)]

**Contextualized Generative Retrieval**  
*Hyunji Lee, Jaeyoung Kim, Hoyeon Chang, Hanseok Oh, Sohee Yang, Vlad Karpukhin, Yi Lu, Minjoon Seo*  
arXiv – Oct 2022 [[paper](https://arxiv.org/pdf/2210.02068.pdf)]

**Transformer Memory as a Differentiable Search Index**  
*Yi Tay, Vinh Q. Tran, Mostafa Dehghani, Jianmo Ni, Dara Bahri, Harsh Mehta, Zhen Qin, Kai Hui, Zhe Zhao, Jai Gupta, Tal Schuster, William W. Cohen, Donald Metzler*  
Neurips 2022 – Oct 2022 [[paper](https://openreview.net/forum?id=Vu-B0clPfq)] [[Video](https://www.youtube.com/watch?v=qlB0TPBQ7YY)] [[third-party code](https://github.com/ArvinZhuang/DSI-transformers)]

**A Neural Corpus Indexer for Document Retrieval**  
*Wang et al.*  
Arxiv 2022 [[paper](https://arxiv.org/abs/2206.02743)]

**Bridging the Gap Between Indexing and Retrieval for Differentiable Search Index with Query Generation**  
*Shengyao Zhuang, Houxing Ren, Linjun Shou, Jian Pei, Ming Gong, Guido Zuccon, and Daxin Jiang*  
Arxiv 2022 [[paper](https://arxiv.org/abs/2206.10128)] [[Code](https://github.com/ArvinZhuang/DSI-transformers)]

**DynamicRetriever: A Pre-training Model-based IR System with Neither Sparse nor Dense Index**  
*Zhou et al*  
Arxiv 2022 [[paper](https://arxiv.org/pdf/2203.00537.pdf)]

**Ultron: An Ultimate Retriever on Corpus with a Model-based Indexer**  
*Zhou et al*  
Arxiv 2022 [[paper](https://arxiv.org/pdf/2208.09257.pdf)]

### Generate a string as an identifier

**Semantic-Enhanced Differentiable Search Index Inspired by Learning Strategies**  
*Yubao Tang, Ruqing Zhang, Jiafeng Guo, Jiangui Chen, Zuowei Zhu, Shuaiqiang Wang, Dawei Yin, Xueqi Cheng*  
KDD 2023 – May 2023 [[paper](https://arxiv.org/abs/2305.15115)] 

**Term-Sets Can Be Strong Document Identifiers For Auto-Regressive Search Engines**  
*Peitian Zhang, Zheng Liu, Yujia Zhou, Zhicheng Dou, Zhao Cao*  
arXiv – May 2023 [[paper](https://arxiv.org/abs/2305.13859)] [[Code](https://github.com/namespace-Pt/Adon/tree/AutoTSG)] 

**A Unified Generative Retriever for Knowledge-Intensive Language Tasks via Prompt Learning**  
*Jiangui Chen, Ruqing Zhang, Jiafeng Guo, Maarten de Rijke, Yiqun Liu, Yixing Fan, Xueqi Cheng*  
SIGIR 2023 – Apr 2023 [[paper](https://arxiv.org/abs/2304.14856)] [[Code](https://github.com/ict-bigdatalab/UGR)] 

**CorpusBrain: Pre-train a Generative Retrieval Model for Knowledge-Intensive Language Tasks**  
*Jiangui Chen, Ruqing Zhang, Jiafeng Guo, Yiqun Liu, Yixing Fan, Xueqi Cheng*  
CIKM 2022 – Aug 2022 [[paper](https://arxiv.org/abs/2208.07652)] [[Code](https://github.com/ict-bigdatalab/CorpusBrain)] 

**Autoregressive Search Engines: Generating Substrings as Document Identifiers**  
*Michele Bevilacqua, Giuseppe Ottaviano, Patrick Lewis, Wen-tau Yih, Sebastian Riedel, Fabio Petroni*  
arXiv – Apr 2022 [[paper](https://arxiv.org/pdf/2204.10628.pdf)] [[Code](https://github.com/facebookresearch/SEAL)]

**Autoregressive Entity Retrieval**  
*Nicola De Cao, Gautier Izacard, Sebastian Riedel, Fabio Petroni*  
ICLR 2021 – Oct 2020 [[paper](https://arxiv.org/pdf/2010.00904.pdf)] [[Code](https://github.com/facebookresearch/GENRE)]

### Applications

**Data-Efficient Autoregressive Document Retrieval for Fact Verification**  
*James Thorne*  
SustaiNLP@EMNLP 2022 – Nov 2022 [[paper](https://arxiv.org/abs/2211.09388)]

**GERE: Generative Evidence Retrieval for Fact Verification**  
*Jiangui Chen, Ruqing Zhang, Jiafeng Guo, Yixing Fan, Xueqi Cheng*  
SIGIR 2022 [[paper](https://dl.acm.org/doi/pdf/10.1145/3477495.3531827)] [[Code](https://github.com/Chriskuei/GERE)]

**Generative Multi-hop Retrieval**  
*Hyunji Lee, Sohee Yang, Hanseok Oh, Minjoon Seo*  
Arxiv – Apr 2022 [[paper](https://arxiv.org/pdf/2204.13596.pdf)]

## Summarization

**Learning to summarize with human feedback**  
*Nisan Stiennon, Long Ouyang, Jeff Wu, Daniel M. Ziegler, Ryan Lowe, Chelsea Voss, Alec Radford, Dario Amodei, Paul Christiano*  
NeurIPS 2020 – Sep 2020 [[paper](https://proceedings.neurips.cc/paper/2020/file/1f89885d556929e98d3ef9b86448f951-Paper.pdf)]

**On Faithfulness and Factuality in Abstractive Summarization**  
*Joshua Maynez, Shashi Narayan, Bernd Bohnet, Ryan McDonald*  
ACL 2020 – May 2020 [[paper](https://aclanthology.org/2020.acl-main.173.pdf)]


## Generative Recommendation

**RecFusion: A Binomial Diffusion Process for 1D Data for Recommendation**  
*Gabriel Bénédict, Olivier Jeunen, Samuele Papa, Samarth Bhargav, Daan Odijk, Maarten de Rijke*  
arXiv – Jun 2023 [[paper](https://arxiv.org/abs/2306.08947)]

**A First Look at LLM-Powered Generative News Recommendation**  
*Qijiong Liu, Nuo Chen, Tetsuya Sakai, Xiao-Ming Wu*  
arXiv – Jun 2023 [[paper](https://arxiv.org/pdf/2305.06566.pdf)]

**DiffuRec: A Diffusion Model for Sequential Recommendation**  
*Zihao Li, Aixin Sun, Chenliang Li*  
arXiv – Apr 2023 [[paper](https://arxiv.org/abs/2304.00686)]

**Diffusion Recommender Model**  
*Wenjie Wang, Yiyan Xu, Fuli Feng, Xinyu Lin, Xiangnan He, Tat-Seng Chua*  
SIGIR 2023 – Apr 2023 [[paper](https://arxiv.org/abs/2304.04971)]

**Blurring-Sharpening Process Models for Collaborative Filtering**  
*Jeongwhan Choi, Seoyoung Hong, Noseong Park, Sung-Bae Cho*  
SIGIR 2023 – Apr 2023 [[paper](https://arxiv.org/abs/2211.09324)] [[code](https://github.com/jeongwhanchoi/BSPM)]

**Recommender Systems with Generative Retrieval**  
*Shashank Rajput, Nikhil Mehta, Anima Singh, Raghunandan Keshavan, Trung Vu, Lukasz Heldt, Lichan Hong, Yi Tay, Vinh Q. Tran, Jonah Samost, Maciej Kula, Ed H. Chi, Maheswaran Sathiamoorthy*  
non-archival – Mar 2023 [[paper](https://shashankrajput.github.io/Generative.pdf)]

**Generative Slate Recommendation with Reinforcement Learning**  
*Romain Deffayet, Thibaut Thonet, Jean-Michel Renders, and Maarten de Rijke*  
WSDM 2023 – Feb 2023 [[paper](https://arxiv.org/abs/2301.08632)]

**Recommendation via Collaborative Diffusion Generative Model**  
*Joojo Walker, Ting Zhong, Fengli Zhang, Qiang Gao, Fan Zhou*  
KSEM 2022 – Aug 2022 [[paper](https://dl.acm.org/doi/abs/10.1007/978-3-031-10989-8_47)]

## Knowledge Graph Generation

**From Retrieval to Generation: Efficient and Effective Entity Set Expansion**  
*Shulin Huang, Shirong Ma, Yangning Li, Yinghui Li, Hai-Tao Zheng, Yong Jiang*  
arXiv – Apr 2023 [[paper](https://arxiv.org/abs/2304.03531v1)]

**Crawling the Internal Knowledge-Base of Language Models**  
*Roi Cohen, Mor Geva, Jonathan Berant, Amir Globerson*  
arXiv – Jan 2023 [[paper](https://arxiv.org/abs/2301.12810)]

**Prompt Tuning or Fine-Tuning - Investigating Relational Knowledge in Pre-Trained Language Models**  
*Leandra Fichtel, Jan-Christoph Kalo, Wolf-Tilo Balke*  
AKBC 2021 – [[paper](https://openreview.net/pdf?id=o7sMlpr9yBW)]

**Language Models as Knowledge Bases?**  
*Fabio Petroni, Tim Rocktäschel, Patrick Lewis, Anton Bakhtin, Yuxiang Wu, Alexander H. Miller, Sebastian Riedel*  
EMNLP 2019 – Sep 2019 [[paper](https://arxiv.org/pdf/1909.01066.pdf)]

---

To get just the paper titles do `grep '\*\*' README.md | sed 's/\*\*//g'`
