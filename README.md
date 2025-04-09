# AN2DL Projects: Image Classification & Semantic Segmentation

Welcome to the **Artificial Neural Nuggets** GitHub repository! This project contains two deep learning tasks developed as part of the *Advanced Neural Networks and Deep Learning* course. Each task is implemented in **Jupyter Notebooks**, and is accompanied by a detailed report.

## 🧠 Projects Overview

### 1. Blood Cell Image Classification

- **Objective**: Classify images of blood cells into one of eight classes from 96x96 RGB images.
- **Approach**: 
  - Data preprocessing: outlier removal, class balancing via oversampling, and custom data augmentation (including RandAugment and class-specific transforms).
  - Transfer learning: leveraged pre-trained EfficientNet variants.
  - Model head: global average pooling, Swish activations, dropout, and group normalization.
  - Fine-tuning: freezing batch norm layers, optimizing with Adam, early stopping, and learning rate scheduling.
- **Results**:
  - Achieved **98.88% accuracy** with **EfficientNetV2S**, with strong precision and recall metrics.
- 📄 Read the full report: [`report.pdf`](./challenge_1/report.pdf)

### 2. Mars Terrain Semantic Segmentation

- **Objective**: Perform semantic segmentation on Mars terrain images to identify terrain types and geological features.
- **Approach**:
  - Data augmentation: applied copy-paste augmentation and general geometric transforms to handle class imbalance.
  - Architecture: a nested U-Net with enhancements like **Dilated Spatial Pyramid Pooling**, **Dual Attention Units**, and experiments with **transformer blocks**.
  - Loss function tuning: experimented with Dice, Focal, and Sparse Categorical Cross-Entropy; final model used the latter.
- **Results**:
  - Achieved **69.91% mean IOU** using Dual Attention + DSPP blocks.
- 📄 Read the full report: [`report.pdf`](./challenge_2/report.pdf)

---

## ⚙️ Technologies Used

- Python 3.10+
- TensorFlow / Keras
- NumPy, Pandas, Matplotlib, Seaborn
- Scikit-learn
- EfficientNet (via `tensorflow.keras.applications`)
- U-Net, U-Net++ inspired architectures
- Custom data augmentation and preprocessing pipelines

---

## 📌 Authors

**Luca Cattani, Simone Lucca, Manuela Marenghi, Andrada Theodora Pascu**  
*Artificial Neural Nuggets - AN2DL @ 2024*
