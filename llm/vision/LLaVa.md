## Visual Instruction Tuning

General Purpose Vision model for Instructions

Multimodal model for multiple tasks

### Data Generation

Use GPT, context:

- Captions
- Boxes

### VIT

#### Architecture

Image -> CLIP ViT ->  Embedding -> Projection to word space

#### Training

- Stage1: Task is to describe the image, target is the captions, froze ViT and LLM, **Only train projection matrix**
  - To align the ViT with frozen LLMs
- Stage2: Finetuning End to End, froze ViT, finetune Projection and LLM

### Experiments

#### ScienceQA

