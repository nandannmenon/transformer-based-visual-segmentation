# Transformer-Based Visual Segmentation

This project explores and implements Transformer-based and CNN-based models for visual segmentation tasks including semantic, instance, and panoptic segmentation. The goal is to compare the qualitative results and performance of both approaches using standard segmentation metrics.

We conducted this work as part of our academic learning to better understand modern computer vision architectures and their practical implementation.

---

## Project Overview

Image segmentation is an essential computer vision task where an image is divided into meaningful regions. CNNs have traditionally dominated this area, but Transformer-based models have recently gained attention for their ability to capture long-range dependencies.

In this project, we implemented and compared both architectures for:

- **Semantic Segmentation**
- **Instance Segmentation**
- **Panoptic Segmentation**

We focused on understanding architectural differences, model behavior, and qualitative performance using a subset of the COCO dataset.

---

## Objectives

- Implement CNN and Transformer-based models for key segmentation tasks
- Compare segmentation outputs qualitatively
- Explore implementation differences and performance trade-offs

---

## Models Implemented

### Semantic Segmentation
- **CNN:** DeepLabV3  
- **Transformer:** SegFormer  

### Instance Segmentation
- **CNN:** Mask R-CNN  
- **Transformer:** Mask2Former  

### Panoptic Segmentation
- **CNN:** Panoptic FPN  
- **Transformer:** Mask2Former  

---

## Dataset

We used a subset of the **COCO (Common Objects in Context)** dataset, which provides:
- Pixel-wise annotations
- Bounding boxes
- Panoptic segmentation labels

Due to hardware limitations, only a portion of the validation set was used for analysis and visualization.

---

## Evaluation Metrics

- **mIoU (Mean Intersection over Union)** for semantic segmentation  
- **PQ (Panoptic Quality)** for panoptic segmentation  

These metrics provide insights into the accuracy and completeness of segmentation.

---

## Implementation Details

### Environment
- Platform: Google Colab  
- Hardware: Tesla T4 GPU  
- Libraries: Hugging Face, Detectron2, PyTorch

### Workflow
- Load pretrained models
- Preprocess input images (resize, normalize)
- Run inference
- Visualize outputs (segmentation masks, class labels, bounding boxes)

---

## Results and Analysis

### Observations
- **Transformer-based models** produced sharper segmentation boundaries, especially for small or overlapping objects.
- **CNN-based models** were faster and worked well for larger, distinct objects.
- **Panoptic segmentation** was more consistent with Transformer models, though more computationally demanding.

---

## Challenges

- **Hardware limitations** restricted full dataset evaluation.
- **Transformer models** required more memory and were occasionally unstable in Colab.
- **Metric computation** was limited due to evaluation constraints; emphasis was placed on qualitative analysis.

---

## Conclusion

This project helped us explore the differences between CNN and Transformer-based segmentation models through hands-on implementation. While Transformers show strong potential, they also introduce practical challenges in terms of resources and complexity. This experience improved our understanding of model design and performance in real-world computer vision tasks.

---

## References

1. Chen et al., "Rethinking Atrous Convolution for Semantic Image Segmentation", arXiv:1706.05587
2. Xie et al., "SegFormer: Simple and Efficient Design for Semantic Segmentation with Transformers", NeurIPS 2021
3. Cheng et al., "Masked-attention Mask Transformer for Universal Image Segmentation", CVPR 2022
4. Lin et al., "Microsoft COCO: Common Objects in Context", ECCV 2014

---


