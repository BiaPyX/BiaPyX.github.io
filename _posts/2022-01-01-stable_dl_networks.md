---
layout: centered_article
title: Stable deep neural network architectures
docs_url: https://biapy.readthedocs.io/en/latest/workflows/semantic_segmentation.html
categories:
- Semantic segmentation
---

The goal is to segment automatically mitochondria in EM images as described in Semantic segmentation. This is a semantic segmentation problem where pairs of EM image and its corresponding mitochodria mask are provided. Our purpose is to segment automatically other mitochondria in images not used during train labeling each pixel with the corresponding class: background or foreground (mitochondria in this case). As an example, belown are shown two images from EPFL Hippocampus dataset used in this work:

<div class="row">
    <img height="230" width="230" src="../assets/images/tutorials/lucchi_test_0.jpg" alt="Lucchi dataset raw image">
    <img height="230" width="230"  src="../assets/images/tutorials/lucchi_test_0_gt.jpg" alt="Lucchi dataset GT image">
</div>
<br>

Citation:

```
Franco-Barranco, Daniel, Arrate Muñoz-Barrutia, and Ignacio Arganda-Carreras. "Stable deep neural network architectures for mitochondria segmentation on electron microscopy volumes." Neuroinformatics 20.2 (2022): 437-450.
```