# Pre-train, Prompt and Recommendation: A Comprehensive Survey of Language Modelling Paradigm Adaptations in Recommender Systems

## 1 Introduction

Deep recommendation models:

- data hungry, likely to overfit without enough data
- bottleneck: data sparsity

prompt learning:

- rely on a suite of appropriate prompts
- reformulate the downstream tasks as the pre-training task

## 2 Generic Architecture of LMRS

## 3 Data Types

- Textual
- Sequential data: User-item interactions
- Graphs
- Multi-modal data

## 4 LMRS Training Strategies

### 4.1 Pre-train, fine-tune paradigm

Advantages:

- better generalization on different downstream recommendation tasks
- universal knowledge
- can avoid overfitting

#### Pre-train

Traditional end-to-end

#### Pre-train, fine-tune holistic model

fine-tune adjust the whole model parameters

#### Pre-train, fine-tune partial model

fine-tune partial parameters

#### Pre-train, fine-tune extra part of the model

fine-tune the extra parts