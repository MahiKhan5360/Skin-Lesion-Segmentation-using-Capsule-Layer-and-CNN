# Skin-Lesion-Segmentation-using-Capsule-Layer-and-CNN
Not Memory Efficient Version
# Capsule-Based CNN for Binary Image Segmentation (ISIC 2018)

This repository contains a custom deep learning architecture that integrates Capsule Networks into a CNN encoder-decoder framework for binary image segmentation (e.g., skin lesion segmentation from dermoscopic images like the ISIC 2018 dataset).

> ⚠️ **Warning**: The current model is **not memory-efficient** and may crash on systems with **<16 GB system RAM** and **<15 GB GPU memory** (e.g., T4 GPU with 15 GB).

---
## 🧠 Model Overview

The model combines:
- Convolutional layers for feature extraction (encoder)
- A **custom Capsule Layer** to learn spatial and part-whole relationships
- Upsampling and convolution (decoder) to recover spatial resolution
- Final sigmoid output for binary segmentation

### Architecture Highlights:
- Capsule layer after encoder
- Dynamic routing inside the Capsule Layer
- Batch normalization and dropout for regularization
- Uses Binary Crossentropy loss and Mean IoU metric

---

## 📁 Project Structure

```bash
├── model.ipynb     # Full model, training, and evaluation script
├── README.md                   # This file

