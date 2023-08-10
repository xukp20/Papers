### Abstract

Outcome supervision < process supervision

On MATH dataset, release PRM800K (?)

Focus on training the most reliable reward model, not finetuning the generator

Two scales:

- Large: based on GPT4, no RLHF
- Small: same structure, less computation, add a pretraining phase for MathMix set



#### Process

##### generator

Train one epoch with the format of step-by-step to learn the format

From the LARGE scale model

##### Data

to label each step with 1, 0, -1

more useful: convincing wrong-answer solutions 



### 4 Small-scale Synthetic Supervision

Use PRMlarge(trained as PRM with human supervision) as the supervision for smaller model



### 6 Discussion

 the marginal value of a negative label from outcome supervision is low: most solutions has a mistake in them -> "where" is more important than "whether"



