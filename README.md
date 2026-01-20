 EEG-SubjectID-CNN

This repository contains a Convolutional Neural Network (CNN) model for **EEG-based subject identification**. The model classifies EEG signals recorded during **Arabic speech processing** to identify individual subjects.

---

## **Features**

- Multi-class classification for **12 subjects**
- Temporal and spatial feature extraction using:
  - `Conv2D` for temporal patterns
  - `DepthwiseConv2D` for spatial/channel patterns
- Optional **Refining Blocks (Residual Dense layers)** for enhanced learning
- Global Average Pooling before the final softmax output
- Achieves **~86% test accuracy** on the dataset
- Includes visualization of:
  - Training/Validation Accuracy & Loss
  - Confusion Matrix
  - Sample prediction heatmaps

---

## **Dataset**

The dataset used is `RIGHT_Real.csv`, containing EEG recordings for multiple subjects.

- **EEG Channels:** 8
- **Time Points per Trial:** 1200
- **Subjects:** 12 (subject0 is excluded)

**Note:** Make sure your dataset follows the column naming convention `v1, v2, ..., v9600` (8 channels × 1200 time points).

---

## **Requirements**

- Python 3.8+
- TensorFlow 2.x
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
