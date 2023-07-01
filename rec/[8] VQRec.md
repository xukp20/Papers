Bert -> Item embedding from PLM -> separate into codes -> min distance to the pre-set codes -> coding embedding -> mean for item embedding -> SASRec -> seq embedding



#### Pretrain

##### Negative sampling

- item: 以已有item的indice index为中心，1-p概率不变，p概率随机选取
- seq：原始样本都是in domain的seq，而一个batch内的不同样本是cross domain的，使用inbatch neg sampling自然得到cross domain的负样本



#### PQ

一种聚类方式

将原始的text embedding -> D 段

所有样本的同一段进行聚类，得到M个center

text embedding被变为D个index，每个对应一个段的center编号



#### Finetune

由于不同domain的text分布不一样，重新进行了PQ，将得到的M * D的centers使用矩阵重排序，以期得到与原来一样的embedding排列

- train 矩阵，使用doubly stochastic matrix
- finetune embedding，固定Θ，上一步的映射

