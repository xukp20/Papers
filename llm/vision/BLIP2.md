## BLIP-2: Bootstrapping Language-Image Pre-training with Frozen Image Encoders and Large Language Models

[BLIP-2：使用冻结图像编码器和大型语言模型的语言-图像预训练 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/602360202)

- Stage1：Get Query -> find visual representation related to text
- Stage2: Add LLM, output text



![image-20230706224652583](..\pngs\Q-Former.png)

Q-Former:

- Image-Text Contrastive Learning: similarity of text & image
  - Q -> Image Transformer, Text -> Text Tranformer, align
- Image-grounded Text Generation
- Image-Text Matching: binary classification task, whether is a pair



- Fully connect projection