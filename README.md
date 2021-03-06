
This repo is the implementation for paper "Improve Gender, Race, and Age classification with
Supervised Contrastive Learning"

Accepted in "2021 International Symposium on Intelligent Signal Processing and Communication Systems (ISPACS)" but I withdrew due to the conflicting of my mid-term examination period.


# Pre-printed version

https://www.researchgate.net/publication/355022065_Improve_Gender_Race_and_Age_classification_with_Supervised_Contrastive_Learning

# Abstract

Automated gender, age, and ethnicity classification have important applications in various fields of life. There are many methods to improve the performance of the task, and deep learning approaches have shown superiority compared to traditional techniques. Furthermore, the cross-entropy loss is most widely used in those works despite its weakness as lack of robustness to noisy labels, poor margins, and low generalization. Meanwhile, contrastive loss methods significantly outperform traditional cross-entropy loss in many other image classification tasks. In this study, we apply multi-output supervised contrastive loss on Resnet-50 compared to the conventional cross-entropy loss. We evaluate our method on 3 recent datasets for gender, age, and race classification called FairFace, UTKFace, and Asian Face Age Dataset (AFAD), and show it significantly improves the accuracy in most of the tasks in all datasets.

# Dataset

We already re-annotated the original datasets for grouping Age and Race groups. Please download and extract the compressed files at root folder of the project.

- FairFace: https://drive.google.com/file/d/1ILVNOBfkd8Ytlp1N055RWoD3sljBhRjq/view?usp=sharing
- UTKFace: https://drive.google.com/file/d/1cGIKU3RtkPruznFWO4DIpkyr7egwCCo6/view?usp=sharing
- AFAD-Full: https://drive.google.com/file/d/1BXWeO606BvcCNFJ7HpiF7ETW2Ien4th2/view?usp=sharing

# Code

In each Notebook, there are 2 phases of training, first one for training from scratch and the second one for Supervised contrastive learning implementation.

After the deadline is extended, we apply more Augmentation methods and increase the image size in Version 1.

## Version 1:

Setting:

- Batch size: 64
- Image size 224x224
- Augementation: RandomFlip, RandomRotation, RandomWidth, RandomHeight, RandomTranslation, and RandomContrast

Code:

- Scratch - and SupCon - AFAD-Full - R50 - MultiOutput - AutoAug - 224.ipynb: Train on AFAD-Full dataset.
- Scratch - and SupCon - UTKFace - R50 - MultiOutput - AutoAug - 224.ipynb: Train on UTKFace dataset.
- Scratch - and SupCon - FairFace - R50 - MultiOutput - AutoAug - 224.ipynb: Train on FairFace dataset.

Result:

Directory result/V1/*.csv/xlsx

## Version 0

Setting:

- Batch size: 64
- Image size: 112x112
- Augementation: RandomFlip, RandomRotation, RandomWidth, RandomHeight

Code:

- Scratch - and - SupCon - AFAD-Full - R50 - MultiOutput.ipynb: Train on AFAD-Full dataset.
- Scratch - and - SupCon - UTKFace - R50 - MultiOutput.ipynb: Train on UTKFace dataset.
- Scratch - and SupCon - FairFace - R50 - MultiOutput.ipynb: Train on FairFace dataset.

Result:

Directory result/V0/*.csv/xlsx

# Reference

- Keras implementation instruction: https://keras.io/examples/vision/supervised-contrastive-learning/
- Supervised Contrastive Learning: https://proceedings.neurips.cc/paper/2020/file/d89a66c7c80a29b1bdbab0f2a1a94af8-Paper.pdf
- FairFace dataset: https://github.com/joojs/fairface
- UTKFace dataset: https://susanqq.github.io/UTKFace/
- AFAD dataset: https://afad-dataset.github.io/


