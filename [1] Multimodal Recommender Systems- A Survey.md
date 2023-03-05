

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
    - DualGNN