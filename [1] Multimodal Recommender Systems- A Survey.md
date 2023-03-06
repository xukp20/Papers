

# [1] Multimodal Recommender Systems: A Survey

MRS: Multimodal Recommender System 

## Introduction

### Procedures of MRS

- Raw Feature Extracting：
  - tabular features + multimodal features
  - $v_f, v_{image}, v_{text}$

- Feature Interaction
  - interact between Vs
- Recommendation
  - interact between user and item's v

### Taxonomy

Three categories of tasks:

- Feature Interaction 
  - fuse various modality features 
- Feature Enhancement 
  - limited data
  - contrastive learning, disentangled learning
- Model Optimization
  - lightweight recommendation models
  - parameterized modality encoder



## Feature Interaction

to realize the nonlinear transformation of feature space to common space 

Three types of interaction

### Bridge

to capture the inter-relationship between users and items considering multimodal information

- get representation from the latent item-item graph

model:

- User-item graph
  - no difference between different modalities
    - MMGCN: a user-item graph for each modality
    - GRCN: upgrade by deleting incorrect interaction data when training
  - consider user's preference for different modallities
    - DualGNN: use correlation (user co-occurrence graph) between users to learn user preferences
    - MMGCL: new multimodal graph contrastive learning method 
      - modal edge loss, modal masking
      - novel negative sampling technique -> correlation between modalities
    - MGAT: gated attention based on MMGCN to catch preference for modalities
- Item-item Graph
  - LATTICE: item-item graph for each modality from user-item graph
  - MICRO: new comparison method
  - HCGCN: clustering graph convolutional network 
    - first groups item-item and user-item graphs
    - dynamic graph clustering
  - PMGT: pre-trained graph transformer, Bert structure
  - BGCN: bundle recommendation, to recommend a bundle of items at a time
    - user-item interaction, user-bundle interaction, bundle-item affiliation
  - Cross-CBR: user-bundle graph + user-item diagram + item-bundle graph
    - contrastive learning: to encode the similar items similarly

- Knowledge Graph
  - MKGAT: first to introduce KG
  - SI-MKR: 
    - alternate training: 多任务学习
    - knowledge graph representation based on MKR
  - MMKGV: graph attention network
  - CMCKG: two modals -> to maximize consistency between two
    - descriptive attributes
    - structural connections 

### Fusion

it aims at combining various preferences to modalities

attention: most used

- Coarse-grained Attention：粗粒度的Attention

  - UVCAN
  - MCPTR
  - CMBF: cross-attention, 分别学习image和text的语义信息
  - different proportions of Attention:
    - MML: attention based on id, assisted by visual & text
    - MCPTR: each modal equal, self-attention -> fusion weight
    - HCGCN: more on visual & text info

- fine-grained Attention

  - >  coarse-grained fusion is often invasive and irreversible

  - POG: online clothing, transformer, encoder
  - NOR: encoder-decoder
  - EFRM: 
    - a Semantic Extraction Network: SEN
  - VECF: image segmentation
  - UVCAN: video -> image
  - MM-Rec: 
    - the target detection algorithm Mask-RCNN,
    - fuses POI with news content using co-attention

- Combined-Attention

- Others

### Filtration

过滤

multimodal data may includes unrelated information

to filter out noisy data

two types:

- exist in interaction graph: bridge part
- exist in the multimodal feature itself: fusion part

methods:

- image processing
  - VECF, UVCAN: image segmentation to remove noise
  - MM-Rec: target detection
- graph neural networks
  - FREEDOM:  degree-sensitive edge pruning method
  - GRCN: prune wrong interaction information
  - PMGCRN
  - MEGCF



## Multimodal Feature Enhancement

to handle sparsity problem

### Disentangled Representation Learning

解纠缠表示学习

不同的模态特征对于user preference 有不同的影响，而同一个样本的多模态feature很多是相互纠缠的，因此需要将不同的模态feature彼此拆分出来，学习各自的表示

### Contrastive Learning

data augmentation 

#### CL Loss

Contrastive learning 对比学习的目标是使在学习到的embedding space中，相似的item距离尽量近，而不相似的item尽量远

这里是将同一个item的多个模态feature的embedding 尽量相似



## Model Optimization

two categories:

- End to end 
- Two step
