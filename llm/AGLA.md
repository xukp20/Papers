Aligned AI system: helpful, honest and harmless

Questions:

- Is naive prompting a workable baseline for alignment? How does it scale, how does it compare to finetuning, and how can we leverage its advantages?
- When and how much does preference modeling improve on imitation learning?
  - preference modeling: use human preference 
  - imitation learning: imitate human moving history
- How can we improve the sample efficiency of preference modeling? 



Contributions: Section 1.3



### 2 Conditioning on Aligned Behavior

#### Prompt

prompt as examples, not contain explicit call for HHH, get better results

#### Context Distillation

to avoid: window occupied, computation loss

- finetune on the prompt (treated as a small dataset)
- distillation: new model generate X = old model generate X when given C

#### Evaluation

##### Toxicity

##### Human Preferences and Model Performance

Human evaluation -> Elo Score for ranking



### 3 Scaling of Preference Modeling vs Imitation Learning

#### Definitions

- Imitation Learning: Here we simply train language models to imitate ‘good’ behavior via supervised learning with the usual cross-entropy loss. 
- Binary Discrimination: Given a sample of ‘correct’ behavior and a sample of ‘incorrect’ behavior, train the model to distinguish between the two. 
- Ranked Preference Modeling: Given a dataset of samples whose overall ‘quality’ is ranked in some way, we train models to output a scalar quality score10 for each sample whose value matches the ranking as closely as possible.

> The ranked preference in this paper is always 2 compare, so same as the binary. The binary are treated as a 2 compare ranking model -> The same

#### Loss

##### Preference and Imitation

Add a value head for generating "score" after all the tokens
$$
L_{PM} = log(1 + e^{r_{bad} - r_{good}})
$$

##### Imitation

Train: sum of neg log-prob

Eval: avg (for different length) of ...

##### Conclusion

- binary: similar
- rank: Preference better



### 4 Preference Model Pre-Training and Transfer

PMP TODO!