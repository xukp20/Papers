## From SASRec

https://zhuanlan.zhihu.com/p/235081694

- ID-based embedding
- Stacking Self-Attention Blocks
- predict: User representation * Item embedding matrix
  - User representation: output of the t-th SA block



## To UniSRec

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