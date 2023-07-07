## Cheap and Quick: Efficient Vision-Language Instruction Tuning for Large Language Models

End to end scheme

Existing ways:

- Expert System: LLM to interpret instructions, Vision model to do the task
- modular training of LLMs: add a neck branch from Vision to LLM
- MMA: light adaptor, routing scheme

![image-20230707164523230](..\pngs\LaVIN.png)

#### MM-Adapter

![image-20230707165130236](..\pngs\MM-Adaptor.png)

modality token -> choose router

![image-20230707165342363](..\pngs\LaVIN_router.png)

m -> tm -> w weight of each modal

#### MMT

freeze ViT and LLM, only train adaptor

**no VL pretraining to align ViT with LLM**

end to end