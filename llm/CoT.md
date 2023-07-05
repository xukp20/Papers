## Chain-of-Thought Prompting Elicits Reasoning in Large Language Models

blogs:

- [如何更好的理解思维链 Chain of Thought (CoT) - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/622213602)
- [Chain of Thought 开山之作论文详解 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/582758381)



### Arithmetic Reasoning

#### Results

- larger model, more gain
- more complicated problem, more gain
- CoT prompting on GPT-3 and PaLM better than SOTA( finetuned models )

#### Ablation Study

- Equation only: output only a mathematical equation before giving the answer
- Variable compute only: Use ... to note different computation time
- Chain of thought after answer: Let prompt be *answer + chain* instead of *chain + answer*

#### Robustness

Different annotators



### Commonsense Reasoning

