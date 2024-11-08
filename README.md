# CCLNet: Causal and Contrastive Learning Framework for Enhanced Pulmonary Embolism Detection

![](https://img.shields.io/badge/-Github-181717?style=flat-square&logo=Github&logoColor=FFFFFF)
![](https://img.shields.io/badge/-Awesome-FC60A8?style=flat-square&logo=Awesome&logoColor=FFFFFF)
![](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=Python&logoColor=FFFFFF)
![](https://img.shields.io/badge/-Pytorch-EE4C2C?style=flat-square&logo=Pytorch&logoColor=FFFFFF)

### Our paper has been accepted by BIBM 2024!
## Proposed method
We propose a new framework called CCLNet, which includes a contrastive learning component for addressing inter-modality heterogeneity and a causal learning component for handling intra-modality heterogeneity. Specifically, we achieve precise alignment between visual and tabular modalities by using global-level information to soften labels during contrastive learning. In addition, by using causal intervention methods to eliminate the influence of heterogeneous factors within the modality, we can accurately reveal the causal relationship between features and targets, thereby improving the accuracy and stability of the model. 

This code is a pytorch implementation of our paper "CCLNet: Causal and Contrastive Learning Framework for Enhanced Pulmonary Embolism Detection".

The figure below shows our proposed network.

![image](images/model.png)
