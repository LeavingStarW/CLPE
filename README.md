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

 ## Experiment result
   We compare our model with some state-of-the-art multimodal methods, single image methods and single table methods. The experimental results show that our model is superior to these methods whether it is a single image module, a single table module or a whole multimodal framework.
<table>
<thead>
  <tr>
    <th>Methods</th>
    <th>AUROC</th>
    <th>ACC</th>
    <th>F1 score</th>
    <th>Sensitivity</th>
    <th>Specificity</th>
    <th>NPV</th>
    <th>PPV</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>3D ResNet50</td>
    <td>0.740</td>
    <td>0.679</td>
    <td>0.667</td>
    <td>0.634</td>
    <td>0.725</td>
    <td>0.659</td>
    <td>0.703</td>
  </tr>
  <tr>
    <td>PENet</td>
    <td>0.834</td>
    <td>0.790</td>
    <td>0.795</td>
    <td>0.805</td>
    <td>0.775</td>
    <td>0.795</td>
    <td>0.786</td>
  </tr>
  <tr>
    <td>PECon(image-only)</td>
    <td>0.838</td>
    <td>0.802</td>
    <td>0.797</td>
    <td>0.768</td>
    <td>0.838</td>
    <td>0.779</td>
    <td>0.829</td>
  </tr>
  <tr>
    <td>TabNet</td>
    <td>0.877</td>
    <td>0.879</td>
    <td>0.895</td>
    <td>0.891</td>
    <td>0.863</td>
    <td>0.852</td>
    <td>0.899</td>
  </tr>
  <tr>
    <td>PEFusion(tabular-only)</td>
    <td>0.921</td>
    <td>0.877</td>
    <td>0.877</td>
    <td>0.866</td>
    <td>0.887</td>
    <td>0.866</td>
    <td>0.877</td>
  </tr>
  <tr>
    <td>PECon(tabular-only)</td>
    <td>0.918</td>
    <td>0.895</td>
    <td>0.898</td>
    <td>0.915</td>
    <td>0.875</td>
    <td>0.909</td>
    <td>0.882</td>
  </tr>
  <tr>
    <td>PEFusion</td>
    <td>0.961</td>
    <td>0.901</td>
    <td>0.908</td>
    <td>0.963</td>
    <td>0.838</td>
    <td>0.957</td>
    <td>0.859</td>
  </tr>
  <tr>
    <td>PECon</td>
    <td>0.960</td>
    <td>0.914</td>
    <td>0.919</td>
    <td>0.963</td>
    <td>0.863</td>
    <td>0.958</td>
    <td>0.878</td>
  </tr>
  <tr>
    <td>PE-MVCNet</td>
    <td>0.938</td>
    <td>0.907</td>
    <td>0.912</td>
    <td>0.951</td>
    <td>0.863</td>
    <td>0.945</td>
    <td>0.876</td>
  </tr>
  <tr>
    <td>CCLNet(image-only)</td>
    <td>0.831</td>
    <td>0.809</td>
    <td>0.803</td>
    <td>0.768</td>
    <td>0.850</td>
    <td>0.782</td>
    <td>0.840</td>
  </tr>
  <tr>
    <td>CCLNet(tabular-only)</td>
    <td>0.931</td>
    <td>0.901</td>
    <td>0.906</td>
    <td>0.939</td>
    <td>0.863</td>
    <td>0.932</td>
    <td>0.875</td>
  </tr>
  <tr>
    <td>CCLNet</td>
    <td>0.966</td>
    <td>0.926</td>
    <td>0.930</td>
    <td>0.976</td>
    <td>0.875</td>
    <td>0.972</td>
    <td>0.889</td>
  </tr>
</tbody>
</table>

 We compare our intermodal alignment approach to the currently popular methods CrossAttention and CLIP. Experimental results show that our proposed intermodal alignment method is superior to the two methods.
<table>
<thead>
  <tr>
    <th>Methods</th>
    <th>AUROC</th>
    <th>ACC</th>
    <th>F1 score</th>
    <th>Sensitivity</th>
    <th>Specificity</th>
    <th>NPV</th>
    <th>PPV</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>CrossAttention</td>
    <td>0.967</td>
    <td>0.914</td>
    <td>0.918</td>
    <td>0.951</td>
    <td>0.875</td>
    <td>0.946</td>
    <td>0.886</td>
  </tr>
  <tr>
    <td>CLIP(InfoNCE)</td>
    <td>0.965</td>
    <td>0.920</td>
    <td>0.925</td>
    <td>0.976</td>
    <td>0.863</td>
    <td>0.972</td>
    <td>0.879</td>
  </tr>
  <tr>
    <td>CCLNet</td>
    <td>0.966</td>
    <td>0.926</td>
    <td>0.930</td>
    <td>0.976</td>
    <td>0.875</td>
    <td>0.972</td>
    <td>0.889</td>
  </tr>
</tbody>
</table>

