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


## Requirements

- TensorFlow ≥ 2.10  
- Python ≥ 3.8  
- GPU with ≥ 15 GB VRAM (recommended)  
- System memory ≥ 16 GB (recommended)

Install required packages:



## 📁 Project Structure

```bash
├── model.ipynb     # Full model, training, and evaluation script
├── README.md                   # This file


## How to Run

1. Load and preprocess your dataset

You need to define and load `train_dataset`, `val_dataset`, and `test_dataset` using `tf.data.Dataset` or a generator. These datasets should yield images of shape `(256, 256, 3)` and binary masks of shape `(256, 256, 1)`.

2. Train the Model





