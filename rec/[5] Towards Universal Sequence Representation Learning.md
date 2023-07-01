## From SASRec

https://zhuanlan.zhihu.com/p/235081694

- ID-based embedding
- Stacking Self-Attention Blocks
- predict: User representation * Item embedding matrix
  - User representation: output of the t-th SA block



## To UniSRec

Summary：

- 学习的是Item的通用表示
- 基础表示来自Bert对于word seq的embedding，使用CLS的embedding
  - Bert是fixed
- 使用不同的白化获得不同domain的item表示
- 使用MoE，通过gate在多个domain的item表示中加权得到通用表示vi
  - gate的输入为基础表示
- item seq级别的算法与SASRec相同

 https://zhuanlan.zhihu.com/p/532650980

- context-based embedding
  - The embedding of the item -> sentence -> CLS
  - comes from pretrained model
- for general domains
  - use several whitening transformation  to get transformed representation for each domain
  - use gk to gate&router different representations 
    - SoftPlus: smooth RELU
    - weighted average of all the representations
- contrastive task
  - S-I: sample a neg sample from the batch
    - to make the representation of the seq and the next item close
  - S-S: augment the sequence
    - drop item
    - drop word(token) in an item's content
    - to make the representation of the seq and the augmented seq close

- finetuning
  - fix the representation from encoder, only finetune the MoE to adapt to a new domain
  - inductive setting: the cases in the test set in not seen in the training set, no id embedding can be used
  - transductive setting: the ids of the test cases are seen in the training set