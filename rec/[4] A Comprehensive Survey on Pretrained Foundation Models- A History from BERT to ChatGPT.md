# A Comprehensive Survey on Pretrained Foundation Models- A History from BERT to ChatGPT

Pretraining: transfer learning

- GPT: autoregressive language model
- BERT: contextual language model

## 1 Introduction

### 1.1 PFMs and Pretraining

pretraining:

- Early pretraining: static technique: NNLM, Word2Vec
- dynamic pretraining: BERT, XLNet

#### ChatGPT

fine-tuned from GPT-3.5

reinforcement learning from human feedback (RLHF)



unified PFMs: PFMs handling multimodal data



### 1.2 Contribution and Organization



## 2 Basic Components 

### 2.1 Transformer for PFMs

### 2.2 Learning Mechanisms for PFMs

#### Supervised Learning

#### Semi-Supervised Learning

既有标记数据又有无标记数据

使用标记数据学习到label的encoder f，对于无标记的数据，使用与有标记数据集X的关系生成伪标签，得到无标记数据的encoder f'

#### Weakly-Supervised Learning

标签不全，不精确（对于一个包内的x都使用同一个标签），不正确

#### Self-supervised Learning

#### Reinforcement Learning

get reward from the environment



### 2.3 Pretraining Tasks for PFMs

#### 2.3.1 NLP

- MLM
- DAE: Denoising AutoEncoder, used the noised corpus to reconstruct the original corpus
- RTD: Replaced Token Detection
- NSP
- SOP

#### 2.3.2 CV

- Specific pretext task: 有固定的前置任务
- Frame Order Learning Task: videos 
- Data Generation
- Data reconstruction: missing patches