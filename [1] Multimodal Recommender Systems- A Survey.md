

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

