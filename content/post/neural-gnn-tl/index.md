---
title: Neural Decoding Using Graph Neural Network and Transfer Learning
subtitle: A data-driven neural decoding method

# Summary for listings and search engines
summary: Maybe this is a new perspective?

# Link this post with a project
projects: []

# Date published
date: "2022-02-13T00:00:00Z"

# Date updated
# lastmod: "2020-12-13T00:00:00Z"

# Is this an unpublished draft?
draft: true

# Show this page in the Featured widget?
featured: true

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**SingularityHub**](https://singularityhub.com/2019/05/01/scientists-created-a-neural-decoder-that-translates-brain-activity-into-speech/)'
  focal_point: ""
  placement: 2
  preview_only: true

authors:
- admin

tags:
- Brain
- Deep Learning
- GNN

categories:
- Research
---

### What is neural decoding?

A human brain can be considered as an encoder-decoder architecture in terms of its interaction with the environment. For the encoding model part, it predicts how the brain encodes one's perceptions (visual, auditory, motor, and etc.) into the brain response. While the decoding model part should give reasonable predictions on one's perception given the response/activity of the brain.

<figure>
  <img src="https://www.researchgate.net/profile/Gael-Varoquaux/publication/268794316/figure/fig1/AS:282616113713184@1444392340570/Schematics-of-the-distinction-between-encoding-and-decoding-in-brain-imaging_W640.jpg" width="300px" height="auto"/>
  <figcaption>
    <a href="https://www.researchgate.net/publication/268794316_How_machine_learning_is_shaping_cognitive_neuroimaging">Varoquaux et al.</a>
  </figcaption>
</>

In our work, we try to prove that using novel graph neural network (GNN) architecture and transfer learning (TL) to model the decoding is a better idea. In addition, we would also like to analyze the characterize the brain's activity using the intermediate representation of the neural network.

### Graph Neural Network: Designed for Network Data

A human brain consists of many regions. Some of them may co-work to finish some task. To characterize the functionality of the brain, researchers conceptualized the "Brain Atlas", which clusters the regions of brain according to the function they are involved. That introduces a topological relation among all the regions of the brain. If we denote a cluster of regions of a brain as a node $n$ where $n \in N$, and the functional relation between two regions as an edge $e$ where $e\in E$. Thus, the brain can be denoted as a graph (or a network) $G$, where $G=\set{N, E}$.

GNN is a deep learning module applied on graph data. With its ability to extract and utilize the information underlying the topology, it is now a promising part to perform a deep learning task on non-Euclidean data. As we illustrated above, the decoding model with GNN-based structure, may fully utilize a brain function atlas, given its essence of the graph structure.

### Transfer Learning: Learn Like A Human Brain with Machine Learning

Transfer learning addresses the generalization ability of the trained model, and so does one's brain. Usually, human brain learns how to finish a task on a limited set of data and then have the ability to deal with unseen data. Inspired by that, we expect our model can also behaves just like the human brain with better generalization ability on other datasets or even cross domain task.

### Our Scope

Previous work<sup>[1-3]</sup> has proved GNN is a promising technique and how the transfer learning process affect the learning of the model. Besides, the interpretability of the model is also explained in the BrainGNN work<sup>[1]</sup> in particular. Therefore, building on the success of these efforts, we would like to investigate a novel GNN- & transfer-learning-based machine learning framework performance on simulating the neural decoding process and behavioral prediction. With transfer learning, even it is possible to generalize to perform cross domain tasks, such as brain disease prediction, which is more convincing that the model captures underlying representation of brain structure.

### Datasets

[Human Connectome Project (HCP)](https://www.humanconnectome.org/study/hcp-young-adult/document/1200-subjects-data-release) dataset and [Individual Brain Charting (IBC)](https://openneuro.org/datasets/ds000244/versions/1.0.0) dataset containing similar human cognitive subjects will be used in our experiments.

### Experiments and Results

To be finished ... 

#### References

[1] Li, X., Zhou, Y., Dvornek, N., Zhang, M., Gao, S., Zhuang, J., Scheinost, D., Staib, L. H., Ventola, P., & Duncan, J. S. (2021). BrainGNN: Interpretable Brain Graph Neural Network for fMRI Analysis. Medical Image Analysis, 74, 102233. <br>
[2] Zhang, Y., & Bellec, P. (2020). Transferability of Brain decoding using Graph Convolutional Networks (p. 2020.06.21.163964). <br>
[3] Zhang, Y., Tetrel, L., Thirion, B., & Bellec, P. (2021). Functional annotation of human cognitive states using deep graph convolution. NeuroImage, 231, 117847. 
