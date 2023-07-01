# A Comprehensive Survey on Transformers for Computer Vision Applications

## 1 Introduction

Vision Transformers (ViTs)

Transformers on images:

- problem: too many pixels -> time-consuming, memory-intensive
- solutions: 
  - divide the image into patches
  - each patch as a token -> embedding 
  - transformer encoder
  - MLP for downstream tasks

Swin transformer

compared with CNNs:

- more general

## 2 Related Work

pass

## 3 Application of ViTs in CV

#### Image Classification

images -> patches -> encoder -> mlp for classification

models:

- CrossViT
- CTNet: remote sensing
- MIL-ViT
- DHViT

#### Object Detection

#### Image Segmentation

#### Image Compression

#### Image Super Resolution



## 4 Open Research Challenges And Future Directions

#### High Computational Cost

#### Large Training Dataset

#### Neural architecture search (NAS)

what's the best/better architectures of ViT models

#### Interpret-ability of the transformers

to visualize the relative contribution of the input tokens to the final predictions

#### Hardware efficient designs

too heavy

